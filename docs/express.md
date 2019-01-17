#express
Express 是一个保持最小规模的灵活的 Node.js Web 应用程序开发框架，为 Web 和移动应用程序提供一组强大的功能。

##安装
``` shell
$ npm install express --save
```

## 文档
<a href="http://www.expressjs.com.cn/4x/api.html" target="_blank">官方文档</a>

##app.js
``` javascript
const express = require('express')
const app = express()

app.get('/', (req, res) => res.send('Hello World1!'))
app.listen(3000, () => console.log('Example app listening on port 3000!'))
```

##运行
``` shell
nodemon app.js
// 或
node app.js
```

##访问
浏览器访问<a href="http://localhost:3000" target="_blank">http://localhost:3000</a>