# Advanced Text Formatting
This topic less known elements
## Description Lists
```html
<dl>
    <dt> Item #1</dt>
    <dd> Description #1</dd>
    <!--It is permitted to have a single term with multiple descrptions-->
    <dd> Description #1.1</dd>
<dl>
```
## Quotations
### Blockquotes
Block-level quotes. Use `<blockquote>` to wrap.  
浏览器默认会将其渲染为缩进的段落以暗示这是Quote.

### Inline quotes
Inline level quotes. Use `<q>`to wrap.  
渲染时默认加上引号.

### Citations/引文
The `cite` attribute won't be displayed by browsers unless using Javascript or CSS to modify. A better way is using `<cite>` and `<a href>` elements.   
The `<cite>` element will rendered in italic font by default.

## Abbreviations/缩略
Use `<abbr title="wtf">` to wrap abbreviations.  
It will look like this: <abbr title="What the Fuck"> WTF </abbr>

## Contact details
Use `<address>`. Refer to [Next page](Introduction-6.md)

## Subscript and Superscript
Use `<sup>` and `<sub>`.

## Computer codes
There are a number of elements available.
- `<code>`: Marking up generic pieces of computer code.
- `<pre>`: For retaining [whitespace](Introduction-1.md#Whitespaces).
- `<var>`: Variable names.
- `<kbd>`: Keyboard inputs.
- `<samp>`: Outputs.

## Time and dates