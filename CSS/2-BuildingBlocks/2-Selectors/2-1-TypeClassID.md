# Type, Class and ID selectors
这些是最简单, 最常见的选择器
## Type selectors
Type -> HTML Tag name or element selector
It selects HTML tag/element in document.  
**The Simplest Selector!!!**

## The Universal Selector
It is indicated by an asterisk `*` and selects everything (inside its parent element(or `<body>`)).

### Using The Universal Selector to Make Selectors more readable

```css
article :first-child{}
/*Might be confused with*/ article:first-child{}
/*To avoid*/ article *:first-child{}
```
<!--没看懂 暂时Pass-->
<!--现在看懂了-->
[Origin](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Type_Class_and_ID_Selectors#Using_the_universal_selector_to_make_your_selectors_easier_to_read)  
[Pseudo-Class/Elements Refer URL](./2-3-Pseudo-Class-Element.md)

## Class selectors
Starts with `.` and will select all element applied with the class. `.highlight{}`  


### Class on Particular Elements
`(Element Tag).(Class) {}`. 就这. 

### More Than one Class
Simple: use multiple full-stop dots.

Plain Example:
```css
/*Below selectors match the HTML document*/
.highlight.green{}
.highlight{}
.green{}
``` 
```html
<span class="green highlight"></span>
```

[Active Example](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Type_Class_and_ID_Selectors#Target_an_element_if_it_has_more_than_one_class_applied)

## ID Selectors
An ID Selector begins with `#`
Example:
```css
#one{}
h1#heading{}
```

> An ID has high specificity and will **overrule** most other selectors. This can make them **difficult** to deal with. In most cases **it is preferable to add a class** to the element rather than use an ID

