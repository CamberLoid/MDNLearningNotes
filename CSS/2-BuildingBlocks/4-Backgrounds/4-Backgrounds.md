# CSS Background
[Origin](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Backgrounds_and_borders)

## Background

### Background Color
`background-color: color`. 属性只影响 Content.

### BG Images
基本食用方法: `background-image: <image>`
其中image=`url(url-to-image)`

#### Repeating
`background-repeat` = `no-repeat`/`repeat`/`repeat-x/y`

#### Sizing
`background-size`. 调整大小. 

<!-- MDN Ref background-size -->

[MDN Ref](https://developer.mozilla.org/en-US/docs/Web/CSS/background-size) 

只使用单个关键字: `contain` `cover`  
-> `background-size: contain / cover`
- `contain`: 收缩/拉伸后硬塞, 如果比例不对可能会有黑边. 
- `cover`: 使图片足够大, 以盖住盒子. 如果比例不对, 多出来的那部分就可能会在盒子外面

手动指定高/宽 `<length>`/`<percentage>` 或 `auto`: **都指定**或者**只使用一个**标记**宽度**的值(高为`auto`)  
`background-size: auto auto`

如果有多个背景, 那就直接按顺序**逗号分隔**叠加上去.  
`background-size: auto, auto`

<!-- 不往下写了 -->

#### Positioning
指定背景图像所处位置. `background-position`.

<!-- MDN Ref background-position -->

使用关键字: `top`等方向关键字(按'指定偏移量->0') 和`center`
指定坐标: `<length>` / `<percentage>`.
指定偏移量: 方向关键字+`length`/`percentage`: `bottom 10px`

如果有多个背景, 那就直接按顺序**逗号分隔**叠加上去. 

<!-- 不往下写了 -->


### Gradient BG
基本食用方法: `background-image: <gradient>`

<!-- MDN Ref <gradient> -->
[`<gradient> Ref`](https://developer.mozilla.org/en-US/docs/Web/CSS/gradient)

使用函数生成. 
- Linear gradient 线性渐变: `linear-gradient([规则],<color>,...,<color>)`
- Radial gradient 放射渐变: `radial-gradient(同上)`
- 重复: repeat-后略, 最后一个参数为<length>
- conic gradient 锥形渐变: FF不支持??

<!-- 不往下写了 -->

### Multiple BG
逗号分隔, 记得把其他修饰性属性跟上. 
当修饰性熟悉不足时, 会开始从头循环.   
前一个会叠在后一个上. 

### Background Attachment
`background-attachment` 定义背景如何跟着内容滚. 接受以下值:
- `scroll`: 不跟元素内滚, 页面滚动时跟着移动.
- `fixed`: 相对页面, 不滚. 
- `local`: 跟元素内滚, 跟页面移动.

例子: https://mdn.github.io/learning-area/css/styling-boxes/backgrounds/background-attachment.html
该属性之在滚动页面时生效

### Shorthand
以上内容都可以使用速记属性`background`实现. 需要注意的几点:
- `background-color`只能在最后一个逗号后
- `position`/`size`需要用斜杠`/`分隔, 且先方位后大小.

### Accessibility 
就, 就算有图也不要忘记设置背景颜色.


## Borders / 边框
Border有一堆速记属性. 包括方向(空格分隔样式)/样式(空格分隔方向)


### Rounded Corners / 圆角边框配置
可以拿来画圆角矩形(好文明)(划掉)  
`border-radius` : 一次全设置  
`border-top-right` / 后略 : 一次设置一个  
只有一个值时按圆半径处理, `: [rad]`  
两个值时先水平后垂直的椭圆处理.`: [horizon_rad] [vertical_rad]`

一个样例: 
```css
.box {
    border: 10px solid purple;
    border-radius: 1em;
    border-top-right-radius: 10% 30%;
}
```

