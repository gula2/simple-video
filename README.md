![](https://badgen.net/badge/Editor.js/v2.0/blue)

# Simple Video Tool

Provides Video Blocks for the [Editor.js](https://editorjs.io).

Works only with pasted videos and URLs and requires no server-side uploader.


## Installation

### Install via NPM

Get the package

```shell
npm i --save-dev simple-video-editorjs
```

Include module at your application

```javascript
const SimpleVideo = require('simple-video-editorjs');
```

### Download to your project's source dir

1. Upload folder `dist` from repository
2. Add `dist/bundle.js` file to your page.

### Load from CDN

You can load specific version of package from [jsDelivr CDN](https://www.jsdelivr.com/package/npm/simple-video-editorjs).

`https://cdn.jsdelivr.net/npm/@editorjs/simple-video-editorjs@latest`

Then require this script on page with Editor.js.

```html
<script src="..."></script>
```

## Usage

Add a new Tool to the `tools` property of the Editor.js initial config.

```javascript
var editor = EditorJS({
  ...
  
  tools: {
    ...
    video: SimpleVideo,
  }
  
  ...
});
```

## Config Params

This Tool has no config params

## Tool's settings

1. Stretch to full-width
2. Add default HTML controls for playback
3. Enable autoplay and muted video.

## Output data

| Field          | Type      | Description                     |
| -------------- | --------- | ------------------------------- |
| url            | `string`  | video's url                     |
| caption        | `string`  | video's caption                 |
| autoplay       | `boolean` | video will autoplay             |
| muted          | `boolean` | video will be muted by defaul   |
| controls       | `boolean` | video should display default controls|
| stretched      | `boolean` | stretch video to screen's width |


```json
{
    "type" : "video",
    "data" : {
        "url" : "https://paul.kinlan.me/videos/2019-11-05--test-post-video-upload-0.mp4",
        "caption" : "An aweomse video",
        "autoplay" : false,
        "controls" : false,
        "muted": false,
        "stretched" : true
    }
}
```
