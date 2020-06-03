# Pseudo-Class&Pseudo-Element/伪类和伪元素
恩, 很多.
## Pseudo-Class
A selector that select elements which is in a specific state.  
按**逻辑关系**选择(而非属性/元素/类/啥的)  
<!--Apply classes on element based on algorithm?
    Need further dig.-->
A pseudo-class's keyword: `:pseudo-class-name` / `:`. Priority=10.

### Simple Example
```css
.first{} /*HTML对应元素使用此类, Hard to maintain*/
article p:first-child{} /*选中article中, 是第一个Child的p, Readable and Maintainable*/
```

#### Some other Examples
同时还有 `:last-child`, `:only-child`, `:invalid`等常用伪类.

- `element:last-child` 选中同时是**最后一个**儿子的element
- `element:only-child` 选中同时是**唯一一个**儿子的element
- `invalid`: 用于`<input>`和`<form>`元素, 当输入无效时应用样式.

### User-action Pseudo-classes
这类伪类样式只在用户作出相应动作时应用. 

样例:
- `a:hover`: 用户鼠标悬浮在超链接上时, 应用样式.
- `a:visited`: 用户已经访问过时, 应用样式.

## Pseudo-Element
*Act as if adding a whole new HTML element into the markup.*  
关键字: `::Pseudo-element-name` / `::`. Priority=1.

Example:
```css
article p::first-line{} /*对第一行应用样式*/
```

## Combining Pseudo-Class&Pseudo-Element
```css
article p:first-child::first-line
```
## Generating content using ::before & ::after
`::before`和`::after`可以用于在元素前后增加内容. 
```css
/*添加文字内容*/
.box::before{
    content: "The BEFORE Content";
}
/*绘制一个紫色方块*/
.box2::before{
    content: "";
    display: block;
    width: 100px;
    height: 100px;
    background-color: rebeccapurple;
    border: 1px solid black;
}
```

[About `content` property](https://developer.mozilla.org/en-US/docs/Web/CSS/content) (MDN Docs/Web/CSS/content)

> Note: CSS 生成内容还有个`quote`属性. Example:
> ```css
> q {quotes: '"' '"' "'" "'";}
> q::before {content: open-quote;}
> q::after {content: close-quote;}
> ```
> 也可以通过在HTML中指定`lang`属性实现自动Quote.

## Other Pseudo-class/element
太长, 看这里: [Reference section](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements#Reference_section)

以及[另写了一个md](./2-3-1-PseudoReference.md)