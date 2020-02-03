# 介绍
* DOM对象
* 
## 注意:原生js和jq不能共用, 因为用jq获取的对象里会添加jq方法
## 获取节点
* $('');

## 绑定事件
# js:
```
        var js_li = document.querySelectorAll('li');
        js_li.forEach((li_obj, index, origin_node_list) => {
            li_obj.addEventListener('click',function(){
                console.log(index);
                console.log('我是li的点击事件');
                
                
            })
        });
```

# jq:
```
        $('li').on('click',function(){
            console.warn('jq:我是li的点击事件');
            
        });
```
# 将js选择的节点变为jq对象
```
var js_li = document.querySelectorAll('li');
$(js_li)
```
## 将jq对象变为原生js
```
var jq_li = $('li');
jq_li[0]
```
## $和JQuery可以互换