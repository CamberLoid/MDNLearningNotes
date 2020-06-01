<style>
    .Note{
        color: gray;
    }
</style>

# Cascade and Inheritance/层叠和继承

## Conflict rules/当发生冲突时
### Cascade
Stylesheets **cascade**: The later comes the first.
### Specificity
See below.
### Inheritance
Some CSS property values set on parent elements are inherited by their child elements, and some aren't.  
For example, `width` doesn't inherit.

## CSS Inheritance
Things like widths (as mentioned above), margins, padding, and borders do not inherit
### Controlling Inheritance
For detail, see: [MDN CSS/Cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/Cascade)

CSS provides four *special __universal__ property values* for controlling inheritance. Every CSS property accepts these valuse. They are:
- `inherit`: 继承, pass
- `initial`: Return to default value. See this: [MDN CSS/Initial_Value](https://developer.mozilla.org/en-US/docs/Web/CSS/initial_value)
- `unset`: Reset it to default. ~~等同于不设置~~  
- `revert` <span class='Note'>(New, not widely support)</span>: Rolling back. See this: [MDN CSS/revert](https://developer.mozilla.org/en-US/docs/Web/CSS/revert)

### Resetting all property values
CSS提供了一个特殊快速属性`all`, 可以被设置为特殊全局值之一。
Example:
```css
blockquote {
    background-color: red;
    border: 2px solid green;
}
        
.fix-this {
    all: unset;
}
```

## Priority/优先级
A rule's importance has three factors to consider.
1. Importance: By using `!important`
2. Specificity:
3. Source order : [Jump](#Cascade)

### Source order
=Cascade; 简单地说(x3): 后来优先

### Specificity
规则越详细越优先.  
规则拥有四个优先级: 
- Ones: Each **element** selector or **pseudo-element** contained inside the overall selector
- Tens: Each **class** selector, **attribute** selector, or **pseudo-class** contained inside the overall selector.
- Hundreds: Each **ID** selector contained inside
- Thousands: 直接写在HTML元素内的**Style属性**中
- 0: 全局选择器`*`和组合器`+ > ~ [空格]`和否定伪类`:not`不对特殊性造成影响

[MDN Specificity Reference](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#Understanding_the_cascade)

### !important
Can be used to override.
```css
.better {
    background-color: gray;
    border: none !important;
}
```
如上.  
只能通过`!important`来Override前面的`!important`, 说白了就是适用Cascade原则.  
> ~~老爹: 要用魔法打败魔法~~

在任何时候都不建议使用`!important`声明覆盖.
## The Effect of CSS location