1. 全局安装webpack 
前提：nodejs npm install webpack -g npm install webpack-cli -g 
2. npm init 生成: package.json 包名
 3. 项目目录中进行局部安装webpack npm install webpack --save npm install webpack-cli --save 
 4. 默认入口和出口 入口:src/index.js entry 出口:dist/main.js output 
 5. 项目的根目录新建一个
webpack.config.jf 
6. hash ：当内容发生变化时，哈希值发生变化 hash作用：清理缓存
 7. 命令操作 package.json "scripts": { "dev": "webpack" }
  8. 使用本地服务器 
  : webpack-dev-server
   1. 安装：npm install webpack-dev-server --save
    2. 配置：webpack.congfig.js devServer: { contentBase:"public", //本地服务的目录
inline:true,
 //实时刷新 port: 9000,
  //端口 open:true 
  //自动打开浏览器 } **********************************************