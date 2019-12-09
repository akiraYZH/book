## display: flex;

## flex-direction: 控制主轴和交叉轴的方向
* row 默认值  主轴方向从左往右
* row-reverse 将主轴切换到右边,从右往左
* column 将主轴方向切换到上边,从上往下
* column-reverse 将主轴方向切换到下边,从下往上

## flex-wrap  指子元素是否换行
* nowrap   强制在一行显示,即使大家需要缩小占地面积
* wrap     子元素会遵守自己的盒子模型,进行布局

## justify-content: flex-start;
* justify-content 水平对齐方式
* flex-start 左对齐
* flex-end    右对齐
* center 居中
* space-between 将多余空间划分给所有子元素的子中间
* space-around 将多余空间划分给所有子元素的子四间

## align-items   垂直方向的对齐
* flex-start    交叉轴的开始位置 
* flex-end    交叉轴的结束位置
* center 居中  交叉轴的中间位子
* baseline     以第一行文字基线对齐
* stretch      默认值,使得所有子元素等高* table-cell

## align-content   垂直方向的对齐(针对多行)
* flex-start    交叉轴的开始位置 
* flex-end    交叉轴的结束位置
* center  交叉轴的中间位置
* stretch 默认值,使得所有子元素等高* table-cell
* space-between 将多余的空间划分给所有子元素的中间
* space-around 将多余的空间划分给所有子元素的四周

## order: 3 
* 调整子元素顺序
## flex-grow: 1 
* 指父元素多余的空间按比例给予子元素 */
## flex-shrink: 0 
* 默认值为1, 当父元素宽度不足以容纳时,按比例进行缩小

## flex-basis: 600px;
* 设置宽度,优先级俾width高