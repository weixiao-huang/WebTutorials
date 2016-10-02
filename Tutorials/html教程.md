# HTML Hello World
## 你的第一个HTML
### Hello world
在你电脑的任何一个目录中，右键新建一个文本文件，然后改名为`index.html`，之后用记事本打开，将以下代码复制粘贴到其中
```html
<!DOCTYPE html>
<html>
<head>
  <title>Hello World!</title>
</head>
<body>
  Hello World
</body>
</html>
```
然后保存，关闭文件，直接双击可以用默认浏览器打开，于是你实现了你的第一个html应用。

### 中文字符
尝试在上述代码的`<title>`和`</title>`或者`<body>`和`</body>`间添加中文，看看会出什么问题？如下所示
```html
<!DOCTYPE html>
<html>
<head>
  <title>SAEPA网页培训!</title>
</head>
<body>
  你好我叫蛤蛤
</body>
</html>
```
重新打开网站，你会发现，出现了乱码。这是因为我们没有指定文件的编码，网页文件利用了默认的编码来执行，而此编码不能很好的展现中文，因此我们必须指定编码，在`<head>`和`</head>`中间添加
```html
<meta charset="utf-8">
```
完整代码如下
```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>SAEPA网页培训!</title>
</head>
<body>
  你好我叫蛤蛤
</body>
</html>
```

## HTML中的其他元素
本节简单介绍一些html的元素，将下述代码复制进之前的`index.html`中
```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>SAEPA网页培训!</title>
</head>
<body>
  <h1>SAEPA萌萌哒</h1>
  <h2>今天来培训的人们萌萌哒</h2>
  <h3>这个标题是第三号的</h3>
  <h4>越来越小了</h4>
  <h5>更小了</h5>
  <h6>小到爆炸</h6>

  <p>这是一个段落</p>

  紧接着的是<span>一个行内版块</span>然后如果你什么也不会写他永远不会换行，除非加一个br<br>
  有没有看到换行？    然后   其  实  人家 对很多空格        也不  买账，要很多空格的话就需要加&amp;nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;你看，现在就有很多空格了吧

  <div>
    其实好多html里面都不太用上面的那些东西，可能用的比较多的就是各种div，反正你可以理解为div就相当于是把这些东西框起来的一个框框
  </div>
  <p>
    但是你仔细看的话就会发现，p和div其实是有行距差别的，不行你看看上下行距
    有没有发觉什么
  </p>

  <ul>one</ul>
  <ul>two</ul>
  <ul>three</ul>

  <li>one</li>
  <li>two</li>
  <li>three</li>

  <a href="https://www.baidu.com">通往你想去的网站</a>
</body>
</html>
```
其实上面说的很多东西，用得比较多的就属于`div`, `span`, `a`, `ul`, `li`了。
好，我们基础的html讲完了。

## HTML5相关知识以及其他额外知识
加入了更详细的块
```html
<header></header>
<footer></footer>
<main></main>
<nav></nav>
<section></section>
<article></article>
```
其他的知识，还有其他的例如button，或者input什么的，用的时候自行百度或者Google即可以得知用法。Html5支持很多特性，限于时间有限，就不给大家详细介绍了

## Sublime Text显神通
打开Sublime Text 3，在最上面的菜单栏中选择`View > Show`，然后下方出现命令窗口，将下述代码复制进去（记住一定要是Sublime Text 3而不是2）
```python
import urllib.request,os,hashlib; h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```
等待安装，片刻之后，重启Sublime，然后按`ctrl+shift+p`，可以看到跳出一个窗口，接着输入`install`，按`Enter`确定，然后又跳出一个窗口，输入`html`，点击`Enter`，便可以安装Sublime Text 3的html插件，让大家更爽的写html.