# APlayer

[![npm](https://img.shields.io/npm/v/aplayer.svg?style=flat-square)](https://www.npmjs.com/package/aplayer)
[![npm](https://img.shields.io/npm/l/aplayer.svg?style=flat-square)](https://www.npmjs.com/package/aplayer)
[![devDependency Status](https://img.shields.io/david/dev/DIYgod/aplayer.svg?style=flat-square)](https://david-dm.org/DIYgod/APlayer#info=devDependencies)
[![npm](https://img.shields.io/npm/dt/aplayer.svg?style=flat-square)](https://www.npmjs.com/package/aplayer)
[![Travis](https://img.shields.io/travis/DIYgod/APlayer.svg?style=flat-square)](https://travis-ci.org/DIYgod/APlayer)

Wow, such a beautiful html5 music player

## Introduction

UI 参考网易云音乐外链播放器

[Demo](https://www.anotherhome.net/file/APlayer)

Screenshot
![image](https://i.imgur.com/JDrJXCr.png)
![image](https://i.imgur.com/eIRyqvT.png)

## Install

```
$ npm install aplayer
```

## Usage

### HTML

```HTML
<link rel="stylesheet" href="APlayer.min.css">
<!-- ... -->
<div id="player1" class="aplayer"></div>
<!-- ... -->
<script src="APlayer.min.js"></script>
```

### JS

```JS
var ap = new APlayer({
    element: document.getElementById('player1'),
    narrow: false,
    autoplay: true,
    showlrc: false,
    music: {
        title: 'Preparation',
        author: 'Hans Zimmer/Richard Harvey',
        url: 'http://7xifn9.com1.z0.glb.clouddn.com/Preparation.mp3',
        pic: 'http://7xifn9.com1.z0.glb.clouddn.com/Preparation.jpg'
    }
});
ap.init();
```

#### Options

```JS
{
    element: document.getElementById('player1'),                       // Optional, player element
    narrow: false,                                                     // Optional, narrow style
    autoplay: true,                                                    // Optional, autoplay, not supported by mobile browsers
    showlrc: false,                                                    // Optional, show lrc
    music: {                                                           // Required, music info
        title: 'Preparation',                                          // Required, music title
        author: 'Hans Zimmer/Richard Harvey',                          // Required, music author
        url: 'http://7xifn9.com1.z0.glb.clouddn.com/Preparation.mp3',  // Required, music url
        pic: 'http://7xifn9.com1.z0.glb.clouddn.com/Preparation.jpg'   // Required, music picture
    }
}
```

#### API

+ `ap.init()`
+ `ap.play()`
+ `ap.pause()`

### With lrc

Using [LRC format](https://en.wikipedia.org/wiki/LRC_(file_format))

HTML:

```HTML
<link rel="stylesheet" href="APlayer.min.css">
<!-- ... -->
<div id="player1" class="aplayer">
    <pre class="aplayer-lrc-content">
        [ti:平凡之路]
        [ar:朴树]
        [al:《后会无期》主题歌]
        [by:周敏]

        [00:00.00]平凡之路 - 朴树
        [00:04.01]作词：韩寒 朴树
        [00:08.02]作曲：朴树 编曲：朴树
        [00:12.02]徘徊着的 在路上的
        [00:17.37]你要走吗
        [00:23.20]易碎的 骄傲着
        [00:28.75]那也曾是我的模样
        <!-- ... -->
    </pre>
</div>
<!-- ... -->
<script src="APlayer.min.js"></script>
```

JS:

Option: `showlrc: false`

## Development

```
$ npm install
$ npm install -g gulp
$ gulp
```

## Todo

- [x] 播放进度拖拽控制
- [x] 音量控制
- [x] 分享到微博
- [x] 加载样式及错误处理
- [x] 窄样式 及 移动版样式
- [x] 歌词展示
- [x] 默认选项
- [x] 移动端兼容性
- [ ] 播放列表

## Issues

- [ ] 在 Firefox 中调整进度后, 播放到最后时音乐总时间会自动变长
- [ ] 移动端各种浏览器触发事件的时机不同
- [ ] 移动版 Safari 和 部分 Android 浏览器不支持 volume
- [ ] 部分 Android 浏览器不支持 duration


## LICENSE

MIT © [DIYgod](http://github.com/DIYgod)