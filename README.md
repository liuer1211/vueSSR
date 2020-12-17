# vue_ssr

## Build Setup

```bash
# 下载依赖
$ npm install

# 运行访问 localhost:3000
$ npm run dev

# 打包
$ npm run build
$ npm run start

# 静态文件
$ npm run generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).

## 介绍
    服务端渲染 SSR 与 静态网站渲染 SSG
    
## github上一个不错的学习项目
    https://github.com/github1586/nuxt-bnhcp
    
## 页面
![image.png](https://github.com/liuer1211/vueSSR/tree/master/show/1.png)

## 优势 
    2、nuxt.js的优势
    1）就是我们无需为了路由划分而烦恼，你只需要按照对应的文件夹层级创建 .vue 文件就行
    2）无需考虑数据传输问题，nuxt 会在模板输出之前异步请求数据（需要引入 axios 库），而且对 vuex 有进一步的封装
    3）内置了 webpack，省去了配置 webpack 的步骤，nuxt 会根据配置打包对应的文件
