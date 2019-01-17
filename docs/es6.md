# ECMAScript 6

## let和const命令
``` javascript
let a = 10;
const b = 10;
```

<a href="https://es6.ch-un.com/#letandconst" target="_blank">详细文档</a>

## 关于...参数
``` javascript
function add(...values) {
    for (var val of values) {
        console.log(val);
    }
}

add(2, 5, 3);
// 2
// 5
// 3

function add1(a,...values) {
    //a:2
    //values:[5, 3]
}

add1(2, 5, 3);


function push(array, ...items) {
  array.push(...items);
}

push([1,2,3],4,5,6)
//[1,2,3,4,5,6]


function add2(x, y) {
  return x + y;
}

add2(...[4, 38]) 
// 42
```
<a href="https://es6.ch-un.com/#rest" target="_blank">详细文档</a>

## 变量的赋值
``` javascript
//es5
let a = 1;
let b = 2;
let c = 3;

//es6，es6中尽量使用let替代var
let [a, b, c] = [1, 2, 3];
```
<a href="https://es6.ch-un.com/#setValue" target="_blank">详细文档</a>


## String的扩展
``` javascript
for (let codePoint of 'foo') { console.log(codePoint) } 
// "f"
// "o" 
// "o"
```
<a href="https://es6.ch-un.com/#string" target="_blank">详细文档</a>

## Function的扩展
``` javascript
function add(...values) {
  let sum = 0;

  for (var val of values) {
    sum += val;
  }

  return sum;
}

add(2, 5, 3) // 10

var f = () => 5;
// 等同于
var f = function () { return 5 };

var sum = (num1, num2) => num1 + num2;
// 等同于
var sum = function(num1, num2) {
  return num1 + num2;
};

```
<a href="https://es6.ch-un.com/#function" target="_blank">详细文档</a>

## Set和Map
``` javascript
var set = new Set([1, 2, 3, 4, 4])
set.size // 4
[...set]
// [1, 2, 3, 4]

set.add("4");
set.size // 5
[...set]
// [1, 2, 3, 4,"4"]

var m = new Map();
var o = {};

m.set(o, "content")
m.get(o) // "content"

m.has(o) // true
m.delete(o) // true
m.has(o) // false
```
<a href="https://es6.ch-un.com/#setandmap" target="_blank">详细文档</a>

## for...of循环
``` javascript
const arr = ['red', 'green', 'blue'];

for(let v of arr) {
  console.log(v); // red green blue
}
```
<a href="https://es6.ch-un.com/#iterator" target="_blank">详细文档</a>

## Promise
``` javascript
var promise = new Promise(function(resolve, reject) {
  // ... some code

  if (/* 异步操作成功 */){
    resolve(value);
  } else {
    reject(error);
  }
});

promise.then(function(value) {
  // success
}, function(value) {
  // failure
});
```
<a href="https://es6.ch-un.com/#generator" target="_blank">详细文档</a>

## class
``` javascript
//定义类
class Point {

  constructor(x, y) {
    this.x = x;
    this.y = y;
  }

  toString() {
    return '(' + this.x + ', ' + this.y + ')';
  }

}
```
<a href="https://es6.ch-un.com/#classmd" target="_blank">详细文档</a>

## module
``` javascript
// profile.js
let firstName = 'Michael';
let lastName = 'Jackson';
let year = 1958;
export default function crc32() {
  // ...
};

// main.js
import some from './profile';
some();
```
<a href="https://es6.ch-un.com/#modulemd" target="_blank">详细文档</a>