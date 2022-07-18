# 一、复习
1. 文本属性及复合写法，至少10个
    - font-family, font-size, color, font-weight:100-900/bold/bolder/lighter/normal, font-style:italic/oblique/normal, text-align:left/center/right/justify, line-height, word-spacing, letter-spacing, text-indent, text-decoration:underline/line-through/overline/none, text-transform:uppercase/lowercase/capitalize/none
    - font:加粗 倾斜 字号/行高 字体
2. 列表复合属性
    - list-style-type:decimal/disc/circle/square/none, list-style-image, list-style-position
    - list-style: 类型 图片 位置;
3. 背景属性及复合写法，至少6个
    - background-color, background-image, background-repeat:no-repeat/repeat/repeat-x/repeat-y, background-position:x y; background-size:cover/contain/w h; background-attachment:scroll/fixed
    - background: 图片 平铺 水平位置 垂直位置 固定 颜色
4. 边框复合属性
    - border-width, border-style:solid/dashed/dotted/double, border-color, border-方向
    - border: 宽度 样式 颜色
5. 姓名

# 二、浮动
1. 应用：让竖着排列的元素横向显示，用于布局元素

2. 取值 float
    - none 默认，不浮动
    - left 左浮动
    - right 右浮动

3. 特点：
    - 前面元素添加浮动，后面元素会上去补位
    - 若父级够宽，所有子元素浮动，会一排显示
    - 若父级不够宽，所有子元素浮动，会折行显示

4. 高度塌陷
    - 单元素浮动
        - 后面元素清除浮动 clear:left/right/both/none  清除左/清除右/全清除/不清除
    - 多元素浮动
        - 给父级添加高度
        - 父元素后面添加一个块级子元素，给这个子元素设置clear:both
        - 父元素设置overflow:hidden;zoom:1;(最常用)

5. 建议：
    - 每个子元素设宽度
    - 每个子元素设浮动
    - 父元素设overflow:hidden; zoom:1;

# 三、盒模型
1. 盒模型的组成
    - 内容部分：设置的宽度和高度（width，height）
    - 内边距：内容与边框的间距（padding）
    - 边框：盒子边缘（border）
    - 外边距：边框与边框的间距（margin）

2. padding 内边距
    - 内容和边框之间的距离
    - 背景颜色能够蔓延到内边距上面
    - padding:0; 取消自带的内边距
    - 能够取正值，能取0，不能取负值，没有意义
    - 方向取值
        - padding-方向  left/top/right/bottom
    - 取值
        - 1个值：上 右 下 左
        - 2个值：上下 ，左右
        - 3个值：上 ，左右 ，下
        - 4个值：上 ，右 ，下 ，左

3. margin 外边距
    - 边框和边框之间的距离
    - 背景颜色不回蔓延到外边距上面
    - margin:0; 取消自带的外边距
    - 能够取正值，能取0，可以取负值，能够移动盒子的位置
    - 方向取值
        - margin-方向  left/top/right/bottom
    - 取值
        - 1个值：上 右 下 左
        - 2个值：上下 ，左右
        - 3个值：上 ，左右 ，下
        - 4个值：上 ，右 ，下 ，左

4. 边距清零（重置）
    - *{ margin: 0; padding: 0;}
    - h1, h2, h3, h4, h5, h6, p, body, ul, ol, li, dl, dt, dd, form{ margin: 0;padding: 0;}

5. 盒模型的计算
    - 组成部分：
        - 四部分组成：内容width/height，内边距padding，边框border，外边距margin
    - # 计算方式
        
        - W3C官方盒模型（标准盒模型）
            - 实际的宽度 = width+左右padding+左右border+左右margin
            - 实际的高度 = height+上下padding+上下border+上下margin
        - IE怪异盒模型
            - 实际的宽度 = width（包括内容、边框和内边距）+左右margin
            - 实际的高度 = height（包括内容、边框和内边距）+上下margin
    - box-sizing 盒模型转成怪异盒模型
        - content-box（内容盒子，W3C官方盒子），默认
        - border-box（边框盒子，IE怪异盒子）
    
6. 外边距的特殊情况
    - 兄弟上下
        - 竖着排列的两个盒子，上面的盒子设置下外边距，下面的盒子设置上外边距
        - 外边距取最大值
    - 兄弟左右
        - 横着排列的两个盒子，左侧的盒子设置右外边距，右侧的盒子设置左外边距
        - 外边距取值是相加的
    - 父子包含
        - 给子元素添加上外边距的时候会作用到父元素上
        - 解决方法
            - 给父元hidden; BFC，块级格式化上下文
    
7. 外边距均分
    - 让该元素在父元素内水平居中
    - margin:0 auto; 0代表上下边距为0，auto左右边距均分

# 四、ps的使用
1. 图片处理软件
2. 作用：测量，吸色，切图
3. 打开
    - 图片右键，选择打开方式，选择ps
    - 把图片拖拽到ps图标上面
    - ps菜单栏，选择“文件”---“打开”
4. 图片的缩放
    - ctrl + "+"
    - ctrl + "-"
    - alt + 滚轮
5. 拖动画布
    - 空格变小手，拖动即可
6. 吸取颜色
    - 工具栏 - 前景色/背景色，出现弹框，画面中吸颜色，弹框内会有十六进制的色值
    - 工具栏 - 吸管，在颜色上右击，拷贝十六进制色值
7. 测量图片大小
    - 工具栏 - 矩形选框工具，快捷键M
    - 查看数据（窗口 - 信息面板 - w宽 h高）
    - 修改测量单位：标尺上右击，选择像素
    - 取消选区框：ctrl + d
8. 参考线
    - 作用：方便测量
    - 调出标尺：ctrl + r
    - 从标尺中往画布拖拽参考线
    - 删除参考线：
        - 工具栏 -- 移动工具，快捷键V，把参考线拖到标尺上
        - 菜单栏“视图” -- “清除参考线”
    - 隐藏/显示参考线
        - ctrl+“;”
9. 切图
    - 方法一：使用快捷键
        - 每次只能截取一个
        - 选框工具选好区域：ctrl+C 复制，ctrl+N 新建，回车 确认，ctrl+V 粘贴，ctrl+S 保存（格式、命名、保存位置）， ctrl+W 关闭
    - 方法二：切片工具
        - 可以批量切图
        - 工具栏 -- 切片工具，快捷键C
        - 切好需要的图片，菜单栏选择“文件”---“导出”---“存储为web所用格式”，按住shift选择多个切片，右上角选择图片类型，下方点击存储，选择存储位置，选择仅限图像，选择选中的切片，修改名字，点击保存
        - 复制切片：alt+shift 水平/垂直平移复制
        - 删除切片：切片左上角右击---删除切片
        - 修改切片：ctrl点击切片左上角，可以修改尺寸

# 作业
1. 整理笔记
2. 敲知识点
3. 周五作业
    - 01/02 必做
    - 03/04 可选
4. 周六作业
    - 05
5. 预习
