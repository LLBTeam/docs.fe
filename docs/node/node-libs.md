## Node 常用模块&扩展包

### Node 常用模块

* [基本模块](https://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000/001434501482448f6b36071ab6949d3a7ecb5a71a3c9df9000)
* [fs](https://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000/001434501497361a4e77c055f5c4a8da2d5a1868df36ad1000)
* [stream](https://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000/001434501515527e6fce6d5ec4b4fd9b572122cd1ec8ded000)
* [http](https://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000/0014345015296018cac40c198b543fead5c549865b9bd4a000)
* [crypto](https://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000/001434501504929883d11d84a1541c6907eefd792c0da51000)

### Node 扩展包

* [mysql](https://github.com/mysqljs/mysql)
* [grpc](https://blog.csdn.net/qq_31989047/article/details/79139710)
* [socket.io](https://socket.io/get-started/chat/)
* [request](https://www.cnblogs.com/liuchuanfeng/p/6686009.html)

有了这个模块，http请求变的超简单。同时支持https和重定向。

```javascript
var request = require('request');
request('http://www.google.com', function (error, response, body) {
  if (!error && response.statusCode == 200) {
    console.log(body) // 打印google首页
  }
})
```
* [cookie-parser](https://github.com/expressjs/cookie-parser)

是Express的中间件，用来实现cookie的解析，是官方脚手架内置的中间件之一。

* [body-parser](https://github.com/expressjs/body-parser)

是非常常用的一个express中间件，作用是对post请求的请求体进行解析。
