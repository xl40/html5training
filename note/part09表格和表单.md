# 一、复习
1. 定位，5种
    - 静态 position:static / 相对 position:relative / 绝对 position:absolute / 固定 position:fixed / 粘性 position:sticky
2. 如何调节层级 z-index
3. 绝对定位和浮动区别
    - 浮动是半脱离文档流，绝对定位是全脱离文档流
4. 模块水平垂直居中显示
    - 子元素设绝对定位，父元素做参照物（相对定位）
    - 设置偏移属性 left:50%; top:50%;
    - margin-top:负的自身高度的一半，margin-left:负的自身宽度的一半
5. 透明3种方法
    - rgba() / opacity:0.5;filter:alpha(opacity=50) / transparent
6. 锚点链接语法
    <a href="#锚点名"></a> <div id="锚点名"></div>
7. 姓名

# 二、表格基本标签
1. 用来显示数据的
    - 数据要放在td里面
    - 想要嵌套的标签也要做td里面

2. table 表格
    - 双标签
    - border="1" 边框
    - width="500" 宽度
    - height="400" 高度
    - align="left/center/right" 水平对齐方式 左/中/右
    - bgcolor="yellow" 背景颜色
    - bordercolor="red" 边框颜色
    - cellspacing="10" 单元格和单元格的间距
    - cellpadding="15" 内容和边框的间距
    - rules="cols/rows" 表格里面的边框线 纵向/横向
    - frame="" 表格外面的边框线
        - above 表格的上边线
        - below 表格的下边线
        - rhs 表格的右边线
        - lhs 表格的左边线
        - box 表格的整个边框线   

3. tr 行
    - bgcolor='red' 本行背景颜色
    - height=‘50’ 本行高度
    - align='left/center/right' 水平对齐方式
    - valign='top/middle/bottom' 垂直对齐方式

4. td 单元格
    - width=‘100’ 单元格的宽度，给一个单元格添加宽度后会影响所在的一整列的宽度
    - height=‘100’ 单元格的高度，给一个单元格添加高度后会影响所在的一整行的高度
    - bgcolor='red' 背景颜色
    - background='./images/1.jpg' 背景图像
    - align='left/center/right' 水平对齐方式
    - valign='top/middle/bottom' 垂直对齐方式
    - rowspan='' 跨行，垂直合并多少个单元格
        - 删除单元格/注释单元格时，需要在其他行进行操作
    - colspan='' 跨列，水平合并多少个单元格
        - 删除单元格/注释单元格时，需要在本行中进行操作

# 三、表格的css属性
1. table
    - border 边框
    - border-spacing 单元格和单元格的间距
    - border- collapse 边框合并
    - table-layout 表格布局算法
        - auto 默认值，自动计算
            - 优点：能够盛放很多内容
            - 缺点：容易把表格撑开，每次页面刷新都需要重新计算宽度
        - fixed 固定宽度
            - 优点：内容不会撑大表格，每次刷新页面不需要重新计算表格宽度
            - 缺点：灵活性差，文本容易溢出
            - 解决：强制换行，word-break:break-all;

2. td
    - border 边框
    - empty-cells 隐藏空内容的单元格
        - show 默认，显示
        - hide 隐藏

# 四、表格其他标签
1. caption 表格标题
    - 位于table里面第一个tr前面
    - css属性
        - caption-side:top/bottom;

2. th 表格标题单元格
    - 默认加粗居中

3. 行分组标签
    - thead 表格头部分组
    - tbody 表格主体分组
    - tfoot 表格底部分组
    - 注意：
        - 如果不带任何分组标签，浏览器会为你创建一个tbody作为盛放数据的主体
            - 编辑器：table>tr>td
            - 浏览器：table>tbody>tr>td
        - 一个表格只有一个头部一个尾部，可以出现多个主体
        - 添加了行分组后，头部和尾部会自动压缩降低高度 

4. colgroup 列分组
    - <colgroup span="数值"></colgroup>
    - 数值：让几列分为一组

# 五、表单
1. 作用：用于收集用户信息

2. form 表单
    - action="跳转地址"
    - method=“提交方式”
    
3. input 表单中的控件
    - 语法：<input type="?">
    - type="text" 单行文本输入框
        - disabled 禁用
        - readonly 只读
        - placeholder="" 提示文本属性
        - value='' 默认值
    - type="password" 密码框
    - type="file" 文件上传，文件域
    - type="hidden" 隐藏域，用来隐藏数据不被用户看到
    - type="radio" 单选框，单选按钮
        - name 属性解决共选，取值需要一致
        - checked 默认选中状态
    - type="checkbox" 复选框，多选框
        - 也有name属性，不是用来解决共选，主要为了分组，获取元素
        - checked 默认选中状态
    - type=‘submit’ 提交按钮，配合form的action属性能实现跳转
    - type=‘reset’ 重置按钮，清空前面输入的数据
    - type=‘button’ 普通按钮，什么功能都没有

4. label 标记标签
    - 提高用户体验，点击文本时让控件选中
    - for属性：指向，与input的id值匹配

5. 下拉菜单
    - select 下拉菜单
        - size=‘数值’ 显示多个
        - multiple 控制选中多个
        - 如果只添加multiple属性的话不添加size则显示4个
    - option 下拉选项
        - value 默认值，方便js获取
        - selected 默认选中状态
    
6. textarea 多行文本输入框，文本域
    - 使用的时候两个标签不要折行显示
    - html标签属性
        - cols 显示的列数
        - rows 显示的行数
    - css属性
        - resize:none 取消宽高的缩放

7. 表单的字段集和字段集标题
    - fieldset 字段集
    - legend 字段集标题

8. value的使用方法和区别
    - 引用在不同的控件中作用不一致
    - 按钮里面：实现按钮上显示的文本
    - 输入框密码框里面：定义字段的初始值
    - 单选框复选框里面：定义与输入相关的值

9. method 表单提交方式
    - get 默认，明提交
        - 能够在地址栏看到密码等数据，安全性比较低，提交数据较少
        - 一般从服务器获取数据时使用
    - post 密文提交
        - 不能看到密码等数据，安全性较高，提交数据较大
        - 一般向服务器提交数据时使用

# 作业
1. 整理笔记
2. 知识点
3. 作业
    - 04 必做
4. 预习