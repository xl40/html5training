# 一、复习
1. 容器属性
    - 主轴方向 flex-direction:row/column/row-reverse/column-reverse / 横轴对齐方式 justify-content:flex-start/flex-end/center/space-between/space-around/space-evenly / 纵轴对齐方式 align-items:flex-start/flex-end/center/stretch  / 换行 flex-wrap:nowrap/wrap / 行间距 align-content:flex-start/flex-end/center/space-between/space-around/space-evenly
2. 项目属性
    - 纵轴对齐方式 align-self:flex-start/flex-end/center/stretch / 顺序 order / 剩余宽高度 flex:1; / 是否挤压 flex-shrink:1/0;
3. 滚动条隐藏
    ::-webkit-scrollbar{ display:none;}
4. 多列布局
    - 列数 column-count / 列宽 column-width / 列间距 column-gap / 列间隔线 column-rule / 列高度 column-fill / 跨列 column-span
5. 不折列 break-inside:avoid
6. 姓名

# 二、了解移动端
1. 什么是移动端
    - 可以移动的设备被称之为移动端，手机、平板、手表，都可以称之为移动端
2. 查看移动端页面
    - 设备模拟器，切换不同的手机屏幕型号，观看对应的页面效果
    - 右键--检查--找到设备模拟器切换窗口进行切换
3. 设备模拟器内容介绍
    - iphone678 手机型号
    - 375*667 手机屏幕分辨率
    - 75% 最佳观看比例
    - 旋转小图标 切换横屏和竖屏
    - 右上角三个圆点
        - capture screenshot 截取手机屏幕设计稿（短图）
        - capture full size screenshot 截取手机屏幕设计稿（长图）
4. 设备的大小/屏幕的大小
    - iphone678 --- 375*667
    - iphone678plus --- 414*736
    - iphonex  --- 375*812
5. 获取设计稿的大小
    - iphone678 --- 750*1334 ---- 2倍
    - iphone678plus --- 1242*2208  --- 3倍
    - iphonex  --- 1125*2436  --- 3倍
6. 倍数，固定好的值
    - 设备像素比：比值（dpr）
    - 物理像素：设计稿中的大小，设计稿中测量出来的距离
    - css像素：作为开发人员，开始时候编写的css像素，可以理解为屏幕大小
    - 设备像素比 = 物理像素 / css像素 

# 三、引入视口
1. 问题：700px明显大于屏幕大小，可以双击缩放（默认移动端不允许缩放）
    - div=700*300
    - 在iphone678(375)能显示出一个700px宽度的盒子

2. 原因：视口不同
    - 视觉视口：看得到的这个窗口，屏幕大小
    - 布局视口：编写的css和html页面是布局视口
    - 理想视口：理想化的视口，将布局视口完整的放在视觉视口中，通过一行代码将页面按照比例放在手机屏幕里

3. 引入理想视口
    - <meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no">
    - meta标签引入
        - name属性=“viewport” 视口
        - content属性=“设置内容”
            - width=device-width 宽度=设备的宽度
            - initial-scale=1.0 最初缩放比例为1
            - minimum-scale=1.0 最小缩放比例为1
            - maximum-scale=1.0 最大缩放比例为1
            - user-scalable=no 不允许用户缩放

# 四、移动端布局步骤
1. 方式
    - flexible，响应式，固定px，rem等
2. 确定设计稿出自于哪一个屏幕
    - 为了确定dpr确定设备像素比
3. 确定css像素
    - css像素=物理像素/dpr
    - 可以这样理解：css像素=测量的距离/2
4. 引入理想视口
    - <meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no">
5. 引入icon图标，引入css样式
    - <link rel="stylesheet" hre="./font/iconfont.css">
    - <link rel="stylesheet" hre="./css/style.css">
6. 编写移动端布局
    - HTML部分
        <body>
            <header></header>
            <section></section>
            <footer></footer> 
        </body>
    - CSS部分
        *{margin: 0; padding: 0;}
        li{list-style: none;}
        img{display: block;}
        a,s,del,u{text-decoration: none;}
        i,em{font-style: normal;}
        strong,b{font-weight: normal;}
        a img{border: 0;}
        input,textarea{outline: 0;}
        .over{overflow: hidden; zoom: 1;}
        .wnqc::after{content: ""; display: block; width: 0; height: 0; visibility: hidden; clear: both;}
        html,body{width: 100%; height: 100%;}
        body{display: flex;flex-direction: column;}
        ::-webkit-scrollbar{display: none;}

# 作业
1. 整理笔记
2. 敲知识点
3. 作业
    - 补周六作业
    - 千锋移动端
4. 预习