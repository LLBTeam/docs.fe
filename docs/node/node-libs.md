## Node 常用模块&扩展包

### Node 常用模块

* [基本模块](https://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000/001434501482448f6b36071ab6949d3a7ecb5a71a3c9df9000)
* [fs](https://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000/001434501497361a4e77c055f5c4a8da2d5a1868df36ad1000)
* [stream](https://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000/001434501515527e6fce6d5ec4b4fd9b572122cd1ec8ded000)
* [http](https://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000/0014345015296018cac40c198b543fead5c549865b9bd4a000)
* [crypto](https://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000/001434501504929883d11d84a1541c6907eefd792c0da51000)

### Node 扩展包

* [mysql](https://github.com/mysqljs/mysql)
* [grpc]
* [socket.io]
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
* [cookie-parser]
* [body-parser]