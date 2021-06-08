# npm-cli
npm cli test

[note->]()

在package.json中声明bin字段  
ps bin配置是生成命令行执行入口用的 main是js模块引入的入口(require import)

mycli/package.json
```json
{
    "bin":{
        "mycli":"bin/cli.js"
    }
}
```
***一定要在cli.js文件开头用 #! node声明运行环境 win和Linux可能会有所不同***  
或者是#!/usr/bin/env node

配置了bin，使用 install 安装mycli后会在 node_modules/.bin/ 文件夹下生成  
 mycli mycli.cmd mycli.ps1 等文件

测试cli执行
```cmd
# 安装cli 依赖
npm install --save ./mycli

# 运行cli
npx mycli
```

测试包导入
```cmd
node src/index.js
```
