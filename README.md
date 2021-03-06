# React Seed (PC)

基于react技术栈的种子站点, 适用于企业中后台管理系统的快速搭建。

## 开发环境

windows下推荐安装终端环境：[cmder.net](http://cmder.net/)

安装nodejs: https://nodejs.org/en/

### 启动项目

进入项目目录,运行

```
npm install
npm run dev
```

等待一会儿，系统自动打开浏览器，即可进行开发。

### 项目打包

```
npm run build
```

运行完成后，在项目下生成dist目录，直接将dist目录下内容发布到生产环境下即可（nginx / apache等），人肉、jekins随便。

### 代码检查

```
npm run lint
```

注意：如果在windows下开发，因为windows换行符和*nux系统不一致，可能会导致以下lint错误：

```
157:3    error  Expected linebreaks to be 'LF' but found 'CRLF'  linebreak-style
```

运行以下命令解决：

```
eslint --fix --ext .js src
```

如果eslint命令找不到，尝试

```
.\node_modules\.bin\eslint.cmd --fix --ext .js src
```

同时，更改编辑器换行符设置: `CRLF -> LF`:

以`sublime`为例，菜单栏 `View` -> `Line Endings` -> `Unix`
 
javascript规范主要参考[airbnb规范](https://github.com/airbnb/javascript)

### 前后端分离 MOCKUP

mockup相关配置在`config/index.js`中:

```
// 后端服务器地址前缀，在`config.dev.mock`为`false`的情况下，
// 以此前缀开头的请求全部转发至指定服务器`targetUrl`
const apiPrefix = '/api';
// 后端服务器, 域名或者都可以
// eg: http://192.168.71.26:9082
const targetUrl = 'http://45.32.79.142:3000';

// mock开关, true表示不访问远程服务器，使用本地mockup目录数据进行开发
config.dev.mock: false
  
```

### git commit hook

git commit时会运行lint进行代码静态检查，代码检查通过才可以正常commit

## 目录说明

[目录说明](docs/catelog.md)

## 开发步骤

[开发步骤](docs/dev.md)

## 项目部署

[项目部署](docs/online.md)

## 学习资源

根据针对当前开发框架，所需了解知识的重要程度，**分为1~5颗星,5表示最重要**

### es6 新一代JavaScript标准 ⭐️⭐️⭐️⭐️⭐️

http://es6.ruanyifeng.com/

### react ⭐️⭐️⭐️⭐️⭐️

官网：https://facebook.github.io/react/docs/hello-world.html


### dva框架 ⭐️⭐️⭐️⭐️⭐️

基于 redux、redux-saga 和 react-router@2.x 的轻量级前端框架.

https://github.com/dvajs/dva

#### 必看文章

1. 关键技术点：https://github.com/dvajs/dva-knowledgemap
2. 关键概念：https://github.com/dvajs/dva/blob/master/docs/Concepts_zh-CN.md

### redux ⭐️⭐️⭐️⭐️⭐️

状态管理

http://cn.redux.js.org/

### react-router ⭐️⭐️⭐️⭐

单页路由管理

https://react-guide.github.io/react-router-cn/index.html

### Redux-saga ⭐️⭐️⭐️ dva已对其做了封装，所以只需了解大致概念

redux-saga 是一个用于管理 Redux 应用异步操作（Side Effects。译注：直译成 “副作用” 不太通顺，所以这里译为 “异步操作” 更好理解）的中间件（又称异步 action）。 redux-saga 通过创建 *Sagas* 将所有的异步操作逻辑收集在一个地方集中处理，可以用来代替 `redux-thunk` 中间件。

http://leonshi.com/redux-saga-in-chinese/

### and ⭐️⭐️⭐️⭐️ 组件库

基于react的UI组件库，蚂蚁金服团队出品，github star 12000+

文档： https://ant.design

### webpack ⭐️⭐️ (构建工具，业务开发中一般不需要关注)

http://webpack.github.io/docs/

## awesome-react ⭐

收集了react社区优秀的文章、工具、周边生态、各类库，非常全面

https://github.com/enaqx/awesome-react


## 其他文章推荐

1. react影响性能的一些反模式分析：[React.js pure render performance anti-pattern](https://medium.com/@esamatti/react-js-pure-render-performance-anti-pattern-fb88c101332f#.kdu55n4xc) 
2. 待补充
