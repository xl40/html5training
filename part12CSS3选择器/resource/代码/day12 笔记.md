# 一、复习
1. 语义化标签，至少7个
    header / footer / section / nav/ main / aside / article / figure / figcaption / hgroup
2. 音频标签和属性
    <audio src="" controls loop autoplay muted></audio>
3. 视频标签和属性
    <video src="" controls loop autoplay muted poster=""></video>
4. 表单类型，至少8个
    <input type="color/range/number/tel/email/url/search/date/week/month/time/datetime-local" value="" min="" max="" step="">
5. 表单新增属性
    required / autofocus / multiple / pattern
    <input type="text" list="">
    <datalist id=""><option value=""></option></datalist>
6. 轮廓、轮廓偏离距离、清除默认样式
    outline / outline-offset / appearance:none
7. 浏览器
    - 谷歌 chrome内核，之前是webkit，现在blink
    - 火狐 firefox内核，gecko内核
    - IE IE内核，Trident内核
    - 欧朋 presto内核，后来webkit，现在blink
    - 苹果 webkit内核
7. 姓名

# 二、css3选择器
1. 关系选择器（层级选择器）
    - 后代选择器
        - 符号（空格）
    - 子代选择器
        - 符号（>）
    - 匹配当前元素的后面一个兄弟（紧紧挨着的兄弟）
        - 符号（+）
    - 匹配当前元素后面所有的兄弟
        - 符号（~）

2. 属性选择器
    - [属性]
        - 匹配页面中的带有对应属性的元素
    - [属性="值"]
        - 匹配页面中的带有对应属性，并且有对应属性值的元素
    - E[属性]
        - 匹配页面中某一类元素中带有对应属性的元素
    - E[属性=“值”]
        - 匹配页面中的某一类元素中带有对应属性并且有属性值的元素
    - [属性^=“值”]
        - 匹配属性值以这个值开头的元素
    - [属性$=“值”]
        - 匹配属性值以这个值结尾的元素
    - [属性*=“值”]
        - 匹配属性值包含这个值的元素，可以是词或字母
    - [属性~=“值”]
        - 匹配属性值包含这个值的元素，必须是完整的词
    - [属性|=“值”]
        - 匹配属性值等于这个值的元素，必须仅有这个完整的词

3. 结构伪类选择器
    - 子元素
        - 常用于父元素下只有一种子元素
        - :first-child
            - 获取子元素中的第一个
        - :last-child
            - 获取子元素中的最后一个
        - :nth-child(参数)
            - 获取子元素中的第？个
            - 参数取值：
                - 具体的数值：表示匹配第几个，比如1，2，3....
                - 表达式，比如3n，4n+1...
                - 关键词，even偶数，相当于2n，odd奇数相当于2n+1
        - :nth-last-child(参数)
            - 获取子元素中倒数第？个
            - 参数取值同上
        - :only-child
            - 匹配有且仅有一个子元素的
    - 类型
        - 常用于父元素下有多种子元素
        - :first-of-type
            - 获取某类型元素中的第一个
        - :last-of-type
            - 获取某类型元素中的最后一个
        - :nth-of-type(参数)
            - 获取某类型元素中的第？个
            - 参数取值：
                - 具体的数值：表示匹配第几个，比如1，2，3....
                - 表达式，比如3n，4n+1...
                - 关键词，even偶数，相当于2n，odd奇数相当于2n+1
        - :nth-last-of-type(参数)
            - 获取某类型元素中的倒数第？个
            - 参数取值同上
        - :only-of-type
            - 匹配有且仅有一个某类型元素

4. 否定伪类
    - :not(选择器) 排除掉的意思，排除某一个/某一类元素

5. 根目录伪类
    - :root 匹配根目录，一个页面有且仅有一个根目录html
    - 等同于html{}

6. 空伪类
    - :empty 匹配的是页面元素中没有任何内容的空元素

7. 目标伪类
    - :target 需要配合锚点效果进行实现，点击哪个锚点实现对应目标高亮

8. UI状态伪类
    - :enabled 匹配可用元素
    - :disabled 匹配不可用元素
    - :checked 设置选中时候的样式，在单/复选框中应用
    - :focus 元素获得焦点时的样式
    - ::selection 选中文本时的样式

# 三、浏览器的属性前缀
1. 解决部分属性在不同浏览器里面不兼容，不能实现的问题

2. 方法
    - -ms- 针对IE浏览器里面的属性前缀
    - -o- 针对opera浏览器里面的属性前缀
    - -moz- 针对firefox浏览器里面的属性前缀
    - -webkit- 针对chrome和safari浏览器里面的属性前缀

# 四、css3属性
1. text-shadow 文本阴影
    - text-shadow: h-shadow  v-shadow  blur  color
    - h-shadow 水平方向阴影的偏离位置，正值右偏，负值左偏
    - v-shadow 垂直方向阴影的偏离位置，正值下偏，负值上偏
    - blur 模糊距离
    - color 阴影颜色，默认黑色
    - 不同方向的阴影用逗号隔开，取值谁在前谁的阴影在上层

2. box-shadow 盒子阴影
    - box-shadow:h-shadow v-shadow blur spread color inset
    - h-shadow 水平方向阴影的偏离位置，正值右偏，负值左偏
    - v-shadow 垂直方向阴影的偏离位置，正值下偏，负值上偏
    - blur 模糊距离
    - spread 阴影大小（px），可选
    - color 阴影颜色，默认黑色
    - inset 设置内阴影，可选
    - 可以添加多个方向的阴影，每一组方向用逗号隔开

3. 自定义字体
    - 引入web自定义字体
        @font-face{
            font-family:自定义名字;
            src:url(字体路径);
        }

4. 字体图标
    - 阿里巴巴矢量图库 https://www.iconfont.cn/
    - 如何下载
        - 先登陆，添加购物车，去购物车点击“下载代码”
    - 如何使用
        - 引入css文件（一般iconfont.css），利用别人写好的样式执行字体图标
        - 图标名打开html文件查看
    - 遵循字体的所有属性

5. background 多背景属性
    - 取值：url(图片1) no-repeat 10px 10px, url(图片2) repeat;
    - 哪一个图片插入的位置在前面，谁的层级就比较高

6. border-radius 圆角属性
    - 取值
        - 一个值：四个角都圆化
        - 两个值：左上 右下 ，右上 左下
        - 三个值：左上 ，右上 左下 ，右下
        - 四个值：左上 ，右上 ，右下 ，左下
    - 倒角，四个角一致
        - border-radius:x/y
        - x 所有角的水平半径
        - y 所有角的垂直半径
    - 倒角，四个角不一致
        - border-radius:x1 x2 x3 x4/y1 y2 y3 y4
        - /前代表每一个角的水平半径
        - /后代表每一个角的垂直半径
    - 正方形
        - 取值为宽度高度的一半时，会出现正圆
        - 取值为50%时会出现正圆
    - 长方形
        - 取值为较小边的一半的时候，会出现操场效果
        - 取值为50%时会出现椭圆
    
# 作业
1. 整理笔记
2. 敲知识点
3. 作业
    - 01/02/03/04
4. 预习