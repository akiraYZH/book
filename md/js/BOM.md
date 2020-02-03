# screen
* clientWidth, clientHeight
    * content—box: clientWidth = 宽度(css上写的)+左右padding
    * border-box: clientWidth=宽度(css上写的)-左右border
* clientTop, clientLeft
    * 元素边框宽度
* offsetWidth, offsetHeight
    * css所设定的宽高
* offsetTop = offsetLeft
    * 以浏览器的可视区域的左上角开始计算
* scrollHeight scrollWidth
    * 容器由内容撑大的实际高度, 滚动条里面内容的实际宽度和高度
* scrollTop(可赋值)
    * 顶部被覆盖的距离

# location
* hash 锚地值
* host 域名加端口
* hostname 域名
* href  域名(带参数)
* search 参数(?后面的)
* pathname 相对地址
* port 端口
* protocol 协议http;/https
* repload() 刷新
* replace() 
# history(历史记录)

* history.go(),
* history.back(),//后退一页
* history.forward()//前进一页
| 命令| 功能|
|:---|:---:|
|window.history.go(-1)；|//后退一页|
|window.history.go(-n)；|//后退n页|
|window.history.go(1)；	|//前进一页|
|window.history.go(n)；	|//前进n页|
|window.history.go(0);	|//刷新页面|

# cookies
* 存放4kb, 有时效性
* `document.cookie = 'name=melon; expires=Sun, 31 Dec 2020 12:00:00 UTC';`
## 函数:
```
function setCookie(cname, cvalue, exdays) {
	var d = new Date();
	d.setTime(d.getTime() + (exdays * 24 * 60 * 60 * 1000));
	var expires = "expires=" + d.toUTCString();
	document.cookie = cname + "=" + cvalue + ";" + expires + ";path=/";
}
```

# local storage
* 存放10mb, 没有时效性 
* `localStorage.setItem('name','melon');`
* `localStorage.getItem('name');`
* `localStorage.removeItem('name');`