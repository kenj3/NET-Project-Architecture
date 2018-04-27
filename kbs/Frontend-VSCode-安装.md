## 安装 VS code
VSCodeSetup-x64-1.17.1

## 下载并安装Node
node-v8.7.0-x64

## 修改npm源
https://blog.csdn.net/qq940853667/article/details/70837646

全局配置切换到淘宝源
```
npm config set registry https://registry.npm.taobao.org
```

全局配置切换到官方源
```
npm config set registry http://www.npmjs.org
```

检测是否切换到了淘宝源
```
npm info underscore
```

## 安装webpack
各种不同的版本有很大差别，会涉及到打包等方法和命令的不同。
在项目的package.json目录下执行的命令分别是
```
npm install -g webpack@3.7.1
```
和 
```
npm install --save-dev webpack@3.7.1
```

切换webpack mode
```
webpack --mode development
webpack --mode production
```

## 全局安装webpack-cli
```
npm install webpack-cli -g
```

## 安装各种解析plugin
es6解析
```
npm install babel-loader --save
```
解析并抽取css
```
npm install --save-dev extract-text-webpack-plugin
```
多线程打包工具
```
npm install --save-dev happypack
```

