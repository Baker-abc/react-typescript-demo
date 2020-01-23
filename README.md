https://juejin.im/post/5c04d3f3f265da612e28649c#heading-29


1、mkdir react-typescript-demo
2、npm init -y
3、npm i react react-dom @types/react @types/react-dom react-router-dom @types/react-router-dom react-redux @types/react-redux redux-thunk redux-logger @types/redux-logger connected-react-router -S

- react // react的核心文件
- @types/react // 声明文件
- react-dom // react dom的操作包
- @types/react-dom 
- react-router-dom // react路由包
- @types/react-router-dom
- react-redux
- @types/react-redux
- redux-thunk  // 中间件
- @types/redux-logger
- redux-logger // 中间件
- connected-react-router

4、npm i webpack webpack-cli webpack-dev-server html-webpack-plugin -D

- webpack // webpack的核心包
- webpack-cli // webapck的工具包
- webpack-dev-server // webpack的开发服务
- html-webpack-plugin // webpack的插件，可以生成index.html文件

5、npm i typescript ts-loader source-map-loader -D

- typescript // ts的核心包
- ts-loader // 把ts编译成指定语法比如es5 es6等的工具，有了它，基本不需要babel了，因为它会把我们的代码编译成es5
- source-map-loader // 用于开发环境中调试ts代码

6、tsc --init
// tsconfig.json
{
  // 编译选项
  "compilerOptions": {
    "target": "es5", // 编译成es5语法
    "module": "commonjs", // 模块的类型
    "outDir": "./dist", // 编译后的文件目录
    "sourceMap": true, // 生成sourceMap方便我们在开发过程中调试
    "noImplicitAny": true, // 每个变量都要标明类型
    "jsx": "react", // jsx的版本,使用这个就不需要额外使用babel了，会编译成React.createElement
  },
  // 为了加快整个编译过程，我们指定相应的路径
  "include": [
    "./src/**/*"
  ]
}

7、在./src/下创建一个index.html文件，并且添加<div id='app'></div>标签

8、在./下创建一个webpack配置文件webpack.config.js

9、在package.json里的script，添加build和dev的配置，运行这个webpack.config.js

10、npm run build && npm run dev

11、http://localhost:8080/
