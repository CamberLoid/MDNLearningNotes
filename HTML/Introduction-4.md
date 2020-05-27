# Hyperlinks

## What is?

## Anatomy of a link

```html
<p> This is a link to
<a href=""> Whatever</a></p>
```
The `href` is aka *Hypertext Reference* 

### Block-level links

Can turn any content into link. Like:
```html
<a href=""><img src='', alt=''></a>
```

## URL&Path
### Directories fundamental

跳过，Pass

### Document fragments

Can use this feature by specifying `id` Attributes and  `href='xxx#thatID'`.  
On same document can use `<a href=#thatID>` to jump to another part of document.

### Absolute/Relative URLs

Pass, 基本知识.

## Best Practices

### Clear link wording

- Good Example: `<p><a href="https://firefox.com/">  Download Firefox</a></p>`  
- Bad Example `<p><a href="https://firefox.com/">  Click here</a>to download Firefox</p>`
- Don't repeat URL as part of the link.
- Don't say "Link" or "Links to"
- Keep link table as short as possible.
- Minimize instance where multiple copies of same text are linked to different places.

### Use relative links wherever possible

- Easier to scan codes.
- Efficient for browsers.

### Non-HTML resources - Leave clear signposts

### Use Download attribute when linking to a download

It goes:
```html
<a href="link-to-download" doanload="that-file-name">
    Click to Download</a>
```

