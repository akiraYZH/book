# ES5
* ECMA标准
    * 语法、语句、关键字、保留字、操作符、对象
    * 类型 number、string、boolean、null、undefined、obj(array、funcition、obj)
* DOM(操控页面标签)
* BOM(关于浏览器内容) 

## DOM(document object model 文档对象模型)
1. 获取页面目标元素对象
2. 绑定事件 给谁绑定 绑定什么
3. 触发事件时需要执行xxx操作

* 起名:
    1. 区分大小写
    2. 只能以英文、下划线、美元符$开头
    3. 其他位置可以是英文、下划线、美元符、数值构成
    4. 起名一定要有意义
    5. 避开关键字、保留字

* 类型
    * number `var num = 123` 
    * string `var str = '123'`
    * boolean `var is_true = true`
    * null `var is_null = null`
    * undefined `var is_unde= undefined`

    ## 判断变量是否为数值类型的方法
    1. 颜色判断法(人类快读识别)
    2. typeof 将变量类型输出

    ## 转换类型
    * Number() 只能转义纯数值类型, 遇到非数值类型时会直接提示NaN(not a number), 当遇到boolean值, 会发生隐形转换, true会变成1, false会变成0, 同时null转化成0,(undefined三个都会转化为NaN) parseInt和parseFloat倒不会.
    * parseInt() 专门用来转移成整数值, 从左往右寻找能转义的数值, 直到非数值类型结束, 如果没有找到则返回NaN. parseInt('1111011', 0);把二进制数值转义成十进制.
    * parseFloat() 专门用来转义成浮点数(带有小数的, 只能识别到第二个小点之前或者非数值类型结束),从左往右寻找能转义的数值, 直到非数值类型结束, 如果没有找到则返回NaN. 

    * toString() 
    * Boolean() 只有数字0, null, "", undefined, NaN为false.
    
* 语法、语句
* 操作符
   