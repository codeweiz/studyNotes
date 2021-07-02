## TypeScript 安装

- NPM 安装

  将镜像源换成淘宝源，安装更快

  ```shell
  npm config set registry https://registry.npm.taobao.org
  ```

  安装 typescript

  ```shell
  npm install -g typescript
  ```

  查看是否安装成功

  ```shell
  tsc -v
  ```

- 简单测试 TypeScript 是否可用

  新建 app.ts 文件

  ```shell
  mkdir TypeScriptProjects
  cd TypeScriptProjects
  touch app.ts
  vim app.ts
  ```

  按 i 进入输入模式，在 app.ts 文件中输入代码

  ```typescript
  var message:string = "Hello World"
  console.log(message)
  ```

  按 esc 进入命令模式，输入 :wq 保存并退出

  ```shell
  :wq
  ```

  将 .ts 文件转换成 .js 文件

  ```shell
  tsc app.ts
  ```

  在同目录下会生成一个 app.js 文件，代码如下

  ```javascript
  var message = "Hello World";
  console.log(message)
  ```

  使用 node 命令执行 app.js 文件

  ```shell
  node app.js
  ```

  显示

  ```shell
  Hello World
  ```



## TypeScript 基础

