# 常见问题

## 配置`TypeScript`使用时的问题

在配合`TypeScript`使用时，有时候会出现下面这样的问题:*You must therefore provide a value for the "parserOptions.project" property for @typescript-eslint/parser*。

这个时候，我们只需要在`.eslint.js`修改为下面的代码即可以。
```javascript
module.exports = {
    // ...
    parseOptions: {
    // ...
    project:[/*tsconfig配置文件的路径*/]
    // ...
    }
    //  ...
}
```
