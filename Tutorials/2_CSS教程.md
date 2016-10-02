# CSS教程
CSS代表了一种样式，相当于word中的排版，你可以利用CSS调节字体、颜色、背景、版式、甚至动画……
## HTML中使用CSS
### 方式一：直接内嵌
```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>SAEPA网页培训</title>
  <style type="text/css">
    h1 {
      color: gray;
    }
    p {
      color: #563d7c;
      background-color: #eee
    }
    div {
      color: #75b;
      margin: 50px 60px;
      padding: 96px 50px;
      background-color: #aaa;
    }
  </style>
</head>
<body>
  <h1>你好这是标题</h1>
  <p>你好这是一个段落</p>
  <div>你好这是一块东西</div>
</body>
</html>
```

### 方式二：分离
```html
// index.html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>SAEPA网页培训</title>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
  <h1>你好这是标题</h1>
  <p>你好这是一个段落</p>
  <div>你好这是一块东西</div>
</body>
</html>


// style.css
h1 {
  color: gray;
}
p {
  color: #563d7c;
  background-color: #eee
}
div {
  color: #75b;
  margin: 50px 60px;
  padding: 96px 50px;
  background-color: #aaa;
}
```
同样的效果

## HTML中的class与id
html中，我们看到很多DOM都有属性(Property)，这些属性可以作为css中的选择器
```html
// index.html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>SAEPA网页培训</title>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
  <h1 class="title">你好这是标题</h1>
  <p class="para">你好这是一个段落</p>
  <div id="block">你好这是一块东西</div>
</body>
</html>


// style.css
.title {
  color: gray;
}
.para {
  color: #563d7c;
  background-color: #eee
}
#block {
  color: #75b;
  margin: 50px 60px;
  padding: 96px 50px;
  background-color: #aaa;
}
```

## CSS中的相关方法
- hover伪选择器
- font的方法
- margin, padding, border的联系与区别，边框模型
- background-color, background-image
- text-align: center
- em, 百分比与px
- 链接样式：hover, link, visited, active。以及text-decoration。注意：a:hover 必须位于 a:link 和 a:visited 之后；a:active 必须位于 a:hover 之后
- css定位机制：static, relative, absolute, fixed
- [浮动效果](http://www.w3school.com.cn/css/css_positioning_floating.asp)
- inline, block