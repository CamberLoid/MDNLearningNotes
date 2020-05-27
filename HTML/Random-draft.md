---
---

# Getting Started with HTML from MDN

## Anatomy

HTML 元素/elements 是由 标签/Tags 和 内容 组成

### Nesting elements

Nesting is a element is placed within other elements.  

Example:  
`<p>My cat is <strong>very</strong>grumpy</p>`
<p>My cat is <strong>very</strong>grumpy</p>

Nesting tags **should** be open and close correctly, as First in First out, or browser may be confused.

### Block-level & Inline-level elements

These are ~~two important fundamental~~ categories of elements in HTML.

> HTML5 has redefined elements categories. See https://developer.mozilla.org/zh-CN/docs/Web/Guide/HTML/Content_categories

- 块元素在页面中以块的形式展现, 通常用于表示结构化内容.
- Block-level elements **wouldn't** be nested by Inline-level elements, but can be nested by another block-level elements.
- Inline elements are those contained within a block-level elements.
- Inline elements often surround small parts of content.
- Inline elements would not cause a new line.

### Empty elements/空元素/Void element(Sometimes)

这类元素没有关闭标签, 通常用于嵌入/插入  
如`<img> <input>`

## Attributes

<p class="Example_Attributes">Like this</p>

An attribute should have:
- A space between it and the element name (or the previous attribute, if the element already has one or more attributes).
- The attribute name, followed by an equal sign.
- An attribute value, with opening and closing quote marks wrapped around it.

### Example:
`<a href="https://camber.moe">`

常用的属性:
- `href` 声明超链接的指向
- `title` 附加信息, 在指针停留时显示
- `target` 用于指定链接如何呈现, 如`target="_blank"`可以使网页在新标签显示

### 布尔属性

Examples: 
`<input disabled>`

