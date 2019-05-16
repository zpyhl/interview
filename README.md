# CNode

> 根据 CNode 社区提供的 API 使用 Vue2.x + Webpack + axios + Vue-router 实现了社区基础功能， 内含代码注释，希望能帮到你~

## Build Setup

```bash
# 安装依赖
npm install

# 运行项目 localhost:8080
npm run dev

# 项目打包
npm run build

```

1, main.js 程序入口文件，是初始化 vue 实例并使用需要的插件,加载各种公共组件.

2, import...from...的 from 命令后面可以跟很多路径格式，若只给出 vue，axios 这样的包名，则会自动到 node_modules 中加载；若给出相对路径及文件前缀，则到指定位置寻找。

3, App.vue 是我们的主组件，页面入口文件 ，所有页面都是在 App.vue 下进行切换的。也是整个项目的关键，app.vue 负责构建定义及页面组件归集。
4, router index.js 把准备好路由组件注册到路由里

index.html 文件入口

src 放置组件和入口文件

node_modules 为依赖的模块

config 中配置了路径端口值等

build 中配置了 webpack 的基本配置、开发环境配置、生产环境配置等
