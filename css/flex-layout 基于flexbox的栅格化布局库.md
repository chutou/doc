# flex-layout 基于flexbox的栅格化布局库





flex-layout
flex-layout是一个基于css3 flexbox的栅格化布局库，提供更直观、丰富的布局方式，可以轻松解决垂直居中，多栏同高等问题。

项目地址：     https://github.com/coffcer/flex-layout文档与demo：http://coffcer.github.io/flex-layout

为什么使用？
与传统的栅格化相比，flex-layout解决了css布局的不少问题:
[list][*]应用一个class就可以垂直居中。
[*]轻松实现多栏同高。
[*]自动计算间距，实现等宽布局，不需要再计算margin。
[*]支持自动填充剩余宽度，以往我们需要通过触发BFC来实现。
[*]支持自动填充剩余高度，比如将footer置于底部。
[*]随意调整[栅格]顺序，比如让main比sidebar提前渲染出来。
[*]丰富的对齐方式：上、下、左、右、左上、右上、左下、右下。
[/list]
概述
与传统的栅格化一样，flex-layout基于容器(相当于Bootstrap的row) 和栅格(相当于Bootstrap的column) 来布局:
[list][*][容器]有两种：
flex-column: 容器里的[栅格]以横向排列，与传统栅格化的row一样
flex-row: 容器里的[栅格]以竖向排列，就像header、content、footer的排列一样
[*]通常，只有[栅格]可以直接放在[容器]中，而你的内容应该放在[栅格]里。但这不是必须的，直接把内容放在[容器]里也没问题。
[*]如果一个[容器]里包含的[栅格]超过24格，多出的部分将另起一行。
[*]Flexbox有主轴，副轴的概念，flex-layout已经封装好了，你不需要懂得flexbox，也无需针对不同轴使用不同的class。不过，如果你对Flexbox有所了解的话，用起来会更顺手。
[*]与Bootstrap等栅格化不同的是：flex-layout不需要container，栅格本身不自带padding。
具体看文档 http://coffcer.github.io/flex-layout
[/list]

~~~
@flex-column: 24;

.flex-clearfix() {
	&:before, &:after {
		content: " ";
		display: flex;
		box-sizing: border-box;
		width: 0;
		height: 0;
		font-size: 0;
	}
	&:after {
		clear: both;
	}
}

.flex-column, .flex-row {
	display: flex;
	flex-wrap: wrap;
	.flex-clearfix();
}
.flex-column {
	flex-direction: row;
}
.flex-row {
	flex-direction: column;
}
.flex-around {
	justify-content: space-around;
}
.flex-between {
	justify-content: space-between;
}
.flex-baseline {
	align-items: baseline;
}
.flex-strech {
	align-items: stretch;
}

.flex-item {
	float: left;
	flex-grow: 1;
}

// 递归生成栅格
.build-item(@i) when (@i > 0) {
	.build-item((@i - 1));
	
	// 栅格
	.flex-item-@{i} {
		float: left;
		width: percentage(@i / @flex-column);
	}
	
	// 向左偏移
	.flex-offset-@{i} {
		margin-left: percentage(@i / @flex-column);
	}
	
	// 排序
	.flex-order-@{i} {
		order: @i;
	}
}

.build-item(@flex-column);

// flex-row的对齐方式
.build-align(@type) when (@type = row) {
	&.flex-left {
		align-items: flex-start;
	}
	&.flex-right {
		align-items: flex-end;
	}
	&.flex-top {
		justify-content: flex-start;
	}
	&.flex-bottom {
		justify-content: flex-end;
	}
	&.flex-center {
		align-items: center;
	}
	&.flex-middle {
		justify-content: center;
	}
}
// flex-column的对齐方式
.build-align(@type) when (@type = column) {
	&.flex-left {
		justify-content: flex-start;
	}
	&.flex-right {
		justify-content: flex-end;
	}
	&.flex-top {
		align-items: flex-start;
	}
	&.flex-bottom {
		align-items: flex-end;
	}
	&.flex-center {
		justify-content: center;
	}
	&.flex-middle {
		align-items: center;
	}
}

.flex-column {
	.build-align(column);
}
.flex-row {
	.build-align(row);
}

[class*=flex-item] {
	&.flex-left {
		margin-right: auto;
	}
	&.flex-right {
		margin-left: auto;
	}
	&.flex-top {
		margin-bottom: auto;
	}
	&.flex-bottom {
		margin-top: auto;
	}
	&.flex-center {
		margin-left: auto;
		margin-right: auto;
	}
	&.flex-middle {
		margin-top: auto;
		margin-bottom: auto;
	}
}

.flex-sm-show, .flex-md-show {
	display: none;
}

@media (max-width: 992px) {
	.flex-md {
		flex-direction: column;
		.build-align(row);
		
		[class*=flex-item] {
			width: 100%;
		}
	}
	.flex-md-hide {
		display: none !important;
	}
	.flex-md-show {
		display: flex !important;
	}
}

@media (max-width: 768px) {
	.flex-sm {
		flex-direction: column;
		.build-align(row);

		[class*=flex-item] {
			width: 100%;
		}
	}
	.flex-sm-hide {
		display: none !important;
	}
	.flex-sm-show {
		display: flex !important;
	}
}
~~~






