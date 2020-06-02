# Images in HTML
## Images
`<img>` 是一个 Void Element.

```html
<img src=""
    alt=""
    width="" height=""
    title="">
```
### Attributes
- `<src>`: 标注图片的来源. 可以是相对路径, 也可以是绝对路径.
- `<alt>`: 替代文本. 在图片加载失败时, 或是使用屏幕阅读器时有帮助. 
- `<height>` and `<width>`: 定义图片的两个属性.
- `<title>`: 图片的标题. 在鼠标移动到上面时显示信息. 

## Annotate image/图片注解
### Solution 1/Non-semantic
```html
<div class="figure">
    <img>
    <p></p>
</div>
```
It could be nicely styled by CSS, but there is no semantic.

### Solution 2/Semantic
Use `<figure>` and `<figurecaption>` elements.
```html
<figure>
    <img>
    <figcaption></figcaption>
</figure>
```

## CSS Background images
By using this:
```css
p {
    background-image: url("images/whatever");
}
```