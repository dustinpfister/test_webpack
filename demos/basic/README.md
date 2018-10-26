# Basic Webpack example

For a basic webpack example I just have a single use of console.log in an index.js file in an src folder, and wish to have a main.js file in my dist folder.

## index.html
```html
<!doctype html>
<html>
  <head>
    <title>Getting Started</title>
    <script src="https://unpkg.com/lodash@4.16.6"></script>
  </head>
  <body>
    <script src="./dist/main.js"></script>
  </body>
</html>
```

## dist/index.js
```js
console.log('this is the index.');
```

I then just called npx webpack from the command line at the root path of this demo.

```
$ npx webpack src/index.js -o dist/build.js
```

this gives me a main.js file in my dist folder that looks like this:

```js
!function(e){var n={};function t(r){if(n[r])return n[r].exports;var o=n[r]={i:r,l:!1,exports:{}};return e[r].call(o.exports,o,o.exports,t),o.l=!0,o.exports}t.m=e,t.c=n,t.d=function(e,n,r){t.o(e,n)||Object.defineProperty(e,n,{configurable:!1,enumerable:!0,get:r})},t.r=function(e){Object.defineProperty(e,"__esModule",{value:!0})},t.n=function(e){var n=e&&e.__esModule?function(){return e.default}:function(){return e};return t.d(n,"a",n),n},t.o=function(e,n){return Object.prototype.hasOwnProperty.call(e,n)},t.p="",t(t.s=0)}([function(e,n){console.log("this is the index.")}]);
```

Totally killing a fly with a canon on this demo, but the basic idea of this is working. I get a build in my dist folder as expected.