# 事件
## 如果在z轴方向有后代元素时, 注意区别点
* mouseover, mouseout 支持事件冒泡: 如果z轴方向, 后代元素和绑定元素有重叠面积, 那么鼠标经过重叠边缘时也会触发事件, 如果没有重叠面积, 那么根据事件冒泡进行触发
* mouseenter mouseleave 不支持事件冒泡

* useCapture capture bubbling
* 改变事件触发方向, 不能阻止事件的传播
* 冒泡-》从内向外
* 捕获-》从外向内

* 阻止事件冒泡, 前提条件, 绑定同样的事件

* 'click'事件是由mousedown, mouseup, 完整触发时才视为一次click
* touchstart x_start的坐标
* touchend  x_end的坐标-x_start 正右负左
* touchmove 防抖节流