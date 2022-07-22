# 一、复习
1. 表格标签，至少6个
    <table>
        <caption></caption>
        <colgroup></colgroup>
        <thead>
            <tr><th></th></tr>
        </thead>
        <tbody>
            <tr><td></td></td>
        </tbody>
        <tfoot></tfoot>
    <table>
2. 表格的标签属性，至少5个
    <table border='' width='' height='' align='left/center/right' bgcolor='' bordercolor='' cellspacing='' cellpadding='' rules='cols/rows' frame='above/below/lhs/rhs/box'></table>
3. 单元格的标签属性，至少6个
    <td width='' height='' align='left/center/right' valign='top/middle/bottom' bgcolor='' background='' rowspan='' colspan=''></td>
4. 表格的css属性
    边框间距 border-spacing
    边框合并 border-collapse
    表格布局 table-layout
    强制换行 word-break:break-all
    标题位置 caption-side
5. 表单控件类型，至少6个
    <input type="text/password/file/radio/checkbox/hidden/submit/reset/button" disabled readonly value='' placeholder='' checked>
6. 表单其他标签
    下拉菜单 <select><option value=''></option></select>
    多行文本 <textarea cols='' rows=''></textarea>
    标记标签 <label for=''><label>
7. 表单提交方式及区别
    - get 明提交，地址栏可看到数据，安全性较低，提交数据较少，一般获取数据时使用
    - post 密文提交，地址栏不可看到数据，安全性比较高，提交数据较大，一般提交数据时使用
8. 姓名

# 二、宽高自适应
1. 宽度自适应
    - 块级元素不设宽度，自适应，默认占父元素宽度的100%
    - 应用：通栏布局

2. 高度自适应
    - 块级元素不设置高度，自适应，被子元素撑开
    - 设置高度，高度太小
        - 内容过多会产生溢出效果，把后面的布局覆盖
    - 不设置高度
        - 若内容特别少，布局不美观
        - 所有用最小高度 min-height
    - 另外：
        - 最大高度 max-height
        - 最小宽度 min-width
        - 最大宽度 max-width

# 三、隐藏元素的方法
1. rgba()
    - 背景透明，元素占空间
2. opacity 
    - 所有内容透明，元素占空间
3. visibility: hidden;
    - 元素不可见，元素占空间
4. transform: scale(0);
    - 缩放为0，元素占空间
5. display:none;
    - 隐藏元素，元素不占空间，后面元素补位
6. width:0; height:0;
    - 隐藏元素，元素不占空间，后面元素补位，若溢出则可以overflow:hidden;

# 四、伪元素选择器
1. 在父元素的里面末尾位置添加一个内容
    - ::after{content:'';}
2. 在父元素的里面开始位置添加一个内容
    - ::before{content:url();}
3. 首字符
    - ::first-letter
4. 首行
    - ::first-line

# 五、解决高度塌陷
1. 单元素浮动
    - 后面元素清除浮动，clear:both;
2. 多元素浮动
    - 给父级添加高度
    - 父元素后面添加块级子元素，给这个子元素设置clear:both
    - 父元素设置overflow:hidden;zoom:1;
3. 万能清除法
    父元素::after{
        content: '';
        display: block;
        width: 0;
        height: 0;
        visibility: hidden;
        clear: both;
    }

# 六、窗口自适应
1. 应用：移动端布局
2. 方法：
    html,body{
        width: 100%;
        height: 100%;
    }

# 七、浮动框架集
1. 语法：
    <iframe src="页面的路径" frameborder="0" width="" height=""></iframe>

# 八、布局
1. 布局方式
    - 两栏布局
    - 三栏布局
    - 上下结构-下两栏
    - 上中下结构-中三栏

2. calc函数
    - 作用：动态计算长度值
    - 语法：calc(100% - ？px)
    - 注意：运算符前后要有空格
    - 支持：+ - * /
    - 规则：数学运算优先级规则

# 九、BFC 块级格式化上下文
    - 形成BFC的条件
        - 浮动元素 float除none以外的值
        - 绝对定位元素，position(absolute，fixed)
        - display为inline-block，flex，inline-flex
        - overflow除了visible以外的值（hidden，auto，scroll）
    - BFC的特点
        - 内部的box会在垂直方向，一个接一个放置（针对块元素）
        - box垂直方向的距离由margin决定，属于同一个BFC的两个相邻box的margin会发生重叠（外边距上下取最大值）
        - 每个box的margin的左边，与包含border box的左边接触（从左到右的格式化），即使存在浮动也是一样
        - BFC的区域不会与float box重叠
        - BFC是页面中一个独立的容器，容器里面的子元素不会影响外面的元素
        - 计算BFC的高度时，浮动元素也参与计算

# 作业
1. 整理笔记
2. 知识点
3. 作业
    - 01/02/03/04 任选一套
4. 预习