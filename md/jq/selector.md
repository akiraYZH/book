# Selector

## $( ":animated" )
* 选择所有正在执行动画效果的元素.
* $("div:animated")
## eq:作者自己写的,用来获取集合中的一个
* $('li:eq(0)') = $('li').eq(0)
    * 获取第一个元素
* $('li:eq(-1)')
    * 获取最后一个元素

## even odd: 注意和css标准选择方式不一样, jq是按照下标选择
`$('li:odd').css('fontSize','36px')`

## first last
`$('li:first').css('fontSize','36px')`
`$('li:last').css('fontSize','36px')`

## gt
`$('li:gt(1)')`
* 获取下标比1大的

## .is()
```
$("ul").click(function(event) {
  var $target = $(event.target);
  if ( $target.is("li") ) {
    $target.css("background-color", "red");
  }
});
```

## jQuery( ":empty" )
* $("td:empty") 选择所有空的td

## jQuery( ":header" )
* 选择所有标题元素，像h1, h2, h3 等.

## jQuery( ":last" )
* 选择最后一个匹配的元素。

## jQuery( ":contains(text)" )
* text: 用来查找的一个文本字符串。这是区分大小写的。

---
### filter
* `$('li').filter(':even').css('background-color', 'red');`
### not
* `$('li:not(:first-child)').css('background','red');`

### has
* `$('li').has('ul').css('background-color', 'red');` 如果li里包含ul就把背景设为红色

### is()

### 遍历
* .map( callback(index, domElement) ) 有返回值
* .each( function(index, Element) )

### .slice( start [, end ] )
* 开始下标不包括, 结束下标包含
