# 一、复习
1. 高度塌陷
    - 单元素浮动，后面元素添加clear:both
    - 多元素浮动，父元素添加overflow:hidden;zoom:1 / 父元素添加高度 / 父元素后面添加块级子元素，这个子元素设置clear:both;
2. 盒模型的组成 外边距，内边距，内容，边框
3. 盒模型的计算
    - W3C官方盒子 宽度范围 = width+左右padding+左右border+左右margin
    - IE怪异盒子 宽度范围 = width+左右margin
4. 标准盒子和怪异盒子的转换 box-sizing:content-box/border-box
5. 外边距的特殊情况
    - 兄弟上下 取最大值
    - 兄弟左右 相加
    - 父子包含 子元素设置上外边距会作用到父元素上
        - 父元素设置上内边距 / 父或子元素设置浮动 / overflow:hidden; / 父元素设透明边框
6. 姓名

# 二、文本溢出
1. overflow 解决溢出效果
    - visible 默认值，溢出显示
    - hidden 溢出隐藏（裁剪的效果）
    - scroll 溢出滚动，带有横纵两个滚动条，如果文本没有溢出，也有滚动条，不过没有作用
    - auto 自动，当文本溢出显示纵向滚动条，没有溢出不显示滚动条

# 三、剩余空间
1. white-space 处理元素内的空白
    - normal 默认值
    - nowrap 文本不换行，横向显示，常用
    - pre 文本不换行，前面显示空格，上下显示换行
    - pre-wrap 文本换行，前面显示空格，上下显示换行
    - pre-line 文本换行，前面不显示空格，上显示换行，下不显示换行

2. 预定义标签
    - ‘’<pre></pre>‘’
    - 能识别空格，换行等格式

# 四、省略号
1. text-overflow 文本溢出处理
    - clip 裁剪
    - ellipsis 显示三个圆点
    
2. 单行文本省略号
    - 设置宽度 width
    - 文本不换行 white-space: nowrap;
    - 文本溢出隐藏 overflow: hidden;
    - 文本后显示三个小圆点 text-overflow: ellipsis;

3. 多行文本省略号
    - 设置宽和高 width，height（行高*行数）
    - 设置弹性伸缩盒子 display: -webkit-box;
    - 垂直排列子元素 -webkit-box-orient: vertical;
    - 文本显示行数 -webkit-line-clamp: 3;
    - 文本溢出隐藏 overflow: hidden;

