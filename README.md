# 前端 React 工程脚手架

## 1. 使用

### 1.1. 安装

```shell
npm i @mini-code/env-scripts --dev
# or
yarn add @mini-code/env-scripts -D
```

### 1.2. 添加到 package.json 的 scripts 中

```json
{
  "scripts": "minictl start"
}
```

## 2. 配置

在工程目录创建 `.mini-scripts-config.js`

```js
module.exports = {
  paths: {
    "srcDir": "src",
    "appIndexJs": "index",
    "appBuildDir": "dist",
    "appHtml": "public/index.html",
    "deployHtml": "public/deploy.html"
  },
  // 给 devServer 的 options
  devServerOptions: {},
  // webpack 的 options
  // 覆盖默认提供的 webpack config
  webpackConfig: {
    output: {
      publicPath: './'
    },
    externals: {
      react: 'React'
    }
  },
  // 完全替代默认的 webpack 配置
  webpackConfigRaw: {},
  preRun: () => {
    // 启动前生命周期函数
  }
}
```
