webpack react material-ui
===================================
webpack
-----------------------------------
```sh
npm install webpack -g
```


index.html
```sh
<html>
  <body>
  	<div id="example"></div>
    <script type="text/javascript" src="./bundle.js"></script>
  </body>
</html>
```
main.jsx
```sh
var React = require('react');
var ReactDom = require('react-dom');
var RaisedButton = require('material-ui/lib/raised-button');
ReactDom.render(
  <div>
    <RaisedButton label="Default" />
  </div>,
  document.getElementById('example')
);
```
webpack.config.js
```sh
module.exports = {
  entry: './main.jsx',
  output: {
    filename: 'bundle.js'
  },
  module: {
    loaders:[
      { test: /\.js[x]?$/, exclude: /node_modules/, loader: 'babel-loader' }
    ]
  }
};
```
添加react和material-ui

```sh
npm react
```
```sh
npm material-ui
```
启动server
```sh
webpack-dev-server
```


[参照https://github.com/callman/material-ui](https://github.com/callemall/material-ui)
[参照https://github.com/ruanyf/webpack-demos](https://github.com/ruanyf/webpack-demos)
