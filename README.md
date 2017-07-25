# webpack构建前端工程
1、确保安装了 Node.js，首先创建一个目录，初始化 npm<br>

`mkdir cat-design && cd cat-design`<br>
`npm init`<br>

2、本地安装 webpack<br>

`npm install -g webpack //全局安装`<br>
`npm install webpack --save-dev //安装到你的项目目录`<br>
`npm install webpack-dev-server --save-dev //开发环境使用的一个轻量的node.js express服务器`<br>

3、安装依赖

* 生产环境依赖<br>
`npm install react —save`<br>
`npm install react-dom —save`<br>
`npm install react-router -save //路由`<br>

* 开发环境依赖 loader<br>
`npm install babel-core --save-dev`<br>
`npm install babel-loader --save-dev //webpack使用`<br>
`npm install babel-preset-env --save-dev //解析ES6`<br>
`npm install babel-preset-react --save-dev //react转码，解析jsx`<br>
`npm install url-loader --save-dev //把较小的图片转换成base64的字符串内嵌在生成的文件里`<br>

* 开发环境依赖 plugin<br>
`npm install babel-plugin-transform-runtime --save-dev //比babel-polyfill更灵活`
`npm install extract-text-webpack-plugin --save-dev //ExtractTextPlugin：分离CSS和JS文件`
`npm install html-webpack-plugin —save-dev//webpack打包生成html页的插件`

* CSS<br>
`npm install style-loader css-loader --save-dev`<br>
`npm install less-loader less --save-dev //css预处理器`<br>

4、配置 babel，在根目录下新建 .babelrc文件
>{<br>
>>"presets": ["env", "react"],<br>
>>"plugins": ["transform-runtime"]<br>
>}<br>

5、配置 webpack，在根目录下新建 webpack.config.js，如果想使用es6去写配置，那么把文件名改为 webpack.config.babel.js<br>

6、配置 .gitignore<br>
`node_modules/`<br>
`build/`<br>
`dist/`<br>

`.idea`<br>
`npm-debug.log`<br>
`yarn-error.log`<br>




