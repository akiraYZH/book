# 水平居中
## text-align:center 针对与非块级元素的水平居中
* 针对子元素或者文本内容居中

    * left center right justify(两端对齐)
    * letter-spacing:文字间距
    * word-spacing:单词间距
    * text-indent:首行锁进

## margin:0 auto
1. 必须设置比父元素要小的宽度
2. 作用于目标标签
3. 必须是块级元素

# 垂直居中
* 直接通过line—height等于height, 只能针对一行文字或者非块级元素
* 针对多行文字时, 需要拿个标签装起来, 并且在要垂直居中的元素样式里重置行高
* 再在要垂直居中的元素样式里加上vertical-align: middle;
## 例子
    ```
    div{
        width:300px;
        margin:0 auto;
        /* 1. 必须设置比父元素要小的宽度
        2. 作用于目标标签
        3. 必须是块级元素 */
        height:300px;
        text-align: center;
        line-height: 300px;
        border:1px solid black;
        /* 直接通过line—height等于height, 只能针对一行文字或者非块级元素 */

    }
    div p{
        display: inline-block;
        line-height: 1.5em;
        vertical-align: middle;
        /* 针对多行文字时, 需要拿个标签装起来, 并且重置行高 */
    }
    ```