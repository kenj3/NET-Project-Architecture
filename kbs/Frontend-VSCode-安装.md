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
在项目的package.json目录下执行的命令分别是
```
npm install -g webpack
```
和 
```
npm install --save-dev webpack
```

切换webpack mode
```
webpack --mode develop
webpack --mode production
```
