# DOM
## DOM可将任何HTML文档描绘成一个由多层次节点构成的结构
* 元素节点
* 属性节点
* 文本节点
* 注释节点

1. 获取节点标签
* `document.querySelector();`完全支持css3选择器, 按照文档流获取第一个符合选择器的标签
* `document.querySelectorAll();` 获取的是一个NodeList(节点列表)
* `document.getElementById();` 通过ID获取元素, 获取的产物是元素节点, 按照文档流顺序获取第一个符合ID的标签
* `document.getElementsByClassName()`; //通过class类名获取元素, 获得的是HTMLCollection(标签集合), 不是数组. 不论数量多少, 都是以标签集合的形式展示
* `document.getElementsByName();` //通过name属性获取元素, 获得的是NodeList(节点列表), 不论数量多少, 都是以节点列表的形式展示. 可以通过forEach方法绑定事件.
* `document.getElementsByTagName();` //通过标签名获取元素, 获得的是HTMLCollection(标签集合), 不是数组. 不论数量多少, 都是以标签集合的形式展示
2. 绑定事件
3. 触发事件后所执行的事情

# 找儿子
* web.childElementCount; //获取孩子的数量
* web.childNodes;   从节点的角度获取孩子
* web.children; 从标签的角度获取孩子
* web.firstChild; 从节点的角度获取第一个孩子
* web.firstElementChild; 从元素标签的角度获取第一个孩子
* web.lastChild 从节点的角度获取最后一个孩子
* web.lastElementChild; 从元素标签的角度获取最后一个孩子
# 找兄弟
* nextElementSibling 下一个兄弟节点
* previousElementSibling 上一个兄弟节点
# 找父亲
* parentElement
* parentNode 
#
* classList;
    * add();
    * remove();
    * toggle();
    * supports();
    * contains();
* className;
#
* document.querySelector('div').getAttribute('data-id');//以字符串的形式进行输出
* document.querySelector('div').dataset.id;//dataset以json的形式进行输出
#
* console.log(div.innerHTML); //能够读取和识别标签
* console.log(div.innerText); //只能读取和识别内容
* `div.innerHTML= '<h1>'+ (++div.innerText)+'</h1>';`
#
* nodeName
# 增加节点
* innerHTML+=; 注意如果内容里元素是否绑定过事件, 如果用innerHTML增加子节点, 会把事件清除
* appendChild() 是从最后添加
* insertBefore(要插入的子节点, 在谁之前) 从指定元素之前插入
# 删除节点
* removeChild(aLi[5]);
# 替换节点
* replaceChild(li, aLi[2]); 替换指定元素