# CSS
## css 按照getComputedStyle封装
`jq_li.eq(0).css('color')`
 ``` 
       $('li:odd').css({
            'fontSize':'36px',
            'collor':'#87ceeb'
        })
```
`jq_li.eq(0).css('color', 'fontSize')`
```
    <script>
        var jq_li = $('li'),
            js_li = document.querySelectorAll('li');
        jq_li.css('color', '#87ceeb');
        // console.log(jq_li.eq(0).css('color'));
        jq_li.css('fontSize', function(index, value){
            return parseInt(value)+index*4+'px';
        })
        
    </script>
```

## attr()
* s_h1.getAttribute('title') 获取
* jq_h1.attr('title', 'jq title') 赋值
* jq_h1.attr('title', function(index, value){}) 通过计算赋值

## prop() 可以选择默认值, attr只能选择行内已有
* jq_ins.prop('checked') 获得
* jq_ins.prop('checked',true); 赋值
# .removeAttr(attributeName) 
# .removeProp()

# val()
* val() 获得
* val(值) 赋值

# class
* jq_div.addClass('color_green font_48');
* jq_div.hasClass('color_green font_48');
* jq_div.removeClass('color_green font_48');
* jq_div.toggleClass('color_green font_48');
