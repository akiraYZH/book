# HTML标签介绍


* `HTML`  页面记得一定要在第一行声明语法规范
`<!DOCTYPE html>`

* `header` 标签通常设置以下属性

    * title **标题**

    * meta **可提供有关页面的元信息**
    
        * keyword **关键字**
        * description **页面的描述**
        * author **作者**
        * viewport **视觉窗口(移动端)**

    * icon 网页小图标

* 盒子模型 Box Model
     <!-- <hr/> -->
        

    * 块级元素 block
        * 特点
            1. 块级元素就算内容不足以支撑一整行, 标签也会自动占满一整行
        * 常见标签
            * 标题标签 `<h1></h1> ~ <h6></h6>`
            * 引用块 `<blockquote></blockquote>`
                * `cite`	(URL)	规定引用的来源。
            * `<div>`标签
            * `<figure>` 标签
            * `<form>` 标签
                * `action`	(URL)	规定当提交表单时向何处发送表单数据。
                * `autocomplete`	(on||off) 规定是否启用表单的自动完成功能。
                * `method`	(get||post) 规定用于发送 form-data 的 HTTP 方法。
            * `<ol>` 标签
                * `reversed`	规定列表顺序为降序。(9,8,7...)
                * `start`	(number)	规定有序列表的起始值。
                * `type`	( `1` || `A` || `a` || `I` || `i` ) 规定在列表中使用的标记类型。

    * 行内元素 inline
         <!-- <hr/> -->
        
        * 特点
            1. 标签占地面积就是文本的占地面积
        * 常见标签
            * 删除标签 `<del></del>`
            * 上标签`<sup></sup>`
            * 下标签`<sub></sub>`
            
            * 超链接 `<a href="链接跳转的地址" target="链接打开方式"></a>`
                * `href` 表示链接跳转的地址
                * `target` 链接打开方式
                 * `_blank` 新的窗口打开
            * `<abbr>` 缩写,效果为双引号
            * `<code>` 定义计算机代码文本。
            * `<dfn>` 定义一个定义项目。
            * `<em>` 把文本定义为强调的内容。
            * 音频 
            `<audio src="someaudio.wav">
                您的浏览器不支持 audio 标签。
            </audio>`
                 * `autoplay` 自动播放
                 * `controls` 如果出现该属性，则向用户显示控件，比如播放按钮。
                 * `loop` 如果出现该属性，则每当音频结束时重新开始播放。
                 * `muted` 规定视频输出应该被静音。
                 * `preload` 如果出现该属性，则音频在页面加载时进行加载，并预备播放。

                    如果使用 "autoplay"，则忽略该属性。

                 * `src` 要播放的音频的 URL。

            

    * 行内会计元素 inline-block
        <!-- <hr/> -->
        
        * 特点
        * 常见标签
            * 图片 `<img src="地址" alt="备注"></img>`

                * `src`  表示引入图片的路径
                * `alt`  表示链接失效时的提示
            

            * 按钮`<button type="button"></button>`
                * `autofocus`	规定当页面加载时按钮应当自动地获得焦点。
                * `disabled`	规定应该禁用该按钮。
                * `form` 规定按钮属于一个或多个表单。
                * `type` 规定按钮的类型。
            * `<embed>` 标签(h5)
                * `height`	(pixels)	设置嵌入内容的高度。
                * `src`	(url)	嵌入内容的 URL。
                * `type`	(type)	定义嵌入内容的类型。
                * `width`	(pixels)	设置嵌入内容的宽度。
            * progress标签 `<progress value="22" max="100"></progress> `
                * `max`	(number)	规定任务一共需要多少工作。
                * `value`	(number)	规定已经完成多少任务。
            * `<select>` 标签
                * `autofocus`	(autofocus)	规定在页面加载后文本区域自动获得焦点。
                * `disabled`	disabled	规定禁用该下拉列表。
                * `form`	(form_id)	规定文本区域所属的一个或多个表单。
                * `multiple`	(multiple)	规定可选择多个选项。
                * `name`	(name)	规定下拉列表的名称。
                * `required`	规定文本区域是必填的。
                * `size`	(number)	规定下拉列表中可见选项的数目。


    <!-- <br />
    <br /> -->

    > 外边距 margin
    >> 边框 border
    >>> 内边距 padding
    >>>> 中心内容 content

