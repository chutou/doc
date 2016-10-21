# sass制作的grid网格系统



        $grid-columns: 12;
    
    unit: (100%  / grid-columns);
    
    $gutter: 1% !default;
    
    $push: 0 !default;
    
    @mixin column(col, fold:left, push:push, margin:gutter){
    
        background:red;
        margin-bottom: 10px;
        float: #{$fold};
        width:(($unit*$col)-$margin)+($margin/($grid-columns/$col));
        @if $fold == left {
                margin-right: $margin;
                
                        &:last-child {
                                margin-right: 0;
                        }
        }
        @if $fold == right {
                margin-left: $margin;
                         &:last-child {
                         margin-left: 0;
                        }
        }
        }
    
    .column-1{
    
      @include column(1);
    
    }
    
    .column-2{
    
      @include column(2);
    
    }
    
    .column-3{
    
      @include column(3);
    
    }
    
    .column-4{
    
      @include column(4);
    
    }
    
    .column-5{
    
      @include column(5);
    
    }
    
    .column-6{
    
      @include column(6);
    
    }
    
    .column-7{
    
      @include column(7);
    
    }
    
    .column-8{
    
      @include column(8);
    
    }
    
    .column-9{
    
      @include column(9);
    
    }
    
    .column-10{
    
      @include column(10);
    
    }
    
    .column-11{
    
      @include column(11);
    
    }
    
    .column-12{
    
      @include column(12);
    
    }

