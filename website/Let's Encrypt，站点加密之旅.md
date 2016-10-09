# Let's Encrypt，站点加密之旅

> HTTPS（全称：Hyper Text Transfer Protocol over Secure Socket Layer），是以安全为目标的HTTP通道，简单讲是HTTP的安全版。即HTTP下加入SSL层，HTTPS的安全基础是SSL，因此加密的详细内容就需要SSL。
>
> Let's Encrypt，是2016年4月12日成立的一家证书授权中心，提供免费的传输层安全（TLS）X.509证书，通过自动化的过程消除目前安全网站证书需要手工创建，加密，签名，安装以及更新的复杂性。

一直以来都觉得浏览器网址开头的那把小绿锁很别致啊，现在Let's Encrypt横空出世提供免费证书，说明https势在必行，那我也来动手给博客加把锁吧，看着就安全是吧。

Let's Encrypt 的[官网](https://letsencrypt.org/)提供的脚本看起来更加自动化一些，但我没有亲自尝试，而是在Github上搜到了一个开源脚本[acme-tiny](https://github.com/diafygi/acme-tiny)，用下来之后成功将博客加密完成。

![file](https://dn-phphub.qbox.me/uploads/images/201609/06/1/wTcqowDx3C.png)

根据acme-tiny提供的说明文档和我自己的实施过程列出以下几步：

### 克隆脚本

```
sudo git clone https://github.com/diafygi/acme-tiny.git  
cd acme-tiny
```

### 创建Let's Encrypt私钥

```
openssl genrsa 4096 > account.key
```

### 创建CSR(Certificate Signing Request，证书签名请求) 文件

> ACME协议 (Let's Encrypt所使用的) 需要一个csr文件，用来进行证书签名和证书更新。

将需要加密的域名加到下面的代码中，目前一张证书最多可以加密 100 个域名：

```
openssl genrsa 4096 > domain.key     
openssl req -new -sha256 -key domain.key -subj "/" -reqexts SAN -config <(cat /etc/ssl/openssl.cnf <(printf "[SAN]\nsubjectAltName=DNS:yoursite.com,DNS:www.yoursite.com")) > domain.csr
```

### 证明你拥有该域名

acme-tiny脚本会生成验证文件并写入到你指定的目录下，然后通过 ".well-known/acme-challenge/" 这个URL来访问到验证文件. 注意: Let's Encrypt 会对你的服务器做一次http请求来进行验证，因此你需要保证80端口能够访问.

- 手动生成challenges目录，用来存放验证文件（路径可以根据需要修改）

  mkdir -p /var/www/challenges

- 配置nignx的80端口

```
    server {

        listen 80;
        server_name yoursite.com www.yoursite.com;
        return 301 https://yoursite.com$request_uri; # 注意进行301重定向到https，否则通过http仍能访问你的站点

        location /.well-known/acme-challenge/ {
            alias /var/www/challenges/;
            try_files $uri =404;
        }

        #...你的其他配置
    }
```

### 获取签名证书

```
sudo chmod +x acme_tiny.py  
python acme_tiny.py --account-key ./account.key --csr ./domain.csr --acme-dir /var/www/challenges/ > ./signed.crt
```

### 安装证书

针对nginx, 你还需要将 Let's Encrypt 的中间件证书 intermediate.pem 内容附加在签名证书signed.crt之后：

```
    wget -O - https://letsencrypt.org/certs/lets-encrypt-x3-cross-signed.pem > intermediate.pem  
    cat signed.crt intermediate.pem > chained.pem

    server {
        listen 443;
        server_name yoursite.com, www.yoursite.com;

        ssl on;
        ssl_certificate /path/to/chained.pem;
        ssl_certificate_key /path/to/domain.key;
        ssl_session_timeout 5m;
        ssl_protocols TLSv1 TLSv1.1 TLSv1.2;
        ssl_ciphers ECDHE-RSA-AES256-GCM-SHA384:ECDHE-RSA-AES128-GCM-SHA256:DHE-RSA-AES256-GCM-SHA384:ECDHE-RSA-AES256-SHA384:ECDHE-RSA-AES128-SHA256:ECDHE-RSA-AES256-SHA:ECDHE-RSA-AES128-SHA:DHE-RSA-AES256-SHA:DHE-RSA-AES128-SHA;
        ssl_session_cache shared:SSL:50m;
        ssl_prefer_server_ciphers on;

        #...你的其他配置
    }
```

### 证书自动更新定时任务

恭喜！你的网站已经使用上了HTTPS。 但Let's Encrypt 证书有效期只有90天, 所以需要定期更新。现在只需要写一个更新脚本并把它放到定时任务中即可。

脚本内容：

```
    #!/usr/bin/sh

    python /path/to/acme_tiny.py --account-key /path/to/account.key --csr /path/to/domain.csr --acme-dir /var/www/challenges/ > /tmp/signed.crt || exit

    wget -O - https://letsencrypt.org/certs/lets-encrypt-x3-cross-signed.pem > intermediate.pem

    cat /tmp/signed.crt intermediate.pem > /path/to/chained.pem

    service nginx reload
```

定时任务可以设置为每个月执行一次：
0 0 1 * * /path/to/renew_cert.sh 2>> /var/log/acme_tiny.log