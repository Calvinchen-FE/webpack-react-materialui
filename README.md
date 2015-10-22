webpack react material-ui
===================================
webpack
-----------------------------------
```sh
npm install webpack -g
```

[参照grunt官网](http://webpack.github.io/docs/installation.html)

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



[参照https://github.com/callman/material-ui](https://github.com/callemall/material-ui)
