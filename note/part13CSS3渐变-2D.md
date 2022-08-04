# 一、复习
1. CSS3选择器
    - 关系 .box > p{} / .box p{} / .box + p{} / .box ~ p{}
    - 属性 [] ^= $= *=  ~=  |=
    - 结构伪类 
        - 子元素 :first-child / :last-child / :nth-child() / :nth-last-child() / :only-child
        - 类型 :first-of-type / :last-of-type  / :nth-of-type () / :nth-last-of-type () / :only-of-type 
    - 否定伪类 :not()
    - 根目录伪类 :root
    - 空伪类 :empty
    - 目标伪类 :target
    - UI状态伪类 :enabled / :disabled / :focus / :checked / ::selection
2. 浏览器的属性前缀
    - -ms- IE / -webkit- 谷歌/苹果 / -o- 欧朋 / -moz- 火狐
3. CSS3属性
    - 文本阴影 text-shadow:水平偏离 垂直偏离 模糊范围 颜色
    - 盒子阴影 box-shadow：水平偏离 垂直偏离 模糊范围 大小 颜色 内阴影
    - 自定义字体 @font-face{font-family:; src:url();}
    - 多背景属性 background:url() no-repeat 0 0,url()
    - 圆角 border-radius
4. 姓名

# 二、渐变
1. 线性渐变
    - 语法：background-image: linear-gradient(deg,col1,col2,col3);
        - deg 方向
            - 到达某一边
                - to bottom 默认，到达下边，从上边开始到下边结束
                - to top 到达上边，从下边开始到上边结束
                - to right 到达右边，从左边开始到右边结束
                - to left 到达左边，从右边开始到左边结束
            - 到达某个角
                - to top right 到达右上角，从左下开始
                - to top left 到达左上角，从右下开始
                - to bottom right 到达右下角，从左上开始
                - to bottom left 到达左下角，从右上开始
            - 角度
                - 单位deg，比如30deg
        - col1,col2,col3 颜色
            - col1 开始颜色
            - col3 结束颜色
            - 加百分比：指这个颜色显示的位置，比如col2 50%
    - 文字渐变
        background-image: linear-gradient(to bottom,red,green);
        -webkit-text-fill-color: transparent;
        -webkit-background-clip: text;

2. 径向渐变：
    - background-image: radial-gradient(center,shape,size,col1,col2,col3);
        - center 渐变中心
            - 渐变中心需要添加浏览器属性前缀 -webkit-radial-gradient
            - x y
        - shape 渐变的形状
            - 形状不可以跟渐变大小同时使用
            - ellipse 默认，椭圆
            - circle 圆形
        - size 渐变的大小
            - 形状不可以跟渐变大小同时使用
            - closest-corner 半径为从圆心到最近角
            - closest-side 半径为从圆心到最近边
            - farthest-corner 半径为从圆心到最远角
            - farthest-side 半径为从圆心到最远边
        - col1,col2,col3 颜色
            - col1 开始颜色
            - col3 结束颜色
            - 加百分比：指这个颜色显示的位置，比如col2 50%

3. 重复渐变
    - background: repeating-linear-gradient(red 30%,yellow 40%,green 50%);
        - 渐变规律：red在30%开始位置，yellow在40%的位置，green在50%结束位置，按此规律依次渐变
    - background: repeating-radial-gradient(red,yellow 20%,green 30%);

4. 背景图片的定位区域
    - background-origin
        - border-box 从边框开始平铺
        - padding-box 从内边距开始平铺
        - content-box 从内容区开始平铺

5. 背景图像的裁剪
    - background-clip
        - border-box 裁剪边框以外的背景图片
        - padding-box 裁剪内边距以外的背景图片
        - content-box 裁剪内容区以外的背景图片

# 三、过渡属性
1. 由一种状态向另外一种状态缓慢变化，需配合鼠标经过才可执行

2. 效果图
    - 如果放在:hover里面，只有经过的时候过渡
    - 如果放在未经过的选择器内，则经过和离开都过渡

3. 语法
    - transition-property 过渡的css属性
        - 单一属性，多个值空格隔开
        - all 所有的css属性
    - transition-duration 过渡所需要的时间
        - 必须有单位s
    - transition-timing-function 过渡的时间曲线
        - linear 匀速
        - ease 逐渐慢下来
        - ease-in 加速
        - ease-out 减速
        - ease-in-out 先加速后减速
        - steps(数值) 执行几步
        - cubic-bezier() 贝塞尔曲线
    - transition-delay 过渡延迟时间
        - 必须有单位s
    - transition: all 2s linear 0s;
        - 过渡复合属性：过渡的css属性 所需时间 时间曲线 延迟时间

# 四、2D
1. 2D指的是平面，平面效果就是二维空间里面的元素旋转、平移、缩放、倾斜

2. 2d属性：transform

3. 旋转
    - transform:rotate()
    - rotateX() 绕x轴旋转
    - rotateY() 绕Y轴旋转
    - rotate() 绕元素正中心旋转

4. 改变旋转中心（原点）
    - transform-origin:x y;
    - x 水平坐标位置
    - y 垂直坐标位置
    - 可以关键词：left top;
    - 可以正值：20px 50px;
    - 可以负值：-50px -50px;

5. 位移
    - transform:translate()
    - translateX() 水平方向位移
    - translateY() 垂直方向位移
    - translate(x,y)
        - x 水平方向位移
        - y 垂直方向位移
    - translate(x) 水平方向位移

6. 缩放
    - transform:scale(数值)
    - scaleX() 沿着水平方向缩小放大倍数
    - scaleY() 沿着垂直方向缩小放大倍数
    - scale(x,y) 
        - x 水平缩小放大x倍
        - y 垂直缩小放大y倍
    - scale(val) 水平垂直都放大缩小val倍
    - ()里面的取值
        - 等于1，不缩小不放大
        - 大于1，放大
        - 小于1，缩小
        - 等于0，隐藏
        - 取值可以为负值，-号代表倒像
            - 负号后面取值等于1，不缩小不放大的倒像
            - 负号后面取值小于1，缩小的倒像
            - 负号后面取值大于1，放大的倒像

7. 倾斜
    - transform:skew(度数)
    - skewX() 水平倾斜，与y形成一个夹角
    - skewY() 垂直倾斜，与x形成一个夹角
    - skew(x,y)
        - x 水平倾斜
        - y 垂直倾斜
    - skew(x) 只有水平倾斜

8. 变形多属性
    - transform: translate(200px) rotate(90deg);
        - 先平移后选中
    - transform: rotate(90deg) translate(200px);
        - 先旋转后平移

# 作业
1. 整理笔记
2. 敲知识点
3. 作业
    - 01 / 02 必做
4. 预习