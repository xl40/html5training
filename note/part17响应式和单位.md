# 一、复习
1. 引入理想视口
    <meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no">
2. 高度塌陷
    - 单元素浮动 后面元素添加clear:both;
    - 多元素浮动，4种
        - 给父级设高度
        - 父元素后添加块级子元素，设置clear:both;
        - 给父级添加overflow:hidden;zoom:1;
        - 父元素::after{content:''; display:block; width:0; height:0; visibility:hidden; clear:both;}
3. 盒模型的计算
    - 官方盒子 水平范围=width+左右padding+左右border+左右margin
    - 怪异盒子 水平范围=width（包含了内容区、内边距、边框）+左右margin
    - box-sizing:border-box/content-box
4. 绝对定位和相对定位的区别
    - 绝对定位，position:absolute; 原位置不保留，相对于最近的已定位的父或祖元素
    - 相对定位，position:relative; 原位置保留，相对于自身
5. 图片下方产生缝隙，如何解决，3种
    - display:block; / vertical-align:top; / float:left;
6. 姓名

# 二、响应式布局
1. 什么是响应式布局
    - 根据不同的设备屏幕大小进行检测，检测出不同的屏幕设备，会改变已有的布局模式

2. 响应式布局的效果样式
    - 挤压/拉伸
    - 删除/增加
    - 显示/隐藏
    - 布局模块改变（左右布局---上下布局）

3. 响应式布局的优缺点
    - 优点：
        - 兼容所有的设备，能够做到很好的适配效果；根据不同屏幕的大小，改变对应的布局效果
    - 缺点：
        - 代码量大，代码冗余，工作量就大了
        - 加载时间过长
        - 容易混淆布局模块，造成用户体验度降低
        - 相应适应布局是一种折中布局方案
    
4. 实现响应式布局的方法
    - 媒体查询
    - 是一种技术，用来检测设备的大小，检测完毕后，会根据对应的内容进行不同的布局显示
    - 检测的是屏幕的大小（屏幕的宽度）

# 三、媒体查询
1. 含义
    - 通过媒体查询技术，检测screen屏幕，并且最小宽度为320px；最大宽度为480px的条件下，对应的选择器执行对应的样式

2. 基本语法
    @media only screen and (min-width:800px) and (max-width:1000px){
        选择器{ css语句 }
    }
    - media 声明媒体查询
    - only 关键词
        - not 排除
        - only 仅仅
    - screen 检测设备的类型（screen，TV等等）
    - and 关键词，检测设备的同时要满足后面的条件
        - and 并且
        - or 或者 符号是逗号
    - (条件) 满足的条件

3. 横竖屏检测
    - 竖屏
        - @media screen and (orientation:portrait){ }
    - 横屏
        - @media screen and (orientation:landscape){}

4. 媒体查询外部样式表
    <link rel="stylesheet" href="css路径" media="screen and (max-width:800px)">

# 四、px-em-rem
1. 常用的单位
    - px 像素单位
        - 固定的死值，是多少个px就显示多少像素的大小
    - em 相对单位
        - 相对于父元素调整字号或宽高
    - rem 相对单位
        - 相对于根目录html调整字号和宽高
        - 默认的1rem=16px
        - 根目录字号调整成font-size:30px;那么1rem=30px

2. 单位如何设置合适？
    - 思考：若移动端布局的时候，使用的单位是rem
        - 设计稿里面测量的距离：100px（物理像素），如何转成rem
        - css像素：100px/dpr ======= 50px
        - css(rem) 50px/16 ====3.125rem
    - 公式：需要转化成rem这个单位
        - css(rem) = 物理像素/dpr/font-size
    - 复杂案例：iphone678
        - 测量的距离：88px
        - 88像素转换成rem单位
        - 88px/dpr(2)/font-size(16)
        - 88/2/16=2.75rem
    - 简单计算：iphone678
        - html{font-size:50px;}
        - 测量的距离：88px
        - 88px/dpr(2)/font-size(50)
        - 88/2/50 = 0.88rem

# 五、vw和vh
1. 能够实现等比例缩放的布局，可以应用在移动端布局里面

2. vw和vh
    - vw：view width
        - 视口的宽度
        - 100vw=一个完整的视口宽度
    - vh：view height
        - 视口的高度
        - 100vh=一个完整的视口高度
    
3. 百分比和vw区别
    - 100% 占父元素的一个百分比
    - 100vw 屏幕的宽度
    - 分情况：
        - 如果页面没有滚动条或间距清零的话，两者实现效果一致
        - 如果页面有滚动条或间距不清零，两者实现效果不一致
            - 视口的宽度，里面包括滚动条
            - width：100% 里面不包括滚动条

4. 单位换算
    - 简单计算案例：ipone678
        - html{font-size:50px}
        - 测量的距离 88px
        - 88px/dpr(2)/50 = 0.88rem
        或者
        - html{font-size:100px}
        - 测量的距离 88px
        - 88px/dpr(2)/100 = 0.44rem
    
    - 现在要设置font-size:?vw，才能相当于font-size:100px;
        - 比如：iphone5手机屏幕
        屏幕大小：320px
            - 320px=100vw
            - 100px=？vw === 31.25vw
        那么制作iphone5等比例缩放的移动端布局的时候，html{font-size:31.25vw;}

# 六、flexible.js
1. js文件是一个脚本文件，不能直接双击打开，可以使用编辑器/txt文档查看

2. 优点：
    - 使用引入js的方法，直接进行rem布局，只需要把js文件引入即可
    - 不需要考虑视口，不需要考虑dpr，测量的物理像素直接/100即可

3. 使用flexible.js文件布局的步骤
    - 注意js文件中7.5数值的意义，ps菜单栏“图像”--“图像大小”--等比例改为750px
    - 引入js文件
        <script src='js文件的路径'></script>
    - 引入icon图标和css文件
    - HTML部分
        <body>
            <header></header>
            <section></section>
            <footer></footer>
        </body>
    - CSS部分
        *{margin: 0;padding: 0;}
        li{list-style: none;}
        a,u,del,s{text-decoration: none;}
        em,i{font-style: normal;}
        b,strong{font-weight: normal;}
        img{display: block;}
        a img{border: 0;}
        input,textarea{outline: 0;}
        .over{overflow: hidden;zoom: 1;}
        .wnqc::after{content: ''; display: block; width: 0; height: 0; visibility: hidden;clear: both;}
        html,body{width: 100%;height: 100%;}
        ::-webkit-scrollbar{display: none;}
        body{display: flex; flex-direction: column;}

# 作业
1. 整理笔记
2. 敲知识点
3. 作业
    - 响应式、淘宝女装 写完
    - 项目10选1，比如6个页面
4. 预习