<!-- <br />
<br />
<br />
<br /> -->

* 绝对路径与相对路径

    1. 绝对路径就是指网络地址路径, 不管在什么环境下都能通过这个地址直接访问到对应文件 `https://www.baidu.com/img/bd_logo1.png?where=super`

    2. 相对路径是指以当前引入文件的根目录为起点, 根据相对应的文件路径找到对应的文件
        * ./ 同级目录

        *  ../ 返回上一级目录

        * xxx/ 进入xxx目录

<!-- <br />
<br />
<br />
<br /> -->

# 作业

## `1. src和href区别`


1. `href`是`Hypertext Reference`的缩写，表示超文本引用。用来建立当前元素和文档之间的链接。常用的有：link、a。例如：

    `<link href="reset.css" rel=”stylesheet“/>`

    浏览器会识别该文档为css文档，并行下载该文档，并且不会停止对当前文档的处理。这也是建议使用link，而不采用@import加载css的原因。


2. `src`是`source`的缩写，src的内容是页面必不可少的一部分，是引入。src指向的内容会嵌入到文档中当前标签所在的位置。常用的有：img、script、iframe。例如

    `<script src="script.js"></script>`

    当浏览器解析到该元素时，会暂停浏览器的渲染，知道该资源加载完毕。这也是将js脚本放在底部而不是头部得原因。

    简而言之，***`src用于替换当前元素；href用于在当前文档和引用资源之间建立联系`***。

<!-- <br />
<br />
<br /> -->

## `2. 标签的分类`

1. 行内元素 (inline)

    ```
    <a>
    <img>
    <input>
    <textarea>
    <abbr>（缩写）
    <acronnym>（首字母）
    <b>
    <bdo> 
    <big>
    <br>
    <cite>（引用）、<code>、<dfn>（定义字段）、<em>（强调）、<font>、<i>（斜体）、<kbd>（定义键盘文本）、<label>（表格标签）、<q>（短引用）、<s>（中画线、不推荐）、<samp>（代码）、<select>、<small>、<span>、<strike>（中划线）、<strong>、<sub>（下标）、<sup>（上标）、<tt>（电传文本）、<u>（下划线）、var
    ```

2. 块级元素 (block)
    ```
    <address>、<blockquote>（块引用）、<center>、<dir>（目录列表）、<div>、<dl>（定义列表）、<fieldset>（form控制组）、<form>、<h1>~<h6>、<hr>、<isindex>（input prompt）、<menu>（菜单列表）、<noframes>（frames可选内容）、<noscript>、<ol>、<p>、<pre>（格式化文本）、<table>、<ul>
    ```

3. 可变元素（根据上下文语境决定该元素为块元素或内联元素）
    ```
    <applet>、<button>、<del>、<iframe>、<ins>（插入文本）、<map>、<script>
    ```
4. 空元素（在HTML[1]元素中，没有内容的元素）
    ```
    <br/>、<hr/>、<input>、<img>、<link>、<meta>
    ```

<br/>
<br/>
<br/>

## `3. HTML4 And HTML5 标签整理`



