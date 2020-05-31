Refer to https://developer.mozilla.org/en-US/docs/Glossary/CSS_Selector

Consider this CSS:
```css
p {
  color: green;
}
div.warning {
  width: 100%;
  border: 2px solid yellow;
  color: white;
  background-color: darkred;
  padding: 0.8em 0.8em 0.6em;
}
#customized {
  font: 16px Lucida Grande, Arial, Helvetica, sans-serif;
}
```

There are three selectors.  
1. `p`: applies to all `<p>` elements
2. `div.warning`: applies to `<div>` elements with `warning` class
3. `#customized`: elements with id=customized