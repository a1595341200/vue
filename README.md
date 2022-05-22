# Vue3 安装
1、独立版本

```
我们可以在 Vue.js 的官网上直接下载最新版本, 并用 <script> 标签引入。
```
下载 Vue.js
2、使用 CDN 方法

以下推荐国外比较稳定的两个 CDN，国内还没发现哪一家比较好，目前还是建议下载到本地。

    Staticfile CDN（国内） : https://cdn.staticfile.org/vue/3.0.5/vue.global.js

    unpkg：https://unpkg.com/vue@next, 会保持和 npm 发布的最新的版本一致。

    cdnjs : https://cdnjs.cloudflare.com/ajax/libs/vue/3.0.5/vue.global.js
```
Staticfile CDN（国内）
<div id="app">
  <p>{{ message }}</p>
</div>
```
```
unpkg（推荐）
<div id="app">
  <p>{{ message }}</p>
</div>
```
```
cdnjs
<div id="app">
  <p>{{ message }}</p>
</div>
```


3、NPM 方法

由于 npm 安装速度慢，本教程使用了淘宝的镜像及其命令 cnpm，安装使用介绍参照：使用淘宝 NPM 镜像。

npm 版本需要大于 3.0，如果低于此版本需要升级它：
```
# 查看版本
$ npm -v
2.3.0

#升级 npm
cnpm install npm -g


# 升级或安装 cnpm
npm install cnpm -g

在用 Vue.js 构建大型应用时推荐使用 cnpm 安装，cnpm 能很好地和 Webpack 或 Browserify 模块打包器配合使用：

# 最新稳定版
$ cnpm install vue@next
```
命令行工具

Vue.js 提供一个官方命令行工具，可用于快速搭建大型单页应用。

对于 Vue 3，你应该使用 npm 上可用的 Vue CLI v4.5 作为 @vue/cli。要升级，你应该需要全局重新安装最新版本的 @vue/cli：
```
# 全局安装 vue-cli
yarn global add @vue/cli
# 或
cnpm install -g @vue/cli

安装完后查看版本:

$ vue --version
@vue/cli 4.5.11

然后在 Vue 项目中运行：

vue upgrade --next

注意：vue-cli 3.x 和 vue-cli 2.x 使用了相同的 vue 命令，如果你之前已经安装了 vue-cli 2.x，它会被替换为 Vue-cli 3.x。
创建项目
```
以下实例我们使用 vue init 命令来创建一个项目：
```
$ vue init webpack runoob-vue3-test
# 这里需要进行一些配置，默认回车即可
? Project name runoob-vue3-test
? Project description A Vue.js project
? Author runoob <test@runoob.com>
? Vue build standalone
? Install vue-router? Yes
? Use ESLint to lint your code? Yes
? Pick an ESLint preset Standard
? Set up unit tests Yes
? Pick a test runner jest
? Setup e2e tests with Nightwatch? Yes
? Should we run `npm install` for you after the project has been created? (recommended) npm

   vue-cli · Generated "runoob-vue3-test".


# Installing project dependencies ...
# ========================

...

进入项目，安装并运行：

$ cd runoob-vue3-test
$ cnpm run dev
  DONE  Compiled successfully in 2558ms          

 I  Your application is running here: http://localhost:8080

成功执行以上命令后访问 http://localhost:8080/，输出结果如下所示：

    注意：Vue.js 不支持 IE8 及其以下 IE 版本。
```
Vite (推荐)

Vite 是一个 web 开发构建工具，由于其原生 ES 模块导入方式，可以实现闪电般的冷服务器启动。

通过在终端中运行以下命令，可以使用 Vite 快速构建 Vue 项目，语法格式如下：
```
npm init @vitejs/app <project-name>

创建项目 runoob-vue3-test2：

$  cnpm init @vitejs/app runoob-vue3-test2

运行项目:

$ cd runoob-vue3-test2
$ cnpm install
$ cnpm run dev
> runoob-vue3-test2@0.0.0 dev /Users/tianqixin/runoob-test/vue3/runoob-vue3-test2
> vite

[vite] Optimizable dependencies detected:
vue

  Dev server running at:
  > Local:    http://localhost:3000/

打开 http://localhost:3000/，显示如下：
```
![vue](./image/1.jpg)