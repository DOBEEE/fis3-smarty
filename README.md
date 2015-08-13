## fis3-smarty

基于 FIS3 的针对 Smarty 模板的前端工程解决方案

### 文档

- Smarty 插件、本地测试套件、上线指导等文档参见 [/doc/INDEX.md](doc/INDEX.md)
- 构建工具文档参见 https://github.com/fex-team/fis3

### 使用方法

**安装**

```
npm install -g fis3
npm install -g fis3-smarty
```

**配置使用**
```js
// vi fis-conf.js

fis.require('smarty')(fis);
fis.set('namespace', <namespace>);

// default media is `dev`，
fis.media('dev').match('*', {
    useHash: false,
    optimizer: null
});

```
- `<namespace>` 当前模块唯一名字
- `fis3 release` 时执行时关闭 **md5**、**压缩**

### 本地测试服务

**安装本地模拟环境**

```bash
fis3 server install server-env
```

**启动服务**

```bash
fis3 server start --type php --rewrite
```

