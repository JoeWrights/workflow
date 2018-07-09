# 前端工作流

- babel(例如vue项目初识完成后有一个.babelrc文件)：js预编译器，将js的未来，现在使用
es6 以前，es6以后
使用最新的js语法来编写，运行的代码可以根据需求编译成相应的版本
babel 编译js
source_code .babelrc cli target(运行平台)
babel 依赖于presets(预处理集)
babel的预处理，只是语法糖(例如es5没有class)，它会把es5里面没有的es6语法，实现一遍，例如最基本的const...
**为什么babel得以运行？因为它有babel-core，它有一系列的语法糖**
- npm
    ```
    npm run dev
    npm install
    项目构建的基本流程
    ```
- postcss
    前缀，css变量
- stylus/scss/less


## babel的使用

- 安装babel
    ```
    yarn global add babel-core babel-cli
    ```
- 进入在项目
    ```
    npm init -y
    yarn add babel-core -D
    yarn add babel-presets-env
    //安装babel插件 
    yarn add babel-plugin-transform-runtime -D
    //针对2015第二季度的编译
    yarn add babel-preset-stage-2 -D    
    ```
- babel-cli的一些命令

    编译js文件
    ```
    babel main.js
    ```
    编译js文件到目标文件
    ```
    babel main.js -o a.js
    ```

## eslint的使用

- 安装eslint
    ```
    yarn add eslint -D
    ```
- 修改package.json
    ```js
    "scripts": {
        "eslint": "eslint *.js"
    }
    ```
- 添加`.eslintrc.js`配置文件
    ```js
        module.exports = {
        env: {
            es6: true,
            node: true
        },
        extends: 'eslint:recommended',
        rules: {                
            quotes: ['error', 'single'],
            semi: ['error', 'always'],
            indent: ['error', 4]
        }
    }
    ```
- 测试代码是否符合规范
    ```
    npm run eslint
    ```


