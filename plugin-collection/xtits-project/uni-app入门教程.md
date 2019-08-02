# uni-app入门文档

#### 1.创建un-app项目

本文使用vue-cli命令行安装

> 1.环境安装： 全局安装vue-cli
>
> ```
> npm install -g @vue/cli
> ```
>
> 2.创建uni-app，选择hello uni-app模板
>
> ```
> vue create -p dcloudio/uni-preset-vue my-project
> ```
>
> 3.打开HBuilderX，导入刚刚创建的项目：文件>导入>从本地目录导入(D)
>
> 4.打开微信开发工具，初次使用微信开发工具的需要开启服务端口：设置>安全>服务端口，开启
>
> 5.运行HBuilderX中导入的项目，运行项目即可查看

#### 2.创建项目目录

```
┌─projext				项目名称，项目根目录
|——dist 				项目运行文件以及打包文件
|——node_modules			项目依赖文件
|——public				项目html模板
|——src					项目内容：所有的页面使用到的文件都在这个里面
|	├——assets			css、scss以及字体样式等静态文件
|	|——components		uni-app组件目录【可复用的组件】
|	|——modules			项目数据接口定义
|	|	|——api			接口定义
|	|	|——enmus		枚举定义
|	|	└——xtp			xtp接口数据处理
|	|——pages			业务页面文件存放的目录
|	|——pagesA			业务页面文件分包存放的目录
|	|——static			存放应用引用静态资源（如图片、视频等）的目录，注意：静态资源只能存放于此
|	|——store			vuex，状态管理
|	|——utils			js小工具
|	|——wxcomponents		微信小程序组件【可复用的组件】
|	|——App.vue			应用配置，用来配置App全局样式以及监听 应用生命周期
|	|——main.js			Vue初始化入口文件
|	|——mainfest.json	配置应用名称、appid、logo、版本等打包信息，详见uni-app文档
|	|——pages.json		配置页面路由、导航条、选项卡等页面类信息，详见uni-app文档
|	└─uni.scss			全局全局样式文件
|
|——babel.config.js		babel打包配置
|——package.json			所需模块配置文件
|——postcss.config.js	css/scss打包配置
└─README.md				介绍
```

#### 3.安装相关依赖

> 1.如果需要在其他地方使用项目的话，需要安装cross-env插件
>
> ```
> npm install cross-env --save
> ```
>
> 2.使用npm在目录安装需要的依赖
>
> npm的依赖不能直接引入使用，需要进入：node_modules>找到相应的依赖文件
>
> 拷贝依赖放到src目录下，然后再在文中进行引用。详见https://ask.dcloud.net.cn/article/19727

使用HBuilderX进行运行到微信开发者工具/浏览器/模拟器，就可以进行开发，具体使用代码

具体框架、组件、API，详见https://uniapp.dcloud.io/