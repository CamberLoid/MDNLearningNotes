# CSS Box Model/CSS盒模型
CSS的每个东西都有那么一个盒子. 理解他*非常重要*(Mozilla说的).

## Block and Inline Boxes
和HTML类似, CSS Box也有Block和Inline之分.  
Box的类型由`display`属性定义.

Block box default behavior: `<display-outside>=block`
- A new line
- Fill the space available in the container
- `width` and `height` are **respected**
- `padding`, `margin` and `border` will push away other elements from the box.

Inline box default behavior: `<display-outside>=inline`
- No new line
- `width` and `height` will **not apply**
- **Vertical** padding/margin/border will apply but not cause pushing away. **Horizontal** (后略) will cause.

[`display` Property](https://developer.mozilla.org/en-US/docs/Web/CSS/display)

## Inner and Outer Display Types
Outer: 决定是Block还是Inline
Inner: 关于元素怎么展示.

在`display`的文档页有将其分为六个类型:`display:  [ <display-outside> || <display-inside> ] | <display-listitem> | <display-internal> | <display-box> | <display-legacy> ;`, 其中outside=outer, inside=inner

### Example
`display: flex`: Flexbox model/使用*弹性盒子布局*, 也就是平铺
`display: inline-flex`: a `<display-legacy>` value = `inline flex`

## What is CSS Box model
Block-level 使用完整的盒模型, 而Inline-level只使用部分.
盒模型**由里至外**分别为: Content - Padding - Border - Margin. [那个关于盒模型的图](https://media.prod.mdn.mozit.cloud/attachments/2019/03/19/16558/29c6fe062e42a327fb549a081bc56632/box-model.png)

- **Content**: 内容. 相关属性`width`, `height`.
- **Padding**: 内边距, 内容和边缘之间. 本身就是一个快速属性.
- **Border**: 边框. 同上.
- **Margin**: 外边距, 边缘外面的. 同上.

### Standard Box Model
```css
.box{
    width: 350px;
    height: 150px;
    margin: 10px;
    padding: 25px;
    border: 5px solid black;
}
```
符合拱拱的思维, Pass.

### Alternative Box Model
`width`和`height`为Content+Padding+border-size的总和.
声明`box-sizing: border-box;`即可.

## Margins, Padding, Borders
`margin`, `padding`, `border`均为简写/Shorthand.

### Margin/外边距
会把别的内容推出去. 可以赋正值和负值, 在某个方向上赋负值会让他盖过页面上别的东西.  
`margin`由`margin-top`, `margin-right`, `margin-bottom`, `margin-left`组成 

#### Margin collapsing/外边距折叠
两个外边距相接的元素, 他们的外边距将合为一个.  
若都为正则取最大, 反之相减.

### Padding/内边距
只能非负值. 所有背景都在内边距后面.  
`padding` is shorthand of `padding-top`, `padding-right`, `padding-bottom`, `padding-left`.

### Border/边框
`border` 用于一次设置四个边框
方向: `border-top`, 后略.
样式: `border-width`, `border-style`, `border-color`
方向+样式: `border-top-width`, 后略.

## Inline Boxes and Inline-block
`width`和`height`被忽略. 垂直内边距/Padding不会推开其他元素.

`display: inline-block;`可以让内联盒子的`width`和`height`应用, 同时垂直内边距/Padding也会推开其他元素

## Reference:
[MDN/Learn/The box model](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)  
[MDN/Learn/The box model/CHN](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/The_box_model)
[MDN/docs/CSS/Display](https://developer.mozilla.org/en-US/docs/Web/CSS/display) 
[Assessments](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Box_Model_Tasks)