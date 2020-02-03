# DOM
* jq_ul.find('li'); //在后代不管多少层进行筛选
* jq_ul.children() //在自元素那一层进行筛选
* jq_lis[0].parent();//上一层父节点
* jq_lis[0].parents(); //所有父节点
* jq_lis[0].parentsUntil('body'); //到body的父节点(不含body标签)
* jq_lis.eq(0).siblings('li') 选择所有兄弟li元素(可以不传参, 排序没关系)
* next() 紧邻的兄弟元素(向后) next('li')限定类型
* nextAll() 向后的所有兄弟元素
* nextUntil() 先后的所有兄弟元素, 直到目标元素停下

* prev()
* prevAll()
* prevUntil()

* addBack(): $('li.third-item').nextAll().addBack() 把自己加到选中范围中

# 插入
## append, appendTo: 
1. 要插入的个数
2. 要插入的节点是否已经存在
### 内部插入
* `jq_ul.append('<li>son</li>','<li>son2</li>');` 能插入多个
* `$('<h2>I am h2</h2>').appendTo(jq_div);` 只能一次
* `.prepend()`
* `.prependTo()`
---
### 外部插入
* `jq_div.after('<h2>I am h2</h2>');` 外部插入, 作为兄弟元素插入
* `.before()`
---
### html, text
* `jq_div.html('<h2>I am h2</h2>');` 加入一个节点
* `jq_div.text('<h2>I am h2</h2>');` 加入一个文本节点
---
### wrap 外部包裹
* `jq_h1.wrap('<div></div>');` 分别用包
* `jq_h1.wrapAll('<div></div>');` 一个大容器包着
* `jq_h1.wrapInner('<div></div>');` 包着里面
* `unwrap()` 去掉包裹

---
### 复制clone
* `jq_lis.eq(0).clone(true);`里面参数为true时, 可连同绑定的事件和子元素内容一并复制
---
### 替换
* `jq_lis.eq(0).replaceAll('h1');`
* `replaceWith()`
---
### 移除
* `.remove([selector])` jq_lis.eq(0).remove();
* `.empty()` 清空内容
* `.detach([selector])` 效果和remove一样,但有个返回值,可保存被删掉的节点绑定的事件(detach和remove的区别点在于是否保留事件)

