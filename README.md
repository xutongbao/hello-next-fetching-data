Toast
===========

[![Version](https://img.shields.io/npm/v/toast-xu.svg)](https://www.npmjs.com/package/toast-xu)
[![Build Status](https://travis-ci.org/xutongbao/toast.svg?branch=master)](https://travis-ci.org/xutongbao/toast)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](https://www.npmjs.com/package/toast-xu)

A simple JavaScript toast for web.

Install with [npm](https://www.npmjs.com/), [Bower](https://bower.io/), or [Yarn](https://yarnpkg.com/):

npm:
```sh
npm install toast-xu --save
```

Bower:
```sh
bower install toast-xu --save
```

Yarn (note that `yarn add` automatically saves the package to the `dependencies` in `package.json`):
```sh
yarn add toast-xu
```

Use with [Node.js](https://nodejs.org/en/), [Browserify](http://browserify.org/), or [webpack](https://webpack.github.io/):

## Examples

Hello World!:
```js
let myToast = new Toast('hello world!');
myToast.show();
```

New Hello World!:
```js
let myToast = new Toast('hello world!');
myToast.show('new hello world!');
```

setTimeout:
```js
let myToast = new Toast();
myToast.show('new hello world!');
setTimeout(function () {
	myToast.hide();
}, 2000);
```

destory():
```js
let myToast = new Toast();
myToast.show('new hello world!');
setTimeout(function () {
	myToast.destory();
}, 2000);
```

custom style:
```js
let myToast = new Toast({
	text: 'hello world!',
	class: {
		toast: 'm-toast',
		toastInner: 'm-toast-inner',
		toastText: 'm-toast-text'
	}
});

myToast.show();
```

html str content:
```js
let myToast = new Toast({
  html: '<div style="line-height:100px;font-size:50px; color:#f66f0c;">Toast</div>'
});
myToast.show();
```

dom content:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width,height=device-height">
  <title>demo07(dom_content)</title>
  <style>
  </style>
</head>
<body>
<div id="m-toast" style="line-height:100px;font-size:50px; color:#f66f0c;">Toast</div>
<script src="../dist/bundle.js"></script>
<script>
let dom = document.getElementById('m-toast');
let myToast = new Toast({
  html: dom
});
myToast.show();
</script>
</body>
</html>
```

tpl content:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width,height=device-height">
  <title>demo08(tpl_content)</title>
  <style>
  </style>
</head>
<body>
<script type="text/html" id="m-toast-tpl">
	<div style="line-height:100px;font-size:50px; color:#f66f0c;">Toast</div>	
</script>
<script src="../dist/bundle.js"></script>
<script>
let dom = document.getElementById('m-toast-tpl').innerHTML;
let myToast = new Toast({
  html: dom
});
myToast.show();
</script>
</body>
</html>
```

delay:
```js
let myToast = new Toast({
	text: 'hello world!',
	delay: 1000
});
myToast.show();
```

## License

[MIT](LICENSE). Copyright (c) 2018 Xu Tongbao.
