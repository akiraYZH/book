# 伪类选择器
## p标签不能包含p标签, 浏览器会解析成另外一个p标签
* `p span:first-child`
    1. 找到页面中所有的p标签
    2. 通过关系选择符找到对应的标签元素(上面的例子就是p标签里面的所有后代span标签)
    3. 同时span标签要符合一个条件(必须是第一个子元素)
    * :fist-child(第一个子元素)
    * :last-child(最后一个子元素)


* `p del:first-of-type`
    1. 找到页面中所有的p标签
    2. 通过关系选择符找到对应的标签元素(上面的例子就是p标签里面的所有后代del标签)
    3. del标签寻找时是按照标签类型来分类的,所以可以找到第一个属于del类型的标签
    * :first-of-type(符合类型的第一个)
    * :last-of-type(符合类型的最后一个)
   

* `:nth-of-child()`, `:nth-of-type()`, `nth-last-of-child`, `nth-last-of-type`,单独控制一系列的同类型标签的其中某一个
    * :nth-of-child(2) 第二个子元素
    * `:nth-of-child(odd), :nth-of-child(2n+1)` 奇数
    * `:nth-of-child(even), :nth-of-child(2n)` 偶数


* ’*‘
* class .
* ID #
* 空格 包含选择符
* > 子选择符
* + 隔壁老王选择符
* ~ 陈浩南选择符
* :hover 鼠标移上去

# 伪对象选择器
## ::before, ::after
1. 必须要声明content属性 `content: "内容"`;
2. display默认是行内元素
3. 它是目标元素的子元素, 不是兄弟元素
* js是选择不了伪对象选择器的
