# Website Structures
## Basic sections
- Headers
- Nav bar
- Main content
- Sidebar
- Footer
## HTML Structuring element
### HTML Layout element more detail
- `<header>`: 页眉
- `<nav>`: 导航栏
- `<main>`: 主要内容
  - `<article>`
  - `<section>`
- `<aside>`: 侧边栏, 常嵌套在`<main>`中
- `<footer>`: 页脚

### 无语义元素
They are `<div>`(block) and `<span>`(inline).  
They should be used with suitable `class` attribute.

### 换行和水平分割
They are `<hr>`(block) and `<br>`(inline).  
`<br>`会导致换行. 正如[1-Getting_Started](./1-Getting_Started.md#Whitespaces)所言, 多余的空格和换行会被浏览器忽略. 
`<hr>` 导致一条水平分割线.

