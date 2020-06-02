# Video&Audio
This page only discuss native solutions.
## Video
The `<video>` element allows one to embed a video easily. This is a native *HTML5* solution.  

Example: 
```html
<video src="path-to-video" controls>
    <p> Browser doesn't support HTML5 Videos</p>
</video>
```
- `src`: The source of resource.
- `controls`: ???
- `<p>` inside `<video>`: Fallback content. Useful when browser doesn't support.

### Multiple format support
简单的说, 不同环境下支持的多媒体格式不一样.  
为了达到多格式支持可以将`src`属性移除, 转而在`<video>`中使用`<source>`元素.  
Example code: 
``` html
<video controls>
    <source src="" type="">
    <source src="" type=""><!--Fallback media-->
    <p></p><!--Fallback text-->
</video>
```
其中`type`属性为视频的MIME Type. 这个属性非必须, 但是填了可以节约一部分浏览器寻找支持的资源.

Reference: https://developer.mozilla.org/zh-CN/docs/Web/HTML/Supported_media_formats

### Others `<video>` Features
- `width`&`height`: This is used to control the size of video
- `autoplay`: Will make multimedia content play immediately. Not recommend.
- `loop`: Will cause media content play loop.
- `muted`: Will cause media content mute by default
- `poster='URL/To/Image'`
- `preload=values`: used for buffering large files. Will come with 3 values.
  - `none`: does not buffer.
  - `auto`: buffers the media file.
  - `metadata`: buffers only the metadata.

### The `<audio>` element.
Typical example:    
```html
<audio controls>
    <source src="" type="">
    <source src="" type=""><!--fallback format-->
    <p></p><!--fallback content-->
</audio>
```

The `<audio>` doesn't support the `width/height` attributes, as well as `poster`.

## Video Text Tracks/VTT/字幕
The HTML5 native solution is use [WebVTT](https://developer.mozilla.org/en-US/docs/Web/API/Web_Video_Text_Tracks_Format) file format and `<track>` element.

HTML Example:
```html
<video controls>
    <source 后略>
    <track kind="subtitles" src="path/to/vtt" srclang="en">
</video>
```
