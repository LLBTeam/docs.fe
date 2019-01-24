# ECMAScript 6

<a href="http://es6.ruanyifeng.com/" target="_blank">阮一峰ECMAScript6入门</a>

## let和const命令
``` javascript
let a = 10;
// 它的用法类似于var，但是所声明的变量，只在let命令所在的代码块内有效。
// 存在暂时性死区
const b = 10;
// 声明一个只读的常量。一旦声明，常量的值就不能改变。
// 其实是不允许修改栈内存的值或者指针，指针指向的对象任然是可以修改的。
```

<a href="https://es6.ch-un.com/#letandconst" target="_blank">详细文档</a>

## 变量的赋值  结构赋值
``` javascript
//es5
let a = 1;
let b = 2;
let c = 3;

//数组的结构赋值
//es6，es6中尽量使用let替代var
let [a, b, c] = [1, 2, 3];

let [foo, [[bar], baz]] = [1, [[2], 3]];
foo // 1
bar // 2
baz // 3

let [ , , third] = ["foo", "bar", "baz"];
third // "baz"

let [x, , y] = [1, 2, 3];
x // 1
y // 3

let [head, ...tail] = [1, 2, 3, 4];
head // 1
tail // [2, 3, 4]

let [x, y, ...z] = ['a'];
x // "a"
y // undefined
z // []

//对象的结构赋值

let { foo, bar } = { foo: "aaa", bar: "bbb" };
foo // "aaa"
bar // "bbb"

let { baz } = { foo: "aaa", bar: "bbb" };
baz // undefined

let { foo: foo, bar: bar } = { foo: "aaa", bar: "bbb" };
```
<a href="https://es6.ch-un.com/#setValue" target="_blank">详细文档</a>

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


## String的扩展
``` javascript
for (let codePoint of 'foo') { console.log(codePoint) } 
// "f"
// "o" 
// "o"

includes() //返回布尔值，表示是否找到了参数字符串。
startsWith() //返回布尔值，表示参数字符串是否在原字符串的头部。
endsWith() //返回布尔值，表示参数字符串是否在原字符串的尾部。

let s = 'Hello world!';

s.startsWith('Hello') // true
s.endsWith('!') // true
s.includes('o') // true

repeat() //方法返回一个新字符串，表示将原字符串重复n次。
'x'.repeat(3) // "xxx"
'hello'.repeat(2) // "hellohello"
'na'.repeat(0) // ""
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

//参数默认值的位置

// 例一
function f(x = 1, y) {
  return [x, y];
}

f() // [1, undefined]
f(2) // [2, undefined])
f(, 1) // 报错
f(undefined, 1) // [1, 1]

// 例二
function f(x, y = 5, z) {
  return [x, y, z];
}

f() // [undefined, 5, undefined]
f(1) // [1, 5, undefined]
f(1, ,2) // 报错
f(1, undefined, 2) // [1, 5, 2]

```
<a href="https://es6.ch-un.com/#function" target="_blank">详细文档</a>

## 对象的新增方法

``` javascript
Object.assign()  // Object.assign方法用于对象的合并，将源对象（source）的所有可枚举属性，复制到目标对象（target）。

const target = { a: 1 };

const source1 = { b: 2 };
const source2 = { c: 3 };

Object.assign(target, source1, source2);
target // {a:1, b:2, c:3}

// Object.assign()方法实行的是浅拷贝，而不是深拷贝

// Object.assign() 返回一个数组，成员是参数对象自身的（不含继承的）所有可遍历（enumerable）属性的键名。

var obj = { foo: 'bar', baz: 42 };
Object.keys(obj)
// ["foo", "baz"]

// Object.values() 方法返回一个数组，成员是参数对象自身的（不含继承的）所有可遍历（enumerable）属性的键值

const obj = { foo: 'bar', baz: 42 };
Object.values(obj)
// ["bar", 42]

//Object.entries() 方法返回一个数组，成员是参数对象自身的（不含继承的）所有可遍历（enumerable）属性的键值对数组。

const obj = { foo: 'bar', baz: 42 };
Object.entries(obj)
// [ ["foo", "bar"], ["baz", 42] ]
```

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

## async函数

``` javascript
//async函数返回一个 Promise 对象，可以使用then方法添加回调函数。当函数执行的时候，一旦遇到await就会先返回，等到异步操作完成，再接着执行函数体内后面的语句。

function timeout(ms) {
  return new Promise((resolve) => {
    setTimeout(resolve, ms);
  });
}

async function asyncPrint(value, ms) {
  await timeout(ms);
  console.log(value);
}

asyncPrint('hello world', 50);


```