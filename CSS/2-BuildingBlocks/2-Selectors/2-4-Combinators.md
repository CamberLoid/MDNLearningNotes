# Combinators/关系选择器/组合器

## Descendant Combinator/后代组合器
`.first .last{}` Select when  `.first` is `.last`'s ancestor.  
也就是后着是前者的后代/前者是后者的祖先. 

```css
.box p{color:red;}
```
```html
<div class="box"><p>Selected</p></div>
<p>Not selected</p>
```

## Child Combinator/子代组合器
`A > B`: Keyword `>`
Similar to descendant combinator, but select direct child(**NOT grand-child**)  
也就是只选择直接儿子而不选择儿子的儿子等.

```css
ul > li {border-top: 5px solid red}
ul li {border-bottom: 3px }
```

## Adjacent Sibling Combinator/相邻兄弟组合器
Keyword: `+`; Syntax: `A + B{}`
Select B when B is **right next** to A, and at the same level.

## General Sibling Combinator/通用兄弟组合器
Keyword: `~`; Syntax: `A ~ B{}`
Select ALL B when B is **after**(在A前面不行) A at the same level.  

## Using Combinators
略/Pass

<!--EOF-->