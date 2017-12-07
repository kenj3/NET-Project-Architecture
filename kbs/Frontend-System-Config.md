# 前端环境配置

#### [返回目录](README.md)

## 1 说明

鉴于前端依赖库大部分都需要翻墙，所以推荐使用taobao镜像库。

## 2 下载安装node环境

开发尽量选择高版本安装。

win64系统选择：node-vx.x.x-x64.msi

- [node淘宝镜像](<https://npm.taobao.org/mirrors/node>)

mac系统推荐使用homebrew来安装node

- [homebrew参考](<http://blog.csdn.net/baihuaxiu123/article/details/51868142>)

## 3 下载安装git

同node

win64系统选择：Git-x.x.x.x-64-bit.exe

- [git淘宝镜像](<https://npm.taobao.org/mirrors/git-for-windows/>)

mac系统推荐使用homebrew来安装git

## 4 切换npm的源路径为taobao镜像路径（推荐）

- [npm淘宝镜像参考](<https://npm.taobao.org/>)

推荐安装nrm来管理npm源路径

- [nrm](<https://github.com/Pana/nrm>)

## 5 开发工具

推荐使用VSCode来进行前端项目的开发。

- [VSCode](<https://code.visualstudio.com/>)

推荐插件列表

- Auto Close Tag
- Auto Rename Tag
- Beautify
- Document This
- ESLint
- Git Lens
- JavaScript(ES6) code snippets
- Path Autocomplete
- Path Intellisense
- React-Native/React/Redux snippets for es6/es7
- stylelint
- vscode-fileheader
- vscode-icons

基本配置

```json
{
    "editor.fontSize": 16,
    "fileheader.Author": "your name",
    "fileheader.tpl": "/*\r\n * @Author: {author} \r\n * @since: {createTime} \r\n */",
    "fileheader.LastModifiedBy": "your name",
    "git.confirmSync": false,
    "git.enableSmartCommit": true,
    "editor.formatOnSave": false,
    "eslint.autoFixOnSave": false,
    "eslint.options": {
        "extensions": [
            ".jsx",
            ".js",
            ".vue"
        ]
    },
    "eslint.validate": [
        "javascript",
        "javascriptreact",
        "vue",
        "vue-html"
    ],
    "extensions.ignoreRecommendations": true,
    "workbench.colorTheme": "Monokai",
    "files.exclude": {
        "**/.git": true,
        "**/.svn": true,
        "**/.hg": true,
        "**/CVS": true,
        "**/node_modules": true,
        "**/.DS_Store": true
    },
    "workbench.startupEditor": "newUntitledFile",
    "beautify.config": {
        "selector_separator_newline": true,
        "space_in_paren": true
    },
    "vsicons.dontShowNewVersionMessage": true,
    "docthis.includeDescriptionTag": true,
    "docthis.inferTypesFromNames": true,

    "typescript.validate.enable": false,
    "typescript.format.enable": false,
    "javascript.validate.enable": false
}
```

#### [返回目录](README.md)