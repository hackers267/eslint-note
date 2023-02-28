# 配置Prettier使用

`Prettier`是一个通用的前端代码格式化的工具。使用`Prettier`可以有效的帮助我们实现前端代码风格的统一，再加上`EsLint`的检查可以进上步规范代码样式。

## 安装必要的依赖

要想让`EsLint`结合`Prettier`，要安装两个npm包:

* eslint-config-prettier
* eslint-plugin-prettier

```shell
pnpm add -D eslint-config-prettier eslint-plugin-prettier
```

## 修改配置文件

要在`eslint`中使用`prettier`除了要安装npm依赖包之外，还要修改一下`.eslint.js`配置文件,主要要修改三个配置：

* extends字段
* plugins字段
* rules字段

```js
module.exports = {
    extends: ['prettier'],
    plugins: ['prettier'],
    rules:{
        'prettier/prettier': 'error'
    }
}
```
> 注意：`prettier`的插件和扩展要放在其他插件和扩展之后
