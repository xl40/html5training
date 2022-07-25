# 一、复习
1. 最小最大高度 min-height max-height
2. 隐藏元素的方法，6种
    - rgba() / opacity / visibility:hidden / transform:scale(0)
    - display:none / width:0;height:0;
3. 伪元素选择器，4个
    - ::after{content:"";} / ::before{content:url();}
    - ::first-letter{} / ::frist-line{}
4. 解决高度塌陷
    - 单元素浮动 后面元素清除浮动，clear:both;
    - 多元素浮动，4种
        - 给父元素设置高度
        - 父元素后添加块级子元素，给这个元素设置clear:both;
        - 父元素设置oveflow:hidden;zoom:1;
        - 父元素::after{content:'';display:block;width:0;height:0;visibility:hidden;clear:both;}
5. 窗口自适应 html,body{width:100%;height:100%;}
6. 浮动框架集
    <iframe src="" frameborder='0' width="" height=""></iframe>
7. 动态计算函数 calc(100% - ?px)
8. 姓名

# 二、html5简介
1. 含义：HTML5是超文本标记语言的第五个版本，仍处于更新迭代中

2. 新增内容
    - 语义化标签
        - 作用：方便开发人员使用，不用再去取类名，获取元素更加方便快捷高效
    - 增强型的表单
        - 作用：增加一些提前验证的功能
    - 音频和视频
        - 用来替换很多的flash
    - 各种API
        - 方法函数直接使用
    - canvas标签
    - svg绘图
        - 绘图方法
    - 离线存储本地存储
        - 存储数据

3. 常用浏览器
    - chrome 谷歌浏览器
    - firefox 火狐浏览器
    - safari 苹果浏览器
    - IE 微软IE浏览器
    - opera 欧朋浏览器
    - 由于浏览器内核不一样，才导致了浏览器的兼容出现问题
    - 内核
        - IE浏览器：Trident内科，俗称IE内核
        - Chrome浏览器：俗称chrome内核，以前是webkit内核，现在blink内核
        - firefox浏览器：gecko内核，俗称firefox内核
        - safari浏览器：webkit内核
        - opera浏览器：最初是presto内核，后来是webkit，现在blink内核

4. 语法
    - 扩展名，.html和.htm
    - DOCTYPE声明不区分大小写
    - 单标记可以不写结束标签
    - 双标签可以省略结束标记
    - 可以省略html、head、body
    - 引号可以使用单引号

# 三、HTML5标签
1. 语义化标签
    - header 头部
    - footer 尾部
    - section 主体
    - nav 导航
    - main 主要内容区域
    - aside 侧边栏
    - article 文章区域
    - figure 独立的文档流区域
    - figcaption 独立的文档流区域的标题
    - hgroup 网页区域的标题进行组合
    - 以上都是块级元素，双标签，遵循所有的css和html对应的语法和属性

2. audio 音频
    - 支持格式：ogg、mp3、wav
    - src 路径
    - controls 控件
    - loop 循环
    - autoplay 自动播放
    - muted 静音
        - 谷歌浏览器，自动播放无效
        - 火狐浏览器，静音和自动播放同时使用则可以自动播放

3. video 视频标签
    - 支持格式：ogg、mp4、webm
    - src 视频路径
    - controls 控件
    - loop 循环
    - autoplay 自动播放
    - muted 静音
        - 需要静音之后才能自动播放
    - poster 加载时显示的图像

# 四、HTML5表单和属性
1. 表单
    - 基本语法：<input type="?">
    - type="color" 颜色拾取器
    - type="range" 滑块
        - value=“当前值” 默认最小为0，最大为100
        - min=“最小值”
        - max=“最大值”
        - step=“数值间隔”
    - type=“number” 数值
        - value=“当前值”
        - min=“最小值”
        - max=“最大值”
        - step=“数值间隔”
    - type=“tel” 拨号盘，唤起拨号盘，移动端使用
    - type=“email” 邮箱
        - 没有输入内容的话，会默认直接验证通过
        - 只要输入内容，必须遵循邮箱地址格式
    - type=“url” 地址栏
        - 没有输入内容的话，会默认直接验证通过
        - 只要输入内容，必须遵循地址栏格式
    - type="search" 搜索框
        - 可以清空输入框中自己输入的数据
    - type=“date” 日期，包含年月日
    - type=“month” 月份，包含年月
    - type=“week” 周期，包含年周
    - type=“time” 时间
    - type=“datetime-local” 本地时间，年月日时间

2. 属性
    - required 验证不能为空，必须填写此字段
    - autofocus 自动获取焦点，只能有一个获取到，无论添加多好都是第一个选中
    - multiple 能提交多个邮箱，多个邮箱之间用逗号分隔
    - 列表清单，仿模糊搜索
        - 语法：
            <input type="text" list="car">
            <datalist id="car">
                <option value="bmw">宝马/</option>
            </datalist>
        - 注意：
            - input标签的list属性值要与datalist标签的id属性值匹配
    - autocomplete=‘off/on’ 开启或关闭自动提示文本
        - on 默认值，开启
        - off 关闭
    - pattern=“[0-9]{2}[a-z]{3}” 正则表达式，实际开发的时候用js编写

# 五、补充
1. outline 轮廓，取值同border

2. outline-offset 轮廓偏离距离，正值外扩，负值内收

3. appearance:none; 清除默认样式，如下拉菜单的下拉图标

# 作业
1. 整理笔记
2. 知识点
3. 作业
    - 探路者
4. 预习