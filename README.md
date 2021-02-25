# supermall

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

新项目:

1.划分目录结构

assets:放置图片和样式文件
components:放置公共组件 /common:放置独立组件,可以在其他项目 /content:放置与当前业务有关的公共组件
views:放置大型页面
common:放置公用的js文件
network:网络请求
router:路由
store:放置全局资源

2.引用两个css文件(normalize/base)

3.配置路径别名(vue.config.js)以及代码风格(.editorconfig)

4.引入Tabbar 配置路由

5.navbar组件

6.封装网络模块 request.js

7.请求首页数据 并展示 (轮播图,首页推荐) 网络请求都在Home界面 向子组件传递数据