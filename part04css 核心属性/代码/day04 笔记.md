# 一、复习
1. 表单标签及标签属性
    <form action="跳转目标" target="打开方式"></form>
2. 表单控件及表单控件类型
    <input type="text/password/submit/reset/button" value="默认值">
3. css语法：选择器{属性:值;}
4. css引用方式，4种
    - 内联（行内）样式 style=""
    - 内部样式表 <style> 选择器{属性:值;} </style>
    - 外部样式表-创建 <link rel="stylesheet" href="css路径">
    - 外部样式表-导入 <style>@import url(css路径)</style>
5. 外部样式表创建和导入的区别
    - 本质的区别：link是标签，@import是方式
    - 加载顺序：link同时加载，@import先加载标签后样式
    - 兼容性：link兼容好，@import要IE5以上识别
    - dom控制样式：link可以控制，@import不可以控制
6. css选择器，至少6个
    - 标签 p{}
    - 类 .demo{}
    - ID #demo{}
    - 后代 div p{}
    - 子代 div > p{}
    - 通配符 *{}
    - 伪类 :link{} :visited{} :hover{} :active{}
    - 群组 div, p, .box{}
7. 选择器的权值
    - 通配符    0
    - 标签      1
    - 类       10
    - ID       100
    - 行内       1000
    - !important 10000
8. 姓名

# 二、文本属性
1. font-size 字体的大小
    - 网页中默认字体大小为16px

2. font-family 字体
    - 字体可以取多个值，多个值之间用逗号隔开
    - 中文字体需要加引号
    - 英文字体，多个单词组成一个字体是加引号

3. color 文本颜色
    - 颜色单词：red，green...
    - rgb(red,green,blue) 颜色的取值范围0-255，例如：rgb(97,160,253)
    - rgba(red,green,blue,透明度) 透明度取值0-1
    - #六位十六进制的颜色值  十六进制0-9a-f

4. font-weight 加粗
    - 数值类型：100-900（整百）
        - 100 细体
        - 400 普通文本
        - 700 加粗
        - 900 更粗体
    - 关键词型：
        - lighter 细体
        - normal 普通文本
        - bold 加粗
        - bolder 更粗体

5. font-style 文本倾斜
    - italic 倾斜
    - oblique 倾斜（更具有强制性）
    - normal 普通文本

6. text-align 水平对齐方式
    - left/center/right/justify  左/中/右/两端对齐

7. line-height 行高
    - 如果与高度一致的话，则垂直居中（经常使用）
    - 如果小于高度，文本居上
    - 如果大于高度，文本居下
    - 应用在多行，可以实现行间距
    - 如果没有单位，是行倍数，指当前字号的倍数

8. word-spacing 词间距（单词与单词之间的间距），可正可负

9. letter-spacing 字符间距（汉字和字母都算字符），可正可负

10. text-indent 首行缩进
    - px为单位的数值或者em为单位的数值
    - em为相对单位：相对于父元素字号的大小
    - 可以去负值
    - 只对第一行文本起作用

11. text-decoration 文本修饰线
    - underline 下划线 u
    - line-through 中划线 del/s
    - overline 上划线
    - none 取消修饰线

12. text-transform 检索字符大小写
    - capitalize 单词的首字母大写
    - uppercase 全大写
    - lowercase 全小写
    - none 不转换

13. 复合属性
    - font: bold italic 40px/200px "微软雅黑";
    - font:加粗  倾斜  字号/行高  字体；

# 三、列表属性
1. list-style-type 列表项显示类型
    - decimal 数字
    - disc 实心圆
    - circle 空心圆
    - square 实心方块
    - none 取消

2. list-style-image:url(图片路径)  列表项显示图片

3. list-style-position 列表项显示位置
    - inside 里边
    - outside 外边

4. 复合属性
    - list-style:circle url() inside;
    - 列表样式：类型  图片  位置；
    - list-style:none; 取消列表项的项目符号，常用

# 四、背景属性
1. background-color 背景颜色
    - 颜色单词
    - rgb(red,green,blue) 0-255
    - rgba(red,green,blue,透明度)
    - #六位十六进制的颜色值

2. background-image:url() 背景图片
    - 会产生平铺效果
    - 图片较小能够看到平铺
    - 图片较大看不到平铺
    - 常见的图片格式
        - jpg，有损压缩格式，不支持透明，不支持动画，靠损失图片本身的质量来减小图片的体积
        - png，无损压缩格式，支持透明，不支持动画
        - gif，无损压缩格式，支持透明，支持动画，支持色彩极少

3. background-repeat 背景图片的平铺
    - repeat 默认，平铺
    - no-repeat 取消平铺
    - repeat-x 横向平铺
    - repeat-y 纵向平铺

4. background-position: x y; 背景图片的位置
    - x是水平方向位置
    - y是垂直方向位置
    - 具体的数值
        - 10px 20px
        - x为正时向右走，x为负时向左走
        - y为正时向下走，y为负时向上走
    - 百分比单位的数值
        - 50% 50%
        - （容器宽度-背景图片宽度）*百分比
    - 关键词类型
        - x：left,center,right
        - y：top,center,bottom

5. background-attachment 背景图片的固定和滚动
    - scroll 默认值，滚动
    - fixed 固定，默认在浏览器窗口左上角，以浏览器窗口为参照物

6. background-size 背景图片的尺寸
    - cover 覆盖，等比例缩放到图片铺满盒子，容易出现裁剪效果
    - contain 包含，等比例缩放到撑满某一个方向为止，容易出现留白区域
    - 一个值x，背景图宽度为x，高度等比例缩放
    - 两个值x y，x为背景图的宽度，y为背景图的高度
    - 百分比，背景图片的宽高是模块宽高的百分比

7. 背景复合属性
    - background: url(./images/aixin.png) no-repeat 100px 50px fixed yellow;
    - 背景：图片路径 是否平铺 水平位置 垂直位置 是否固定 背景颜色
    - 注意事项：
        - 复合属性可以取一个值，但是这行代码放在最后会覆盖前面的单一属性
        - 可以跟少量值或者6个值

# 五、边框属性
1. border-width 边框宽度

2. border-style 边框样式
    - solid 单实线
    - double 双实线
    - dashed 虚线
    - dotted 点状线

3. border-color 边框颜色

4. 边框复合属性
    - border:10px solid red;
    - 边框：宽度  样式  颜色;

5. 边框方向
    - border-top 上边框
    - border-left 左边框
    - border-bottom 下边框
    - border-right 右边框

# 作业
1. 整理笔记
2. 敲知识点
3. 作业
    - 01/02/03 必做
    - 04 可选
4. 预习