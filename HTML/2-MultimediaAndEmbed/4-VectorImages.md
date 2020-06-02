# Vector graphics
In short: Vector images have small file sizes and are highly scalable.
## What are?
Basically there are two types of image:
- Raster images. They are defined by grid of pixels.
- Vector images. They are defined by algorithms.

## SVG

## Adding SVG
### Using <img>
```html
<img 
    src="equilateral.svg" 
    alt="triangle with all three sides equal"
    height="87"
    width="100" />
```
#### Pros
- Quick, Familiar image syntax.
- Easy hyperlinks.
- The SVG file can be cached by the browser.
#### Cons
- Cannot manipulate(操纵) image with JS
- If you want to control the SVG content with CSS, you must include inline CSS styles in your SVG code
- Cannot restyle the image with CSS *pseudoclasses*

### Inline SVG
```html
<svg width="300" height="200">
    <rect width="100%" height="100%" fill="green" />
</svg>
```
#### Pros
- Saves HTTP Request;
- Able to assign with `class` and `id` and style them with CSS.
- The only approch to use *CSS interactions*
#### Cons
- Extra SVG Codes.
- Cannot be cached by browsers, which may cause perfomance costs.
- May include fallback in a `<foreignObject>` element

### Using <iframe>
Not recommended.
```html
<iframe src="triangle.svg" width="500" height="500" sandbox>
    <img src="triangle.png" alt="Triangle with three unequal sides" />
</iframe>
```
