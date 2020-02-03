# 定时器

* setTimeout(()=>{}, 1000)
* setInterval(()=>{}, 1000)

```
var count =0;
var time = 1000;//16.67
setTimeout(print, time);
function print(){
    console.log('怪物弹珠');
    if(time>200){
        time+=1000;
    }
    if(++count<5){
        setTimeout(print, time);
    }
            
}
```
# Date
```
var date = new Date();
new 实例化
console.log(date);
console.log(date.getFullYear());
console.log(date.getMonth());//少一个月
console.log(date.getDate());
console.log(date.getDay());
console.log(date.getHours());
console.log(date.getMinutes());
console.log(date.getSeconds());
console.log(date.getTime());
```

# Array
```
var arr = [123,true,null,undefined,function(){}{'name':'bluej'}];
// var arr1 = new Array();
arr.push('string');
arr.unshift('我是从前面插进去');
var arr_0 = arr.shift();
var arr_last = arr.pop();

var arr_2to3 =arr.slice(2,3); //不会改变原数组, 获取,开始下标,结束下标, 不包括结束下标
var arr_2_2 = arr.splice(2,2,'我是补位1', '我是补位2') // 改变原数组, 截取和替换, 截取下标, 长度

        
console.log(arr);
```

# String
```
var str1 = '山羊上山, 山碰山羊角';
var str2 = '水牛过河, 水没水河腰';

console.log(str1.indexOf('山',1));
//如果找到则返回下标, 否则返回-1
//第二参数是指开始寻找的下标

console.log(str1.lastIndexOf('山'));
//从尾部开始找, 如果找到返回下标, 下标顺序不变

console.log(str1.substr(3,4));
//获取, 开始下标, 长度, 不获取最后一位

console.log(str1, substring(4,6));
//开始下标,结束下标

var str3 = str1.replace(/山/g,'三');
//不会影响原来字符串
console.log(str3);
console.log(str1);
        
var arr = str1.split('');
// 切割成为数组

sort()方法 默认从小到大, 如果需要从大到小, 使用reverse()方法就可以了. sort方法是按照unicode编码排序的

arr.join('');
//数组转回字符串
```