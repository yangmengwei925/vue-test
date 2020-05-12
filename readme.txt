全局安装
webpack
cli（脚手架）
npm(cnpm) install webpack webpack-cli -g
局部安装 webpack
npm init
npm（cnpm）install webpack webpack-cli --save
默认参数
入口(entry):./src/index.js
出口 (output):./dist/main.js
压缩（未压缩）
webpack --mode development 
webpack --mode production 压缩
自定义
在 package.json->script->新增一个键值
运行 ：npm run 指令的名称
本地服务
webpack-dev -server
安装本地服务 npm (cnpm) install webpack-dev -server --save
在webpack.config.js->devServer->contentBase；“webpack打包路径”
打包html文件
安装html-webpack-plugins npm(cnpm) install html-webpack-plugin --save
在webpack.config.js->引用html-webpack-plugin->新增plugins->实例化一个htmlwebpackplugins(template:"需要打包的html文件路径./src/index.html")
打包css文件以及其他文件
loader加载程序
加载css文件->下载npm(cnpm) install css-loader style-loader --save
ts-loader typescripts