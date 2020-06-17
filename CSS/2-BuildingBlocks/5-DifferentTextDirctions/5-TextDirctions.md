# Text Directions / 文字书写方向

MDN很注意i18n这件事, 虽然窝这边主要只使用`horizontal-tb`...  
然而世界上总有国家用的是奇奇怪怪的书写方式.  
可以不需要那么认真.

## Writing modes
`writing-mode: ` [
- `horizontal-tb`, 水平, 从上往下
- `vertical-rl`, 垂直, 自左往右
- `vertical-lr` 垂直, 自右往左
]

## Writing modes and block/inline layout

一般情况下是Horizontal,  
如果切换到Vertical的话Inline维度和Block维度会调换.  
但是Width/height不会调换.

水平的情况:  
![](https://media.prod.mdn.mozit.cloud/attachments/2019/04/06/16574/e4f6ece210f6928bcbca0d6abd4d0d4f/horizontal-tb.png)

垂直的情况:  
![](https://media.prod.mdn.mozit.cloud/attachments/2019/04/06/16575/d9cb0009e49df85d9e99a76d79d4b2e7/vertical.png)

<!-- BTW, 如需自右到左, 使用`text-align`属性.  
上面写了之后会说这个的 -->

## Logical Properties&Values / 逻辑属性和逻辑值

由于一般情况下的`width`在垂直书写模式下不管用, 故引入逻辑属性/逻辑值概念. (或者叫相对变化/flow relative). 在逻辑值概念中,  
- `width` -> `inline-size`
- `height` -> `block-size`

Ref: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Logical_Properties

### Logical Margin/Border/Padding
替换以下属性的词
- `top` -> `block-start`
- `bottom` -> `block-end`
- `left` -> `inline-start`
- `right` -> `inline-end`

### Logical Values
`top` `bottom` `left` `right`可以作为关键字使用.  
他们的替代逻辑值是`block-start` `block-end` `inline-start` `inline-end`

## 所以, 用什么? / Summary
逻辑值适用于书写方式非一般情况的.  
对于大多数情况, 可能会更喜欢用绝对值/Physical Value.
这部分主要是用于更好理解CSS的. 
