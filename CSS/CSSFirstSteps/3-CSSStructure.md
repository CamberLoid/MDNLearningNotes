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
Examples:
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
Will render as:<div class="outer" style='border: 5px solid black'><div class="box" style="padding: 10px;width: calc(90% - 30px);background-color: rebeccapurple;color: white;">The inner box is 90% - 30px.</div></div>

## @rules/at-rules