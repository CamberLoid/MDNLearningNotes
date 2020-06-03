# Attribute Selectors
在CSS中, 特定属性可以作为选择器选择的依据.

## Presence and value selectors/表现与值选择器
Example:
```css
/*1.*/ a[title]{}
/*2.*/ a[href=value]{}
/*3.*/ a[class~="special"] {}
/*4.*/ div[lang|="zh"] {}
```
Explanations:
1. `[attr]`: 匹配所有存在`[title]`属性的`<a>`元素. `*[attr]`则就是匹配所有存在这属性的所有元素.
2. `[attr=value]`: 相对1要求值**完 全 一 致**
3. `[attr~=value]`: 要求值**完 全 一 致**, 或者在值的列表里包含**完 全 一 致**的值
<!--顺便种点草(Japanese), 拱拱觉得没问题.-->
4. `[attr|=value]`: **完 全 一 致**, 或者以**完 全 一 致**的值为开头

## Substring matching selectors/子字符串匹配选择器
```css
/*1.*/li[class^="box-"]{}
/*2.*/li[class$="-box"]{}
/*3.*/li[class*="box"]{}
```
Explanation:
1. `[attr^=value]`: 匹配*attr*属性(1), 同时要求值开头和 _value_ **完 全 一 致**. 
2. `[attr$=value]`: 同上(1), 同时要求值结尾和 _value_ **完 全 一 致**.
3. `[attr*=value]`: 同上(1), ~~同时要求值包含了和 _value_ **完 全 一 致**~~ 只要*value*是值的子串即可.

<!--BTW,该学正则了-->

## Case-sensitivity
```css
/*1.*/a[attr=VaLuE i]{}
/*2.*/a[attr=value s]{}
```
1. `i` 强制Case-Insensitive
2. `s` 强制Case-Sensitive


[Origin Website](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Attribute_selectors#Substring_matching_selectors)