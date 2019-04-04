使用 egg-mysql /mysql2 和 egg-sequelize

[https://blog.csdn.net/Cappuccino200/article/details/82428809](https://blog.csdn.net/Cappuccino200/article/details/82428809)

1. 启用插件
2. 配置数据库信息

安装了mysql 和egg-sequelize

中间件

插件

一个插件其实就是一个迷你的应用，和应用app几乎一样

\(它包含了Service,中间件，配置，框架扩展等等\)

\(它没有独立的Router和Controller,它没有plugin.js\)

应用可以直接引入Koa的中间件。

多个插件可以包装成一个上层框架。

定时任务。

方法扩展

属性扩展

本地开发

单元测试。

egg-cluster

egg-scripts

cookie and Session.

Session 专门用作用户身份识别。

多进程模型和进程间。

ctx.cookies.get\(key,options\)

ctx.session\(\)

储存扩展，sessionStorage

Cluster

master  包工头

worker 工人

根据服务器的CPU核数来定，这样就可以完美利用多核资源。

异常处理

try

catch

validate 插件

typeScript 的静态类型检查，智能提示，IDE友好性等特性，对于大规模企业级应用，是非常有价值的

EGG 最精髓的Loader自动加载机制，导致TS无法静态分析出部分依赖。



