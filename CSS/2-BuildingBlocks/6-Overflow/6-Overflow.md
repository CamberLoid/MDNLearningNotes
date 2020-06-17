# Overflow / 溢出

当内容太多, 盒子装不下时, 就会导致溢出.  
处理溢出使用属性`overflow`.

## Overflow 属性

- `overflow: visible` 默认属性. 显示溢出的内容到盒子外.
- `overflow: hidden` 隐藏溢出的内容. 只在确认不会出事时使用.
- `overflow: scroll` `overflow: x-scroll` `overflow: y-scroll`  
  会有x, y方向的滚动条处理溢出的内容. 或者也可以指定只有某个轴
- `overflow: auto` 交给浏览器.

此外还有`word-break` 和 `overflow-wrap`等
- `word-break`: 指定怎么在单词内换行.
- `overflow-wrap`: 制定浏览器该在哪里插入换行符

### REF
https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Overflowing_content
[word-break](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow-wrap)
[overflow-wrap](https://developer.mozilla.org/en-US/docs/Web/CSS/word-break)

