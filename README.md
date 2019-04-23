# Egg
Egg.js 为企业级框架和应用而生


## 特性

* 提供基于 Egg 定制上层框架的能力
* 高度可扩展的插件机制
* 内置多进程管理
* 基于 Koa 开发，性能优异
* 框架稳定，测试覆盖率高
* 渐进式开发


## 脚手架

```bash
$ mkdir egg-example && cd egg-example
$ npm init egg --type=simple
```

* simple - Simple egg app boilerplate
* microservice - Microservice app boilerplate based on egg
* sequelize - egg app with sequelize
* ts - Simple egg && typescript app boilerplate
* empty - Empty egg app boilerplate
* plugin - egg plugin boilerplate
* framework - egg framework boilerplate



##### Egg 与 Koa 的版本关系
###### Egg 1.x
* 底层基于 Koa 1.x，异步解决方案基于 co 封装的 generator function。
* 官方插件以及 Egg 核心使用 generator function 编写，保持对 Node.js LTS 版本的支持，在必要处通过 co 包装以兼容在 async function 中的使用。
* 应用开发者可以选择 async function（Node.js 8.x+） 或者 generator function（Node.js 6.x+）进行编写。

###### Egg 2.x
* 底层基于 Koa 2.x，异步解决方案基于 async function。
* 官方插件以及 Egg 核心使用 async function 编写。
* 建议业务层迁移到 async function 方案。
* 只支持 Node.js 8 及以上的版本。
