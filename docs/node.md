#nodejs 

##安装教程
<a href="http://www.runoob.com/nodejs/nodejs-install-setup.html" target="_blank">教程</a> 

##NPM 使用介绍
<a href="http://www.runoob.com/nodejs/nodejs-npm.html" target="_blank">教程</a> 

##nodemon简单配置和使用
###描述
在之前我们每次修改完node代码之后都需要重启服务器才能完成修改，nodemon，是一个监听node代码变化的工具，会自动完成node服务器和数据库服务器的重启
###安装
```
npm install -g nodemon (全局)
npm install --save-dev nodemon (本地)
```
###自动启动
用nodemon替换node去启动项目的入口文件机会在项目改变成自动重启服务器
```
nodemon app.js
```
###手动启动
在nodemon运行时，如果需要手动重新启动应用程序，而不是停止并重新启动nodemon，则可以键入rs回车符，并且nodemon将重新启动你的进程。


##express
###安装
```
$ npm install express --save
```
###app.js
```
const express = require('express')
const app = express()

app.get('/', (req, res) => res.send('Hello World1!'))

app.listen(3000, () => console.log('Example app listening on port 3000!'))
```

###运行
```
nodemon app.js
```

###访问
浏览器访问<a href="http://localhost:3000" target="_blank">http://localhost:3000</a>