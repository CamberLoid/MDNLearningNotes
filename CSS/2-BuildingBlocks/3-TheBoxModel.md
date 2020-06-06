# CSS Box Model/CSS盒模型
CSS的每个东西都有那么一个盒子. 理解他*非常重要*(Mozilla说的).

## Block and Inline Boxes
Similar to HTML, CSS also has two types of boxes: Block&Inline.  

Box type is defined by `display` property, and relate to the **outer** value of `display`.  
Accept value: `block`, `inline`.

Block box default behavior:
- A new line
- Fill the space available in the container
- `width` and `height` are **respected**
- `padding`, `margin` and `border` will push away other elements from the box.

Inline box default behavior:
- No new line
- `width` and `height` will **not apply**
- Vertical padding/margin/border will apply but not cause pushing away. Horizontal (后略) will cause.

