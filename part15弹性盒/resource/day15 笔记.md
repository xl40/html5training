# 一、复习
1. 定义动画两种方式
    @keyframe 动画名{ from{}  to{} }
    @keyframe 动画名{ 0%{}  50%{}  100%{} }
2. 动画的属性，8个，及复合属性
    animation-name / animation-duration / animation-timing-function / animation-delay / animation-iteration-count / animation-direction / animation-fill-mode / animation-play-state
    animation:动画名 播放时间 时间曲线 延迟时间 播放次数 播放方向 时间外的属性
3. 3D旋转、位移
    transform:rotateX() / rotateY() / rotateZ() / rotate3d(1,0,0,deg)
    transform:translateX() / translateY() / translateZ()
4. 3D舞台、景深
    transform-style:preserve-3d; perspective
5. 姓名

# 二、弹性盒
1. 含义
    - 弹性盒是css3里面引入进来的一种新的布局方式，只对子元素起作用，只会影响子元素的排列方式
    - 父元素设置 display:flex;

2. 名称
    - 容器：盛放子元素的盒子，父元素
    - 项目：所有的弹性盒子里面的子元素，子元素

3. 弹性盒子的特点
    - 当父元素变成弹性盒之后，子元素默认横向显示
    - 当父元素变成弹性盒之后，子元素能识别宽高
    - 当父元素变成弹性盒之后，如果只有一个子元素，实现水平垂直居中可以给子元素添加margin:auto;

# 三、容器属性
1. flex-direction 调整主轴方向
    - row 默认值，规定主轴方向在横向
    - column 规定主轴方向在纵向
    - row-reverse 规定主轴方向在横向，项目反向排列
    - column-reverse 规定主轴方向在纵向，项目反向排列

2. justify-content 调整项目在横轴对齐方式
    - flex-start 横轴的开始位置对齐，没有间距
    - flex-end 横轴的结束位置对齐，没有间距
    - center 横轴的中间位置对齐，没有间距
    - space-between 横轴的两端对齐，元素与元素的间距自动分配
    - space-around 横轴的间距环绕，元素与元素两边间距是中间的一半
    - space-evenly 横轴的间距环绕，元素与元素的间距一致

3. align-items 调整项目在纵轴上的对齐方式
    - flex-start 纵轴的开始位置
    - flex-end 纵轴的结束位置
    - center 纵轴的中间位置
    - stretch 拉伸，子元素不设高度有效

4. margin:auto 原理
    - 横轴居中，纵轴居中
    - justify-content: center;
    - align-items: center;

5. flex-wrap 是否换行
    - nowrap 不换行
    - wrap 换行
    - 父元素变成弹性盒后，子元素过多
    - 默认不回折行，会产生挤压效果
    - 默认折行后，行间距自动分配，行间距比较大

6. align-content 调整行间距
    - flex-start 纵轴开始位置对齐，没有行间距
    - flex-end 纵轴结束位置对齐，没有行间距
    - center 纵轴中间位置对齐，没有行间距
    - space-between 纵轴两端对齐，中间间距自动分配
    - space-around 纵轴间距环绕，元素与元素上下间距是中间的一半
    - space-evenly 纵轴间距环绕，元素与元素间距一致

# 四、项目属性
1. align-self 项目纵轴的对齐方式
    - flex-start 纵轴的开始位置
    - flex-end 纵轴的结束位置
    - center 纵轴的中间位置
    - stretch 纵轴拉伸，不设置高度

2. order 子元素的前后顺序
    - 是一个数值，没有单位
    - 取值越大越靠后

3. flex:1 占剩余宽度/高度
    - 如果子元素都添加了flex:1/2/3 代表占几份

4. flex-shrink 元素是否被挤压
    - 1 默认值，挤压
    - 0 不挤压，制作移动端的横向滚动

5. 移动端滚动条隐藏
    ::-webkit-scrollbar{
        display:none;
    }

# 五、多列布局
1. 应用：制作瀑布流布局，按照列数进行布局
2. column-count 列数
    - 取值：数值
3. column-width 列宽
    - 取值：px为单位的数值
4. column-gap 列间距
    - 取值：px为单位的数值
5. column-rule:1px solid red 列间隔线
    - 类似于边框属性
6. column-fill 列高度
    - balance 默认值，均分高度
    - auto 先填满父元素所在的第一列再去补第二列
7. column-span 跨列
    - all 跨所有列
    - none 不跨列
8. break-inside: avoid; 不折列

# 作业
1. 整理笔记
2. 敲知识点
3. 作业
    - 03 长图 / 04 / 练习小青蛙
4. 预习