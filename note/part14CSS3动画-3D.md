# 一、复习
1. 渐变，线性/径向/重复
    background-image:linear-gradient(deg,col1 20%,col2,col3...)
    background-image:radial-gradient(center,shape,size,col1,col2,col3...)
    background-image:repeating-radial-gradient(col1 20%,col2 30%,col3 40%)
2. 背景图片的定位区域和裁剪
    background-origin:border-box/padding-box/content-box
    background-clip:border-box/padding-box/content-box
3. 过渡属性及复合写法
    transition-property / transition-duration / transition-timing-function / transition-delay
    transition: css属性 所需时间 时间曲线 延迟时间
4. 2D，旋转/平移/缩放/倾斜
    transform:rotate(角度)/rotateX()/rotateY()
            translate(像素值)/translateX()/translateY()/translate(x,y)
            scale(数值)/scaleX()/scaleY()/scale(x,y)
            skew(角度)/skewX()/skewY()/skew(x,y)/
5. 改变原点 transform-origin:x y
6. 姓名

# 二、动画
1. 声明动画
    - 方法一：
        @keyframes 动画名{
            from{ 起始状态 }
            to{ 结束状态 }
        }
    - 方法二：
        @keyframes 动画名{
            0%{ 起始状态 }
            30%{}
            60%{}
            100%{ 结束状态 }
        }

2. 动画属性
    - animation-name 声明动画的名字
    - animation-duration 动画播放一次所需时间
        - 必须有单位s
    - animation-timing-function 动画播放时间曲线
        - linear 匀速
        - ease 逐渐慢下来
        - ease-in 加速
        - ease-out 减速
        - ease-in-out 先加速后减速
        - steps(数值) 每一帧动画执行几步
            - step-start 开始值不保持
            - step-end 结束值不保持
        - cubic-bezier() 贝塞尔曲线
    - animation-delay 动画延迟时间
        - 必须有单位s
    - animation-iteration-count 动画播放次数
        - 数字，是几就是几次
        - infinite 无限次
    - animation-direction 动画执行方向
        - normal 正常方向
        - reverse 反方向
        - alternate 先正向再反向，交替反复执行
        - alternate-reverse 先反向再正向，交替反复执行
    - animation-fill-mode 动画时间外的属性
        - backwards 等待时执行第一帧
        - forwards 结束时执行最后一帧
        - both 等待时执行第一帧，结束时执行最后一帧
    - animation-play-state 动画播放状态
        - running 默认，播放
        - paused 暂停
    - 动画复合属性
        - 动画：名字 播放时间 时间曲线 延迟时间 播放次数 播放方向 时间外的属性；

3. 过渡和动画的区别
    - transition，animation
    - 过渡需要配合鼠标经过，动画不需要
    - 过渡是从状态1-状态2
    - 动画是从状态1-状态2-状态3...

# 三、3D
1. transform-style:preserve-3d 父元素添加，出发3D舞台

2. transform:rotate() 旋转
    - rotateX() 绕x轴旋转
    - rotateY() 绕y轴旋转
    - rotateZ() 绕z轴旋转
    - rotate3d(x,y,z,deg) 前三个分别为是否绕x，y，z旋转，1为是，0为否，deg为角度

3. transform:translate() 位移
    - translateX() 水平方向位移
    - translateY() 垂直方向位移
    - translateZ() z轴上面前后位移

4. perspective 景深，透视，值越大，距离越远
    - 若位移加了景深，负值远，变小，正值近，放大

# 作业
1. 整理笔记
2. 敲知识点
3. 作业
    - 01/02/03
4. 预习