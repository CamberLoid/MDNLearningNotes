# CSS Structure
## Apply CSS to HTML -2
### External stylesheet links
At `<head>`, using `<link rel="stylesheet" href="">`

### Inline stylesheet
At `<head>`, directly place stylesheet in`<style></style>`

### Inline style attributes
`<div style="">`. Not recommended. More common under certain occasions.  
Reasons:
- Least implementation of CSS for maintenance
- Mix CSS code with HTML code. Less readable.

## Selectors
Each CSS rule starts with a (list of) selector(s).  
Valid Examples:  
```css
h1{} a:link{} .manythings{}
#onething{} *{} .box p{} .box p:first-child{}
h1, h2, .intro{}
```
### 冲突: 后优先(Cascade)和特别优先(Specificity)
- Specificity: 更详细的声明优先
- Cascade: 后声明的优先
 
## Properties and values
一个合法的*声明(Declaration)*由属性和值组成: `color: blue;`  
多个在同一选择器下的声明组成CSS声明块(*CSS declaration block*), 声明块和选择器组成CSS规则集(*CSS ruleset/rule*)

若属性未知, 或是赋值不合法, 则声明无效. 该声明将被浏览器忽略. CSS语法拼写以美式英语为准.

### Functions
CSS有函数概念, 不过看起来不能用户自定义.
An example of `calc()`:
```css
.outer {
  border: 5px solid black;
}

.box {
  padding: 10px;
  width: calc(90% - 30px);
  background-color: rebeccapurple;
  color: white;
}
```
```html
<div class="outer"><div class="box">The inner box is 90% - 30px.</div></div>
```

另一个例子为`transform: rotate(0.8turn)`

## @rules/at-rules
CSS @rules provide instruction for what CSS should perform or how it should behave. 

部分样例: 
### @import
可以用`@import`快速在一个样式表中导入另一个样式表
### @media
被用于创建*media queries*, 该特性使用条件逻辑应用样式表.

## Shorthand Properties/速记属性
Some properties like `font`, `background`, `border`, `margin` are so called. They set several properties in a single line.

## Comments
Pass
## Whitespace
要有, 但不论多少当作一个处理. 

## Appendixes
[At-rules Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/At-rule)
[About media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries)