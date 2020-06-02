# CSS Getting Started

## Adding CSS to document
Use `<link rel="stylesheet" href="path/to/css">` inside `<head>` to link CSS and HTML.

## Styling HTML Elements
Selector's target can be a element. This will apply to all the element.  
Target multiple selectors at once is allowed.

## Changing the default behavior of elements
Browsers have its default stylesheets containing default styles.  
Example: 
```css
li {
    list-style-type: none;
}
```
## Adding a class
`class` is a global attribute of HTML elements. By specifying class in selector as `.some-class` it will match all element with this class.  

Adding a class attribute:`<div class="some-class">`  

In CSS: 
```css
.some-class {
    /*Will match all elements with this class*/
}
div.some-class{
    /*Will only match <div> elements with this class*/
}
```
## Style things based on location.
### Descendant Combinator/后代组合器
Simply takes the form of a space between two other selectors.Example:
```css
li em {
    color: purple;
}
```
This selector will select any `<em>` element inside (a descendant of) `<li>`

### Adjacent sibling combinator/相邻兄弟组合器
当第二个元素紧跟在第一个元素之后，并且两个元素都是属于同一个父元素的子元素，则第二个元素将被选中. 使用`+`标记
Example
```css
h1+p{
    font-size:200%;
}
```

## Style base on state/基于状态的样式
Example: `<a>`'s state can be:
- link
- visited
- hover
 
By using `a:link, a:visited, a:hover{...}`

## 组合组合器和选择器
Example:
```css
article p span{...}
h1+ul+p{...}
body h1+p .special{...}
```