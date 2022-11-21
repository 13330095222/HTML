# HTML
HTML的基本使用

## HTML的基本结构
```
<!-- 文档类型声明，便于浏览器正确解析标签及渲染样式 -->
<!doctype html> 
<!-- HTML文档开始的标志 -->
<html> 
   <!-- 头部设置，可在head中设置网页标题，网页选项卡图标，引入外部的资源文件，设置网页相关信息等 -->
   <head>
       <!-- 设置网页标题，显示在网页选项卡上方 -->
       <title>网页标题</title>
       <!-- 设置网页字符编码 -->
       <meta charset="utf-8"> 
   </head>
   <!-- 网页主体部分，显示网页主要内容 -->
   <body> 
       网页主体内容
   </body>
</html>
```

## HTML的常用标签结构
|标签|介绍|描述|
|:-:|:-:|:-:|
|``<!doctype html>``|声明|便于浏览器正确解析标签及渲染样式|
|``<html></html>``|文档|用于HTML文档开头和结尾,在vscode 中输入!可以快速生成文档<br>使用方法：``!``|
|``<head></head>``|头部|可在head中设置网页标题，网页选项卡图标，引入外部的资源文件，设置网页相关信息等|
|``<title></title>``|网页标题|显示在浏览器窗口上|
|``<meta>``|标签|常用于指定网页的描述，关键词，SEO及其他设置|
|``<body></body>``|主体|网页显示的主要内容|
|``<h1></h1>``|一级标题|创建一级标题的标签,一般为居中显示<br>使用示例：``<h1 style="text-align: center">h1居中显示</h1>``|
|``<span></span>``|行分区|用于对特殊文本特殊处理<br>使用示例：``<span class=""></span>``|
|``<b></b>``|加粗|加粗标签<br>使用示例：``<b>加粗文本内容</b>``|
|````|||
|``<strong></strong>``|强调标签|效果同b标签<br>使用示例：``<strong>强调加粗文本内容</strong>``|
|``<label></label>``|文本标签|常与表单控件结合实现文本与控件的绑定<br>使用示例：``<label for="username">姓名：</label>``|
|``<i></i>``|斜体标签|常用文本的显示<br>使用示例：|
|``<u></u>``|下划线标签|常用文本的显示<br>使用示例：|
|``<hr>``|水平线标签|在页面中插入一条水平分割线<br>使用示例：|
|``<div></div>``|容器标签|常用于页面结构划分，结合CSS实现网页布局<br>使用示例：``<div id="top" class="header" style="..">页面顶部区域</div>``|
|``<img>``|图片标签|用于在网页中插入一张图片， src 用于给出图片的URL，必填。<br>title 用于设置图片标题，鼠标悬停在图片上时显示<br>alt 用于设置图片加载失败后的提示文本<br>使用示例：``<img src="" width="" height="" title="" alt="">``|
|``<a></a>``|超链接标签|超链接实现跳转至其他页面,[可以使用标签id作为锚点，跳转到页面指定位置](https://github.com/13330095222/HTML/edit/main/README.md#a)<br>target默认在当前窗口打开,可以设置新建窗口打开目标文本(取"_blank")<br>使用示例：``<a href="https://github.com/13330095222/HTML/edit/main/README.md#a" target="_self"></a>``|
|``<ol></ol>``|有序列表|默认使用阿拉伯数字标识每条数据|
|``<ul></ul>``|无序列表|默认使用实心圆点标识列表项|
|``<li></li>``|列表项|列表项,在vscode中快捷创建多个列表控件<br>快速创建使用示例：``ol>li*5``|
|``<table></table>``|表格标签|数据展示或辅助排版,border控制线条粗细，cellspacing控制间距<br>使用示例：``<table border="1px" cellspacing="0" width="" height="" style="text-align: center">``|
|``<tr></tr>``|行标签|创建行标签|
|``<td></td>``|单元格|创建单元格以显示数据，在vscode中快捷创建多个列表控件<br>快速创建使用示例：``table>td*5``<br>横向合并单元格：``<td colspan=""></td>``<br>纵向合并单元格：``<td rowspan=""></td>``|
|``<form></form>``|表单标签|表单用于采集用户的信息并提交给服务器<br>使用示例：``<form action="设置数据的提交地址" method="设置数据的提交方式，默认为get方式，可以设置为post" enctype="设置数据的编码类型，涉及二进制数据提交（例如图片，文件，音视频等），必须设置数据的提交方式为post,编码类型为"multipart/form-data"">提交数据</form>``|
|``<input>``|表单控件|用于采集用户信息，type设置控件类型可选：<br>``<input type="text">文本框``<br>``<input type="password">密码框``<br>``<input type="radio">单选按钮``<br>``<input type="file">文件上传``<br>``<input type="button"> 普通按钮``<br>``<input type="submit">  提交按钮``|
|``<select></select>``|下拉菜单|size 滚动菜单  multiple 多选<br>``<select name="addrss" id="" size="3" multiple>``|
|``<textarea></textarea>``|文本域 |文本框常用于留言板块<br>``<textarea name="" id="" cols="30" rows="10"></textarea>``|
|``&lt;``|转制<|在页面中呈现 ``<``|
|``&gt;``|转制>|在页面中呈现 ``>``|
|``&nbsp;``|转制空格|在页面中呈现一个空格`` ``|
|``&copy;``|转制版权|在页面中呈现版权符号``©``|

## 表单的简单示例
<table border="1px" cellspacing="0" width="300px" height="">
  <tr>
    <td>姓名</td>
    <td>年龄</td>
    <td>爱好</td>
  </tr>
  <tr>
    <td>wall</td>
    <td>20</td>
    <td>唱歌</td>
  </tr>
</table>

```
<table border="1px" cellspacing="0" width="300px" height="">
  <tr>
    <td>姓名</td>
    <td>年龄</td>
    <td>爱好</td>
  </tr>
  <tr>
    <td>wall</td>
    <td>20</td>
    <td>唱歌</td>
  </tr>
</table>
```
### 表单的合并示例
<table border="1px" cellspacing="0" style="text-align: center">
    <thead>
      <tr>
        <!-- th 专门用于表头 默认加粗居中 -->
        <th colspan="6">课程表</th>
      </tr>
    </thead>
    <tr>
      <td>星期</td>
      <td>一</td>
      <td>二</td>
      <td>三</td>
      <td>四</td>
      <td>五</td>
    </tr>
    <tr>
      <td rowspan="4">上午</td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <!-- <td></td> -->
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <!-- <td></td> -->
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <!-- <td></td> -->
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td colspan="6" style="text-align: center">午休</td>
      <!-- <td></td> -->
      <!-- <td></td> -->
      <!-- <td></td> -->
      <!-- <td></td> -->
      <!-- <td></td> -->
    </tr>
    <tr>
      <td rowspan="3">下午</td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <!-- <td></td> -->
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <!-- <td></td> -->
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
  </table>
  
  ```
  <table border="1px" cellspacing="0" style="text-align: center">
    <thead>
      <tr>
        <!-- th 专门用于表头 默认加粗居中 -->
        <th colspan="6">课程表</th>
      </tr>
    </thead>
    <tr>
      <td>星期</td>
      <td>一</td>
      <td>二</td>
      <td>三</td>
      <td>四</td>
      <td>五</td>
    </tr>
    <tr>
      <td rowspan="4">上午</td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <!-- <td></td> -->
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <!-- <td></td> -->
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <!-- <td></td> -->
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td colspan="6">午休</td>
      <!-- <td></td> -->
      <!-- <td></td> -->
      <!-- <td></td> -->
      <!-- <td></td> -->
      <!-- <td></td> -->
    </tr>
    <tr>
      <td rowspan="3">下午</td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <!-- <td></td> -->
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <!-- <td></td> -->
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
  </table>
  ```

## form表单控件的简单使用
```
<form action="" method="get">
  <!-- 表单控件 get：地址栏明文拼接  post:地址栏隐藏-->
    <div>
      <label for="username">姓名：</label>
      <input id="username" type="text" name="username" placeholder="请输入用户名" maxlength="10">
    </div>
    <div>
      <label for="userpassword">密码：</label>
      <input id="userpassword" type="password" name="userpassword" placeholder="请输入密码" maxlength="16">
      <!-- name设置控件名称，最终与值一并发送给服务器 placeholder设置输入框中的提示文本 maxlength设置输入框中可输入的最大字符数 -->
    </div>

    <!-- 单选框 -->
    <div>
      性别：
      <input id="boy" value="0" checked name="gender" type="radio">
      <label for="boy">男士</label>
      <input id="girl" value="1" name="gender" type="radio">
      <label for="girl">女士</label>
    </div>

    <!-- 复选框 -->
    <div>
      爱好：
      <input id="sing" value="sing" name="hobby" type="checkbox">
      <label for="sing">唱歌</label>
      <input id="dance" value="dance" name="hobby" type="checkbox">
      <label for="dance">跳舞</label>
      <input id="rap" value="rap" name="hobby" type="checkbox">
      <label for="rap">rap</label>
      <input id="ball" value="ball" name="hobby" type="checkbox">
      <label for="ball">篮球</label>
    </div>

    <!-- 下拉菜单 -->
    <div>
      地址：
      <!-- size 滚动菜单  multiple 多选-->
      <select name="addrss" id="" size="3" multiple>
        <option value="10001">北京</option>
        <option value="10002">上海</option>
        <option value="10003">深圳</option>
        <option value="10004">杭州</option>
        <option value="10005">武汉</option>
      </select>
    </div>

    
    <!-- 文件上传<div>
      头像：
      <input type="file" name="" id="">
    </div> -->


    <!-- 文本框<div>
      留言框：
      <textarea name="" id="" cols="30" rows="10"></textarea>
    </div> -->


    <div>
      提交：
      <!-- 提交按钮 -->
      <input type="submit" value="注册">
      重制：
      <!-- 重制按钮 -->
      <input type="reset">
    </div>

    <div>
      <input checked="checked" autocomplete="off" type="checkbox">用户协议
      <!-- checked 设置单选按钮或复选按钮的默认选中 -->
    </div>

    <div>
      普通按钮：
      <!-- 不含特殊功能按钮 -->
      <input type="button" value="普通按钮">
    </div> 
</form>
```

## 折叠博客文档功能示例
<details>
 <summary>简化整体结构，文档折叠功能示例</summary>
 <ol>
  <li>打印Hello World</li>
  <pre>print "Hello World"</pre>
 </ol>
</details>

```
<details>
 <summary>简化整体结构，文档折叠功能示例</summary>
 <ol>
  <li>打印Hello World</li>
  <pre>print "Hello World"</pre>
 </ol>
</details>
```

<p id="a">锚点</p>