* HTML5中新增的标签

    ```
    <article> 定义文章
    <aside> 定义页面内容旁边的内容
    <audio> 定义声音内容
    <canvas> 定义图形
    <command> 定义一个控制按钮
    <datagrid> 指树或表格状数据格式中的动态数据
    <datalist> 定义一个下拉列表
    <details> 定义一个元素的细节
    <dialog> 定义会话或人的交谈
    <embed> 定义额外的交互内容或插件
    <figcaption>定义指定元素的标题
    <figure> 定义一组媒体内容，以及他们的标题
    <footer> 为章节或页面定义一个底部
    <header> 为章节或页面定义一个头部
    <hgroup> 定义文档中某段落的信息
    <keygen> 定义表单生成的关键
    <mark> 定义被标记的文本
    <meter> 定义预定义范围内的测量
    <nav>  定义导航链接
    <output> 定义某种类型的输出
    <progress> 定义任意种类任务的进程
    <rp> 定义浏览器不支持ruby元素的替代者
    <rt> 定义ruby注释的解释
    <ruby> 定义 ruby 注释（中文注音或字符）
    <section> 定义章节
    <source> 定义媒体资源
    <summary> 定义某”detail”元素的头部
    <time> 定义日期/时间
    <video> 定义视频
    <wbr> 定义可能的换行
    ```

* HTML5支持且同时存在于HTML4中的标签

    ```
    <!– …–> 定义注释
    <!DOCTYPE> 定义文档类型
    <a>      定义超链接
    <abbr> 定义缩写
    <address> 定义地址元素
    <area> 定义图片地图的某区域
    <b>   定义加粗文字
    <base> 定义整个页面的基础URL
    <bdo> 定义文本显示的方向
    <blockquote> 定义一个长引用
    <body> 定义主体元素
    <br> 插入单个的换行
    <button> 定义按钮
    <caption> 定义表格的标题
    <cite> 定义引用
    <code> 定义计算机代码文本
    <col> 定义表格列的属性
    <colgroup> 定义表格列的组
    <dd> 定义个定义描述
    <del> 定义删除文本
    <dfn> 定义个定义项
    <div> 定义文档章节
    <dl> 定义定义列表
    <dt> 定义定义项
    <em> 定义强调文本
    <fieldset> 定义控件组                                 <form> 定义表单
    <h1>到<h6> 定义头部1到头部6
    <head> 定义文档信息
    <hr> 定义水平线
    <html> 定义个html文档
    <i> 定义倾斜文本 
    <iframe> 定义内联替代窗口（框架）
    <img> 定义个图片
    <input> 定义输入域
    <ins> 定义插入文本
    <kbd> 定义键盘文本
    <label> 定义表单控件的标签 
    <legend> 定义控件组的标题
    <li> 定义列表项
    <link> 定义相关资源
    <map> 定义图片地图
    <menu> 定义菜单列表
    <meta> 定义元信息
    <noscript> 定义无脚本章节
    <object> 定义内嵌对象
    <ol> 定义一个有序列表
    <optgroup> 定义个选项组
    <option> 定义下拉列表选项
    <p> 定义段落 
    <params> 定义object的参数
    <pre> 定义预格式化文本
    <q> 定义短引用
    <s> 定义不再正确的文本
    <samp> 定义简单的计算机代码
    <script> 定义脚本                                    <select> 定义可选择列表
    <small> 定义小点的文本
    <span> 定义文档章节
    <strong> 定义强调的文字
    <style> 定义一个样式定义
    <sub> 定义下标文字
    <sup> 定义上标文字
    <table> 定义表格
    <tbody> 定义表格的主体
    <td> 定义表格单元格                                 <textarea> 定义文本域
    <tfoot> 定义表格底部
    <th> 定义表格头
    <thead> 定义表格头
    <title> 定义文档的标题
    <tr> 定义表格行 
    <ul> 定义无序列表
    <var> 定义变量
    ```
 

* HTML5不支持的标签

    ```
    <acronym> 在HTML4.01中定义首字母缩略词
    <applet> 定义内嵌的小应用程序
    <basefont> 定义文档中基本的字体属性
    <big> 让文字变大点
    <center> 居中显示文字或内容
    <dir> 定义目录列表
    <font> 指定字体种类，大小，颜色等
    <frame> 在框架集中定义独有的窗体
    <frameset> 定义框架集，包含多个窗体
    <noframe> 当浏览器不支持框架的时候显示文字
    <strike> 定义删除线文本
    <tt> 定义电传打字机文本
    <u> 定义下划线文字
    <xmp> 定义格式化的文字
    ```