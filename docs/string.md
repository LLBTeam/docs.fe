# String

## 初始化

``` javascript
let a = '';
let a = String('a');
```

## 属性

属性|概述|描述
-|-|-
length|表示一个字符串的长度|该属性返回字符串中字符编码单元的数量

```
var x = "Mozilla";
var empty = "";

console.log("Mozilla is " + x.length + " code units long");
/* "Mozilla is 7 code units long" */

console.log("The empty string is has a length of " + empty.length);
/* "The empty string is has a length of 0" */
```


## 方法

方法|概述|语法
-|-|-
<a href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String/charAt" target="_blank">charAt</a>|一个字符串中返回指定的字符|str.charAt(index)
<a href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String/concat" target="_blank">concat</a>| 将一个或多个字符串与原字符串连接合并，形成一个新的字符串并返回|str.concat(string2, string3[, ..., stringN])
<a href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String/indexOf" target="_blank">indexOf</a>|返回调用  String 对象中第一次出现的指定值的索引，开始在 fromIndex进行|str.indexOf(searchValue[, fromIndex])
<a href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String/split" target="_blank">split</a>|使用指定的分隔符字符串将一个String对象分割成字符串数组，以将字符串分隔为子字符串，以确定每个拆分的位置。|str.split([separator[, limit]])
<a href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String/substring" target="_blank">substring</a>|返回一个字符串在开始索引到结束索引之间的一个子集, 或从开始索引直到字符串的末尾的一个子集|str.substring(indexStart[, indexEnd])
<a href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String/substr" target="_blank">substr</a>|返回一个字符串中从指定位置开始到指定字符数的字符 | str.substr(start[, length])
<a href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String/substr" target="_blank">slice</a>|提取一个字符串的一部分，并返回一新的字符串|str.slice(beginSlice[, endSlice])
<a href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String/substr" target="_blank">toLowerCase</a>|将调用该方法的字符串值转换为小写形式，并返回。|str.toLowerCase()
<a href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String/toUpperCase" target="_blank">toUpperCase</a>|将调用该方法的字符串值转换为大写形式，并返回|str.toUpperCase()
<a href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String/toUpperCase" target="_blank">trim</a>|会从一个字符串的两端删除空白字符|str.trim()

