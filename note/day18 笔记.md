# 一、复习
1. 响应式的优缺点
    - 优点 兼容所有设备，做到适配效果，根据不同屏幕大小，改变对应的布局效果
    - 缺点 代码冗余 / 加载时间长 / 容易混淆模块，影响用户体验
2. 媒体查询基本语法
    @media screen and (min-width:?px) and (max-width:?px){
        选择器{ css语句 }
    }
3. 媒体查询-横屏竖屏
    - 竖屏 @media screen and (orientation:portrait){}
    - 横屏 @media screen and (orientation:landscape){}
4. px、em、rem、vw、vh
    - px 像素单位，固定死值
    - em 相对单位，相对于父元素
    - rem 相对单位，相对于根目录
    - vw 一个完整的视口宽度
    - vh 一个完整的视口高度
5. 姓名

# 二、网格布局
1. 作用
    - 制作一些特殊的布局模式，把网页划分成一个一个的网格，然后进行合并，拼接出各种不同的布局效果
    - 网格布局又叫做grid布局

2. grid布局与flex布局的异同点
    - 相同点：
        - 二者都存在两个概念，容器（父元素），项目（子元素）
    - 不同点：
        - flex布局，轴线布局按照某一个轴进行布局，称之为一维布局
        - grid布局，网格布局，有行和列，称之为二维布局

3. 方法：
    - 给父元素添加display属性
    - display:grid 块状网格
    - display:inline-grid 行内网格

4. 网格线
    一个1行1列的网格，2条横线，2条纵线
    一个1行2列的网格，2条横线，3条纵线
    一个2行1列的网格，3条横线，2条纵线
    一个3行3列的网格，4条横线，4条纵线
    一个m行n列的网格，m+1条横线，n+1条纵线

# 三、容器属性
1. 设置网格布局
    - display:grid/inline-grid

2. 行和列
    - 后面跟多少组值代表的是多少行多少列
    - grid-template-columns 划分列数
    - grid-template-rows 划分行数
    - 取值
        - 绝对大小
            - grid-template-columns: 100px 200px 200px;
        - 百分比
            - grid-template-columns: 20% 20% 30%;
        - 重复函数
            - grid-template-columns: 10% repeat(3,20%);
            - 重复函数 repeat(重复次数，重复显示的宽和高)
        - 自动重复填充
            - grid-template-columns: 10% repeat(auto-fill,20%);
        - 片段划分
            - grid-template-columns: 1fr 2fr 3fr;
            - 1等份，2等份，3等份
        - 剩余填充
            - grid-template-columns: 100px auto 50px;
        - 最小最大函数
            - grid-template-columns: minmax(100px,200px) 400px 150px;

3. 网格线命名
    - 在对应的当前格的行列前后添加[]进行命名
    - grid-template-columns: [c1] 100px [c2] 100px [c3];
    - grid-template-rows: [r1] 100px [r2] 100px [r3];

4. 行间距和列间距
    - grid-column-gap 列间距
    - grid-row-gap 行间距
    - grid-gap:行间距 列间距;

5. 区域命名和合并
    - 一般使用的是简单字母
    - 九宫格
    - 矩形范围内命名
    grid-template-areas: 'a a c'
                         'a a f'
                         'g h i';
    - 子元素合并
        - grid-area: a;

6. 排列方式
    - grid-auto-flow
        - row 默认值，横向排列
        - column 纵向排列

7. 项目对齐方式（子元素在各自单元格的对齐方式），子元素设宽高
    - justify-items 项目水平对齐方式
        - start 单元格的起始位置
        - end 单元格的结束位置
        - center 单元格的居中位置
        - stretch 拉伸，不设宽度的话，占满整个单元格
    - align-items 项目垂直对齐方式
        - start 单元格的起始位置
        - end 单元格的结束位置
        - center 单元格的居中位置
        - stretch 拉伸，不设高度的话，占满整个单元格
    - 复合属性
        - place-items:垂直对齐方式 水平对齐方式;

8. 内容对齐方式（子元素整体在容器内的对齐方式）
    - justify-content 内容水平对齐方式
        - start 容器的起始位置
        - end 容器的结束位置
        - center 容器的中间位置
        - space-around 项目两侧的间距是中间的一半
        - space-between 两端对齐无间距，中间间距均分
        - space-evenly 所有间距均分
    - align-content 内容垂直对齐方式
        - start 容器的起始位置
        - end 容器的结束位置
        - center 容器的中间位置
        - space-around 项目两侧的间距是中间的一半
        - space-between 两端对齐无间距，中间间距均分
        - space-evenly 所有间距均分
        - stretch 拉伸，行只有线没有高度，则盛满父级
    - 复合属性
        - place-content:垂直对齐方式 水平对齐方式
        
# 四、项目属性
1. 网格线合并
    - grid-column-start 左边框所在的垂直网格线
    - grid-column-end 右边框所在的垂直网格线
    - grid-row-start 上边框所在的水平网格线
    - grid-row-end 下边框所在的水平网格线
    - 复合属性
        - grid-column:1/3 或者 c1/c3
        - grid-row:2/4 或者 r2/r4
            - /前面的是起始线
            - /后面的是结束线，合并到的那一条线