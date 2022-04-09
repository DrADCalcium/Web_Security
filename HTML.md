# HTML

+++

## VS Code使用

**语言编译器** ，支持目前流行的所有语言

### Web学习：

+ 插件：
  + vscode-icons：图标
  + Path Intellisense：路径补齐
  + HTML Snippets：HTML标签补齐
  + Beautify：代码格式修饰
  + Open In Browse：在浏览器内打开本地文件

+++

## HTML概述

超文本标记语言，通过浏览器进行渲染。

+++

## 文档结构

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

+++

## HTML标签

根据 **自身特点** 分类：

1. 有开始标签，有结束标签
2. 自身闭合标签

根据 **功能** 不同：

1. 行级标签：内容
2. 块级标签：布局

**常见标签：**

1. 标题标签

```html
<body>
    <h1>Title 1</h1>
    <h2>Title 2</h2>
    <h3>Title 3</h3>
    <h4>Title 4</h4>
    <h5>Title 5</h5>
    <h6>Title 6</h6>
</body>body
```

> **emmet语法：**
>
> `h1*6` 意为h1标签重复六次
>
> `$` 按数字降级
>
> `<!-- Comment -->` HTML注释

2. 段落标签（p标签）

```html
<p>Part 1</p>
<p>Part 2</p>
<p>Part 3</p>
```

3. 换行标签（br标签）

```html
Content 1 <br>
Comment 2 <br>
```

> 段落分割比换行的段间距更大

4. 分割线标签（hr标签）

```html
<hr>
```

5. 斜体标签（i标签）

```html
<i> Italic </i>
```

6. 粗体标签（b标签）

```html
<b> Bold </b>
```

7. 范围标签

**不会影响当前样式** ,对范围内的文本进行样式调整。

```html
<span> Content </span>
```

8. 列表标签

   + 无序列表 

   ```html
   <ul>
       <li> 张三 </li>
       <li> 李四 </li>
   </ul>
   ```

   > **emmet** 
   >
   > `ul>li{无序列表内容$}*3`

   + 有序列表

   ```html
   <ol>
       <li> 张三 </li>
       <li> 李四 </li>
   </ol>
   ```

   > **emmet** 
   >
   > `ol>li{Content $}*3`

   + 定义列表

   ```html
   <dl>
       <dt> 路由器</dt>
       <dd> 进行路由选路 </dd>
   </dl>
   ```

> **emmet**
>
> `dl>dt{Content 1}+dd{Content 2}`

9. 图片标签

```html
<img src="图片引用路径" alt="无法加载时显示文本" title="鼠标悬停时的注释文本"
```

10. 超链接标签

```html
<a herf="超链接引用位置" target="定义链接显示形式，覆盖显示/新窗口显示(new)"> Content </a>
```

11. 锚点超链接

+ 定义锚点

```html
<a name="锚点名"> 锚点 </a>
```

+ 引用锚点

```html
<a herf="(路径)#锚点名"> 锚点超链接 </a>
```

12. 布局标签

+ 表格标签

```html
<table width="" border="" height="">
    <tr>
        <td> 1.1 </td>
        <td> 1.2 </td>
    </tr>
    <tr>
        <td> 2.1 </td>
        <td> 2.2 </td>
    </tr>
</table>
```

+++

###### 【案例】静夜思

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <b>
        静夜思
    </b>
    <br>
    <span style="font-size: 10px;">
        作者：李白
    </span>
    <br>
    床前明月光，疑是地上霜。
    <br>
    举头望明月，低头思故乡。
</body>

</html>
```

+++

## 标签内的常用属性

+ id：标签唯一标识符，不同标签不能重复
+ class：类属性，可以相同
+ name：标签的名字，多用于form表单中的标签，后台语言会通过name属性获取value值
+ width：img专用，图片显示宽度
+ height：img专用，图片显示高度
+ border：table专用，表格边框粗细

#### form表单：收集前端数据；action：提交给后台的页面

+ input：文本输入框
+ textarea：文本域
+ select：下拉菜单
+ button：按钮
+ ……

```html
<form action="">
    <input type="text" name="" id="" placeholder="用户名">
    <br>
    <input type="password" name="" id="" placeholder="密码">
    <br>
    <input type="submit" value="提交注册">
</form>
```

#### method：提交方法

+ GET：安全系数不高，明文url传输

+ POST：安全系数高，密文传输

```html
<form action="post">
    <p>网络安全意识</p>
    <input type="checkbox" name="" id="">
    是否了解网络安全有关法律<br>
    <input type="checkbox" name="" id="">
    是否了解网络安全对自身影响<br>
    <p>是否学习过网络安全？</p>
    <input type="radio" name="1" id="">
    是 <br>
    <input type="radio" name="1" id="">
    否
    <!-- 利用name一致互斥做出单选 -->
    <p>选择你想要学习的时间</p>
    <select name="" id="">
        <option value="">1月</option>
        <option value="">2月</option>
        <option value="">3月</option>
        <option value="">4月</option>
        <option value="">5月</option>
        <option value="">6月</option>
        <option value="">7月</option>
        <option value="">8月</option>
        <option value="">9月</option>
        <option value="">10月</option>
        <option value="">11月</option>
        <option value="">12月</option>
    </select>

</form>
```

