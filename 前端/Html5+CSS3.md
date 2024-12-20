
> 文章持续更新中，最近更新日期`2024-9-19`（~~不保证100%完工.jpg~~）  
> 
> 课程视频[B站链接](https://www.bilibili.com/video/BV1XF41187ZJ)  
> 
> 当前进度`058-盒子模型-内边距特性`  
  
  
#  环境配置  
  
* VScode  
    * [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag) 自动同步修改头尾标签  
    * [view-in-browser](https://marketplace.visualstudio.com/items?itemName=koppt.vscode-view-in-browser) 跳转浏览器查看文件  
    * [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) 实时查看页面，开启本地服务器  
* webstrom  
  
  
# I.html基本语法  
  
## 1.1 常规标记  
  
`<标签> </标记>`  
  
`<标签  属性="属性值"  属性="属性值"> </标记>`  
  
标记也可以叫做标签或者元素  
  
例如：`<head> </head>`  
  
## 1.2 空标记  
  
`</标记>`  
  
`</标记  属性="属性值">`  
  
例如：`<br/>`  
  
# II. 文档声明与字符编码  
  
## 2.1 文档声明标签  
  
文档声明标签`<!DOCTYPE ****>`，告诉浏览器如何解析代码  
  
## 2.2 语言声明  
`<html lang="en">`中`lang`就是对html标签的修饰，对搜索引擎和浏览器有帮助，书写的时候声明和书写尽量一致  
  
* `en`英文  
* `zh-CN`中文  
* `ja-jp`日文  
* `ru`俄文  
  
## 2.3 编码格式  
  
`<meta charset="UTF-8">`表示使用UTF-8进行编码，注意和editor的编码设置使用的一致  
  
# III. HTML常用标签  
  
## 3.1文本标题标签h1-h6  
  
* `<h1>一级标签</h1>`  
* .......  
* `<h6>六级标签</h6>`  
  
## 3.2 段落文本p  
  
`<p>文本</p>`  
  
## 3.3 换行  
  
`<br/>`换行是一个空标记，强制换行  
  
## 3.4 水平线  
  
`<hr/>`空标记  
  
## 3.6 加粗有2个标记  
  
推荐**strong**  
  
`<b>加粗内容</b>`只是显示加粗  
  
`<strong>强调的内容</strong>`突出的文本  
  
## 3.6 倾斜的2个标记（推荐em）  
  
`<em>强调文本</em>`  
  
`<i>倾斜文本</i>`  
  
## 3.7 删除线有2个标记（推荐del）  
  
`<s>文本</s>`删除线  
  
`<del>文本</del>`删除线  
  
## 3.8 扩展  
  
`<u>文本</u>`下划线  
  
`<sub></sub>`下标  
  
`<sup></sup>`上标  
  
  
# IV. 属性的使用  
  
以`<hr/>`为例子  
  
~~~html  
<hr color="green" size="10" width="300" align="left" noshade/>  
~~~  
  
* color颜色  
* size高度  
* width长度  
* align对其方向  
* noshade不显示阴影  
  
# V. 特殊符号  
  
* 尖角号  
    * 左<`&lt;`  
    * 右>`&gt;`  
* 空格  
    * `&nbsp;`受字体影响大小  
    * `&emsp;`正好是一个中文宽度  
* 商标  
    * `&trade;` ™  
    * `&reg;`®  
* 版权  
    * `&copy;`©  
  
# VI. div和span标签  
  
div标签，没有具体含义，用来划分页面的区域，独占一行  
  
span，没有实际意义，主要应用在对于文本独立修饰的时候，内容有多宽就占用多宽的空间距离，不会破坏结构。  
  
# VII. 列表  
  
## 7.1 无序列表list  
  
~~~html  
<ul>  
    <li>1</li>    <li>2</li>    <li>3</li></ul>  
~~~  
  
* `ul`里面只能放`li`，`li`里面可以放其他标签  
* 默认的是黑色的实心圆  
* `type`可以为黑色实心圆`disc`，空心圆`circle`，正方形`square`，`null`空白  
  
## 7.2 有序列表orderlist  
  
~~~html  
<ol type="A" start="4">  
    <li>1</li>    <li>2</li>    <li>3</li></ol>  
~~~  
  
* `type`是列表开用什么来表示序号`A`，`a`，`1`，`I`，`i`  
* `start`是列表由第几个开始  
* `li`里面可以随意放标签，但是`ol`里面只能防止`li`  
## 7.3 自定义列表divlist  
  
~~~html  
<dl>  
    <dt>可以是图片也可以是文字</dt>  
    <dd>相关文字</dd>  
</dl>  
  
<dl>  
    <dt>可以是图片也可以是文字</dt>  
    <dd>相关文字</dd>  
</dl>  
~~~  
  
一般都是写多份`dl`来工作，有序和无序列表都是多个`li`  
  
# VIII.图片标签  
  
* 正斜杠和反斜杠都是可以使用的  
* 注意相对路径和绝对路径，**常用相对路径**  
    * `./`是同级文件夹内  
    * `../`是上一级文件夹内  
  
~~~html  
    <img src="C:\Users\code\code.png">    <img src="./code.jpg">    <img src="../code.jpg">  
~~~  
  
添加属性对图片进行设置  
  
~~~html  
<img src="./code.jpg" title="鼠标悬停上去之后的提示信息" alt="图片不显示之后(加载失败)的提示信息" width="200px" height="200px">  
~~~  
  
# IX. 超链接标签  
  
~~~html  
<a href="路径" title="鼠标放上去之后的提示信息" target="规定在何处打开文档">内容</a>  
~~~  
  
* target属性：规定在何处打开文档。  
    * `target="_self"`当前窗口打开（默认值）  
    * `target="_blnk"`新窗口打开  
  
~~~html  
<a href="./test1.html"></a>  
<a href="../test2.html"></a>  
~~~  
  
可以像图片一样加入相对路径  
  
~~~html  
<a href="http://www.baidu.com" title="去百度" target="_blank">  
    <img src="./BaiduLogo.jpg"></a>  
~~~  
  
内部插入图片，点击图片就可以跳转  
  
# X. table表格  
  
## 10.1 创建表格  
  
~~~html  
<table>  
    <tr>       <td>1</td>       <td>2</td>    </tr>    <tr>        <rd>3</rd>       <rd>4</rd>    </tr></table>  
~~~  
  
* `table`创建表格  
* `tr`表示行  
* `td`单元格  
  
## 10.2 表格属性  
  
* `<table>属性`  
    * 宽度 `width`（单位`px`或者`%`父元素的百分比）  
    * 高度 `height`（单位`px`或者`%`父元素的百分比）  
    * 边框 `border`  
    * 边框颜色 `bordercolor`  
    * 背景颜色 `bgcolor`  
    * 水平对齐 `align="left"`或`align="right"`或`align="center"`  
    * 单元格与单元格之间的间距`cellspacing="间距宽度"`  
    * 单元格与内容之间的空隙`cellpadding="空隙大小"`  
* `行tr属性`  
    * 高度 `height`  
    * 背景颜色 `bgcolor`  
    * 文字水平对齐 `align="left"`或`align="right"`或`align="center"`  
    * 文字垂直对齐 `valign="top"`或`valign="middle"`或`valign="bottom"`  
* `单元格td属性`  
    * 宽度 `width`(一个单元格设置了宽度，影响一整列的宽度)  
    * 高度 `height`（一个单元格设置了高度，影响一整行的高度）  
    * 背景颜色 `bgcolor`  
    * 文字水平对齐 `align="left"`或`align="right"`或`align="center"`  
    * 文字垂直对齐 `valign="top"`或`valign="middle"`或`valign="bottom"`  
 ## 10.3 合并表格  
  
 `Colspan="所要名并的单元格的列数"`必须给td。  
  
 `Rowspan="所要合并的单元格的行数"`必须给td。  
  
 # XI. 表单标签  
  
 `<from><from>`表单  
  
 `<input/>`输入框  
  
* 属性 type 定义输入框的类型  
    * 文本框 `type="text"`  
    * 密码框 `type="password"`  
    * 提交框 `type="submit"`和`<button>提交按钮</button>`一样  
    * 按钮框 `type="button"`单纯的按钮  
    * 重置框 `type="reset"`清空的效果  
* 属性`placeholder`描述输入字段预期值的简短的提示信息。兼容到IE8以上。  
* 属性`name`必须设置，否则在提交表单时，用户在其中输入的数据不会被发送给服务器  
* 属性`value`  
  
~~~html  
    <form action="http://github.com" method="get">        用户名：<input type="text" placeholder="请输入用户名" name="username"/>  
        <br>        密码：<input type="password" placeholder="请输入密码" name="userpassword"/>  
        <br>        <input type="submit" value="登录">  
       <input type="reset" value="清空输入值">  
    </form>`  
~~~  
  
  
 输入11和11之后点击登录就会被带到地址上给后端  
  
 > https://github.com/?username=111&userpassword=111  
  
 一般不会这么写，应为这样数据会非常的不安全。可以使用`post`进行数据传输  
  
 Form当中method的post和get的别?  
  
1. get是从服务器上获取数据，post是向服务器传送数据。  
2. get是把参数数据队列加到提交表单的ACTION属性所指的URL中，值和表单内各个字段-一对应，在URL中可以看到。post是通过HTTP post机制，将表单内各个字段与其内容放置在HTMLHEADER内一起传送到ACTION属性所指的URL地址。用户看不到这个过程。  
3. 对于get方式，服务器端用Request.QueryString获取变量的值，对于post方式，服务器端用Request.Form获取提交的数据,  
4. get传送的数据量较小，不能大于2KB。post传送的数据量较大，一般被默认为不受限制。但理论上，IIS4(Internet Information Service 互联网信息服务)中最大量为80KB，IIS5中为100KB  
  
~~~html  
    <form action="http://github.com" method="post">        用户名：<input type="text" placeholder="请输入用户名" name="username"/>  
        <br>        密码：<input type="password" placeholder="请输入密码" name="userpassword"/>  
        <br>        <button type="submit">登录</button>  
       <button type="reset">清空输入值</button>  
    </form>  
~~~  
  
> http://github.com  
  
此时就看不到信息了，确保了数据安全。  
  
这里也用`<button>`来做按钮，效果是一样的  
  
~~~html  
<input type="button" value="普通按钮">  
~~~  
  
制作一个普通按钮，可以配合JS写自己的行为  
  
# XII.CSS样式表  
  
## 12.1 内部样式表  
  
1. 每个CSS样式由两部分组成，即选择符和声明，声明又分为属性和属性值  
2. 属性必须放在花括号中，属性与属性值用冒号连接  
3. 每条声明用分号结束  
4. 当一个属性有多个属性值的时候，属性值与属性值不分先后顺序,用空格隔开  
5. 在书写样式过程中，空格、换行等操作不影响属性显示  
  
~~~html  
<html lang="en">  
<head>  
    <meta charset="UTF-8">    <meta name="viewport" content="width=device-width, initial-scale=1.0">    <title>Document</title>    <style>       h1{          color: red;       }       h2{          color: yellow;       }    </style>    <style>       h3{          color: blue;       }    </style></head>  
<body>  
    <h1>1111111</h1>    <h2>2222222</h2>    <h3>3333333</h3></body>  
</html>  
~~~  
  
* `style`可以放在`head`和`body`里面，放在`head`里面可以提高代码的易读性。  
* `style`可以放多个，一个里面可以放多个选择符，如`h1`  
  
## 12.2 外部样式表  
  
2种CSS外部样式表引入方法，优先使用link标签  
  
~~~html  
<head>      
    <!-- CSS外部引入方法1 -->    
    <link rel="stylesheet" type="text/css" href="./CSS/028.css">    
    <!-- CSS外部引入方法2 -->    
    <style type="text/css">    
        @import url("./CSS/028.css");    
</style>  </head>  <body>    
<h1>11111111111111</h1>  </body>  </html>  
~~~  
  
**link和import之间的差别**  
  
1. 本质的差别:link属于XHTML标签，而@import完全是CSS提供的一种方式。  
2. 加载顺序的差别:当一个页面被加载的时候(就是被浏览者浏览的时候)，link引用的CSS会同时被加载，而@import引用的CSS会等到页面全部被下载完再被加载。所以有时候浏览@import加载CSS的页面时开始会没有样式(就是闪烁)，网速慢的时候还挺明显。  
3. 兼容性的差别:@import是CSS2.1提出的，所以老的浏览器不支持，@import只有在IE5以上的才能识别，而link标签无此问题。  
  
## 12.3 行内样式表  
  
~~~html  
<div style="css代码"></div>  
~~~  
  
直接在标签里面写就可以了  
  
## 12.4 样式表的优先级  
  
行内样式表>内部样式表>外部样式表（就近原则）  
  
~~~css  
div{  
    color:red!important;}  
~~~  
  
加一个`!important`就是让被标记的成为最高优先级  
  
# XIII. 选择器  
  
要使用CSS对HTML页面中的元素实现一对一，一对多或者多对一的控制，这就需要用到CSS选择器  
  
## 13.1 标签选择器  
  
标签选择器范围太广，推荐使用类选择器  
  
~~~css  
div{  
    color:red;}  
~~~  
  
## 13.2 类别选择器  
  
~~~html  
<div class="top">11</div>  
~~~  
  
~~~css  
.top{  
    background-color:red}  
~~~  
  
## 13.3 ID选择器  
  
~~~html  
<div id="box">11</div>  
~~~  
  
~~~css  
#box{  
    width:100px}  
~~~  
  
一个id名称只能对应文档中一个具体的元素对象。(唯一性)  
  
## 13.4 通配符选择器  
  
~~~css  
*{  
    margin:0;    padding:0;}  
~~~  
  
主要用法就是清除所有元素的默认边距值和填充值;  
  
## 13.5群组选择器  
  
~~~css  
div,p,h1{  
    background-color:red}  
  
div,.box,h1{  
    background-color:red}  
~~~  
  
~~~html  
<div>背景色为红色</div>  
<p>背景色为红色</p>  
~~~  
  
提出公共代码，节约代码量  
  
## 13.6包含选择器（后代选择器）  
  
~~~css  
div p{  
    background-color:red}  
~~~  
  
~~~html  
<div>  
    背景色为白色  
    <p>背景色为红色</p>  
</div>  
~~~  
  
## 13.7伪类选择器  
  
**语法:**  
  
1. `a:link{属性:属性值;}`超链接的初始状态;  
2. `a:visited{属性:属性值;}`超链接被访问后的状态;  
3. `a:hover{属性:属性值;}`鼠标悬停，即鼠标划过超链接时的状态;  
4. `a:active{属性:属性值;}`超链接被激活时的状态，即鼠标按下时超链接的状态;  
5. `Link--visited--hover--active.`（lvha）  
  
**说明:**  
  
1. 当这4个超链接伪类选择符联合使用时，应注意他们的顺序，正常顺序为`:a:link,a:visited,a:hovera:active`，错误的顺序有时会使超链接的样式失效  
2. 为了简化代码，可以把伪类选择符中相同的声明提出来放在a选择符中;例如：`a{color:red;} a:hover{color:green;}` 表示超链接的初始和访问过后的状态一样，鼠标划过的状态和点击时的状态一样  
  
~~~css  
    a:link{        color: yellow;    
    }    
    a:valid{    
        color: red;    
    }    
    a:hover{    
        color:green;    
    }    
    a:active{    
        background-color: orange;    
}    
~~~  
  
## 13.8选择器权重  
  
选中的是同一个元素，且都为他当多个选择器，们定义了样式，如果属性发生冲突了，会选择权重高的来执行  
  
~~~  
!important           最高优先级（慎用）  
内联样式                1，0，0，0，0  
包含选择器            0，1，0，0，0  
id选择器               0，0，1，0，0  
类和伪类选择器       0，0，0，1，0  
元素选择器            0，0，0，0，1  
通配符选择器           0，0，0，0，0  
继承的样式            没有优先级（最低）  
~~~  
  
# XIV.文本属性  
  
## 14.1 字体大小  
  
单位是px，浏览器默认是16px，设计图常用字号是12px  
  
~~~css  
.p1{    
font-size: 16px;  }  
~~~  
  
## 14.2 字体  
  
当字体是中文字体、英文字体中有空格时，需加双引号  
多个字体中间用逗号链接，先解析第1个字体，如果没有解析第2个字体,以此类推  
  
~~~css  
.p2{    
font-family:"Microsoft YaHei UI Light","Microsoft New Tai";  }  
~~~  
  
## 14.3 文字颜色  
  
~~~css  
p{    
    color: white;    
    color: #ffffff;    
    color: rgb(255,255,255);    
color: rgba(255,255,255,0.5);  }  
~~~  
  
rgba相比rgb添加了透明度控制  
  
## 14.4 文字加粗  
  
~~~css  
p{    
font-weight: bolder;  更粗的  
    font-weight: bold;  加粗  
    font-weight: normal;  常规  
}  
~~~  
  
## 14.5 文字倾斜  
  
~~~css  
p{    
font-style: italic;  斜体字  
    font-style: oblique;  倾斜的文字  
    font-style: normal;  常规显示  
}  
~~~  
  
## 14.6 文本水平对齐  
  
~~~css  
.box{    
    text-align: center;    
    text-align: left;    
    text-align: right;    
    text-align: justify;  
}  
~~~  
  
text-align: justify;  2端对齐，多行文本中才生效  
  
## 14.7 行高  
  
~~~css  
.box{    
    line-height: 50px;    
    height: 50px;    
    width: 800px;    
    text-align: center;    
background-color: red;  }  
~~~  
  
行高和高度设置一样，配合文本居中就是在box的中心位置  
  
多行文本不能这么设置  
  
## 14.8 文本间距  
  
~~~css  
.p1{    
    letter-spacing: 20px;    
word-spacing: 20px; }  
~~~  
  
每个字符或者词语之间的间隔距离  
  
## 14.9 首行缩进  
  
~~~css  
.box{    
    text-indent: 32px;    
text-indent: 2em; }  
~~~  
  
`text-indent`就是每段话前面空多少个像素，或者多少字符  
  
## 14.10 文本修饰线  
  
~~~css  
.box{    
    text-indent: 2em;    
text-decoration:none;    没有    
text-decoration:underline;   下划线    
text-decoration:overline;    上划线    
text-decoration:line-through;    删除线  }  
~~~  
  
## 14.11 文字大小写  
  
~~~css  
.box{    
text-transform: capitalize;   首字母大写  
    text-transform: lowercase;   全大写  
    text-transform: uppercase;   全小写  
}  
~~~  
  
## 14.12 文字缩写  
  
font是font-style，font-weight，font-size /line-height，font-family 的简写。顺序不能修改，里面直接写属性就可以了  
  
~~~css  
.box{    
font: italic bold 20px/2em "Microsoft New Tai";  }  
~~~  
  
# XV.列表属性  
  
`list-style-type`定义列表符合样式  
  
~~~css  
ul{    
    list-style-type: circle;    
    /*    
    disc实心圆    
    circle空心圆    
    none不显示    
     */  
}  
~~~  
  
`list-style-image`将图片设置为列表符合样式  
  
~~~css  
ul{    
list-style-image: url("****");  }  
~~~  
  
`list-style-position`设置列表标记的放置位置  
  
~~~css  
ul{    
    list-style-position: outside;    
    /*    
    outside列表外面，默认值    
    inside列表里面  
     */}  
~~~  
  
`list-style`简写  
  
~~~css  
ul{    
    list-style:none url("*") outside;  
~~~  
  
# XVI.背景属性  
  
## 16.1 背景颜色  
  
~~~css  
.box{    
background-color: orange;   }  
~~~  
  
## 16.2 背景图片的平铺  
  
~~~css  
.box{    
    background-image: url("./img/background_home.jpg");   
    background-repeat: repeat-x;  
    /*        repeat-x        repeat-y y轴平铺  
        no-repeat 不平铺  
    */    background-position: 10px 20px;  
    /*距离左边10px，顶部20px  
    */    background-position: center;    /*        center  
        left        right        top        botton        left center        right center        center center        .....       几个参数可以自由的搭配  
    */}  
~~~  
  
默认的背景效果是平铺效果  
  
## 16.3 背景图片的大小  
  
~~~css  
.box{    
    width: 800px;    
    height: 800px;    
    background-image: url("./img/background_home.jpg");    
      
    background-size: 800px 800px;     
    background-size: cover;    
    background-size: contain;  
}  
~~~  
  
* `background-size: 800px 800px`可能会导致图片被拉升改变比例  
* `background-size: cover`使图片覆盖组件，部分可能会被裁剪  
* `background-size: contain;`图片完整展示出来，不改变比例，可能出现留白  
## 16.4 背景图片的滚动和固定  
  
~~~css  
.box3{    
    width: 3000px;    
    height: 3000px;    
    background-image: url("./img/background_home.jpg");    
    background-repeat: no-repeat;    
    /*background-attachment: scroll; */  
    background-attachment: fixed;  }  
~~~  
  
`background-attachment: fixed; `相对于浏览器顶部进行了固定  
  
## 16.5 背景的复合属性  
  
~~~css  
.box{    
background: yellow url("") no-repeat center fixed;  }  
~~~  
  
除了backgound-size都可以无顺序的直接放在里面  
  
后面的属性会覆盖前面的属性  
  
# XVII.浮动属性  
  
1. 定义网页中其它文本如何环绕该元素显示  
2. 让竖着的东西横着来排列  
  
~~~css  
.box{  
    float:left;    float:right;    float:none}  
~~~  
  
* "见缝插针"，先填满一排  
* 文字会在里面游动  
  
~~~css  
.box{  
    Clear: none; /*允许有浮动对象*/  
    Clear: right; /*不允许右边有浮动对象*/  
    Clear: left; /*不允许左边有浮动对象*/  
    Clear:both; /*不允许有浮动对象*/  
}  
~~~  
  
清除浮动只是改变元素的排列方式，该元素还是漂浮着，不占据文档位置  
  
# XVIII.盒子模型  
  
## 18.1 内边距  
  
~~~css  
.box{  
    padding:30px;/* 一个值就是4个方向都一样 */    padding-left:20px 30px;/* 上下20px，左右30px*/  
    padding-left:20px 30px 40px;/* 上20px，左右30px，下40px*/  
    padding-left:10px 20px 30px 40px;    /* 上10px，右20px，下30px，左40px 顺时针方向*/  
}  
~~~  
  
特点  
  
* 背景色蔓延到内边距  
* 可以设置单一方向  
  
~~~css  
.box{  
    padding-left:20px;    padding-right:20px;    padding-top:20px;    padding-bottom: 20px;}  
~~~  
  
## 18.2 边框  
  
  
## 18.3 外边距