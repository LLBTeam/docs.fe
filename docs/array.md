#Array 对象

##语法
``` javascript
let a = [];
new Array();
new Array(size);
new Array(element0, element1, ..., elementn);
```
##描述
Array 对象用于在单个的变量中存储多个值。

##属性
<table class="dataintable">
  <tbody><tr>
    <th style="width:25%">属性</th>
    <th>描述</th>
  </tr>
  <tr>
    <td><a target="_blank" href="http://www.w3school.com.cn/jsref/jsref_length_array.asp" target="_blank">length</a></td>
    <td>设置或返回数组中元素的数目。</td>
  </tr>
  <tr>
    <td><a target="_blank" href="http://www.w3school.com.cn/jsref/jsref_length_array.asp" target="_blank">prototype</a></td>
    <td>在原型链上添加属性或者方法</td>
  </tr>
</tbody></table>

##方法
<table class="dataintable">
  <tbody><tr>
    <th style="width:25%">方法</th>
    <th>描述</th>
  </tr>
  <tr>
    <td><a target="_blank" href="http://www.w3school.com.cn/jsref/jsref_concat_array.asp">concat()</a></td>
    <td>连接两个或更多的数组，并返回结果。</td>
  </tr>
  <tr>
    <td><a target="_blank" href="http://www.w3school.com.cn/jsref/jsref_join.asp">join()</a></td>
    <td>把数组的所有元素放入一个字符串。元素通过指定的分隔符进行分隔。</td>
  </tr>
  <tr>
    <td><a target="_blank" href="http://www.w3school.com.cn/jsref/jsref_pop.asp">pop()</a></td>
    <td>删除并返回数组的最后一个元素</td>
  </tr>
  <tr>
    <td><a target="_blank" href="http://www.w3school.com.cn/jsref/jsref_push.asp">push()</a></td>
    <td>向数组的末尾添加一个或更多元素，并返回新的长度。</td>
  </tr>
  <tr>
    <td><a target="_blank" href="http://www.w3school.com.cn/jsref/jsref_reverse.asp">reverse()</a></td>
    <td>颠倒数组中元素的顺序。</td>
  </tr>
  <tr>
    <td><a target="_blank" href="http://www.w3school.com.cn/jsref/jsref_shift.asp">shift()</a></td>
    <td>删除并返回数组的第一个元素</td>
  </tr>
  <tr>
    <td><a target="_blank" href="http://www.w3school.com.cn/jsref/jsref_slice_array.asp">slice()</a></td>
    <td>从某个已有的数组返回选定的元素</td>
  </tr>
  <tr>
    <td><a target="_blank" href="http://www.w3school.com.cn/jsref/jsref_sort.asp">sort()</a></td>
    <td>对数组的元素进行排序</td>
  </tr>
  <tr>
    <td><a target="_blank" href="http://www.w3school.com.cn/jsref/jsref_splice.asp">splice()</a></td>
    <td>删除元素，并向数组添加新元素。</td>
  </tr>
  <tr>
    <td><a target="_blank" href="http://www.w3school.com.cn/jsref/jsref_toString_array.asp">toString()</a></td>
    <td>把数组转换为字符串，并返回结果。</td>
  </tr>
  <tr>
    <td><a target="_blank" href="http://www.w3school.com.cn/jsref/jsref_unshift.asp">unshift()</a></td>
    <td>向数组的开头添加一个或更多元素，并返回新的长度。</td>
  </tr>
  <tr>
    <td><a target="_blank" href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach">forEach()</a></td>
    <td>方法按升序为数组中含有效值的每一项执行一次callback 函数</td>
  </tr>
  <tr>
    <td><a target="_blank" href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/filter">filter()</a></td>
    <td>方法创建一个新数组, 其包含通过所提供函数实现的测试的所有元素</td>
  </tr>
  <tr>
    <td><a target="_blank" href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/map">map()</a></td>
    <td>创建一个新数组，其结果是该数组中的每个元素都调用一个提供的函数后返回的结果</td>
  </tr>
  <tr>
    <td><a target="_blank" href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/some">some()</a></td>
    <td>测试是否至少有一个元素通过由提供的函数实现的测试</td>
  </tr>
  <tr>
    <td><a target="_blank" href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/every">every()</a></td>
    <td>测试所有元素通过由提供的函数实现的测试</td>
  </tr>
   <tr>
    <td><a target="_blank" href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce">reduce()</a></td>
    <td>方法对数组中的每个元素执行一个由您提供的reducer函数，将其结果汇总为单个返回值</td>
  </tr>
</tbody></table>


##示例 forEach
``` javascript
var words = ["one", "two", "three", "four"];
words.forEach(function(word) {
  console.log(word);
});
// one 
// two
// three
// four
```

##示例 filter
``` javascript
var words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter(word => word.length > 6);

console.log(result);
// expected output: Array ["exuberant", "destruction", "present"]
```

##示例 map
``` javascript
var array1 = [1, 4, 9, 16];

// pass a function to map
const map1 = array1.map(x => x * 2);

console.log(map1);
// expected output: Array [2, 8, 18, 32]
```

##示例 some
``` javascript
var array = [1, 2, 3, 4, 5];

var even = function(element) {
  // checks whether an element is even
  return element % 2 === 0;
};

console.log(array.some(even));
// expected output: true
```

##示例 reduce
###语法
``` javascript
arr.reduce(callback[initialValue])
reduce为数组中的每一个元素依次执行callback函数，不包括数组中被删除或从未被赋值的元素，接受四个参数
```
+ accumulator 累计器
+ currentValue 当前值
+ currentIndex 当前索引
+ array 数组

``` javascript
[0, 1, 2, 3, 4].reduce(function(accumulator, currentValue, currentIndex, array){
  return accumulator + currentValue;
});
```
同
``` javascript
[0, 1, 2, 3, 4].reduce((prev, curr) => prev + curr );
```