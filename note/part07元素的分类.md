# 一、复习
1. 解决高度塌陷
    - 单元素浮动 后面的元素设置clear:both
    - 多元素浮动 父元素overflow:hidden;zoom:1; / 父元素添加高度 / 父元素后添加块级子元素，给它设置clear:both
2. 盒模型的计算，以水平范围为例
    - 标准盒子 水平范围 = width + 左右padding + 左右border + 左右margin
    - 怪异盒子 水平范围 = width（包含内容、padding、border） + 左右margin
3. 单行文本省略号
    - 设宽 width:
    - 阻止换行 white-space:nowrap;
    - 文本溢出隐藏 overflow:hidden;
    - 显示三个小圆点 text-overflow:ellipsis;
4. 多行文本省略号
    - 设宽和高 width，height（行高*行数）
    - 设置弹性伸缩盒子 display:-webkit-box;
    - 垂直排列子元素 -webkit-box-orient:vertical;
    - 文本显示行数 -webkit-line-clamp
    - 文本溢出隐藏 overflow:hidden;
5. 姓名

# 二、元素的分类
1. 行内元素
    - 默认横向显示，不能设置宽度高度
    - 比如：span,b,strong,em,i,u,s,del,a,sup,sub

2. 块级元素
    - 默认纵向排列，跟父级一样宽，可以设置宽度高度
    - 比如：div,p,h1~h6,ul,ol,li,dl,dt,dd,hr,form

3. 行内块元素（置换元素）
    - 既有行内元素的特点，也有块级元素的特点，既能显示一行，也可以设置宽度和高度
    - 比如：img,input

# 三、元素的转换
1. display 控制元素的显示类型
    - inline 行内元素
    - block 块级元素
    - inline-block 行内块元素
    - none 隐藏元素

2. 如何让一个元素识别宽高
    - display:block/inline-block
    - 添加浮动 float
    - 添加定位 position
    - 让父元素变成弹性盒子 display:flex;

# 四、补充
1. vertical-align 行内块元素的垂直对齐效果，注意跟着文本行高走
    - baseline 默认，基线对齐
    - top 顶线对齐
    - middle 中线对齐
    - bottom 底线对齐

2. 图片与下面块元素产生缝隙：
    - 原因：元素显示类型不一致，图片与基线对齐，基线是英文格子的第三条线
    - 方法：
        - display:block;
        - vertical-align:top;
        - float:left;    

# 作业
1. 整理笔记
2. 知识点
3. 作业
    - 建桥完成
    - 01/02 必做
4. 预习