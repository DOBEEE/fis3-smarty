## 起步

### 安装使用

通过 [README.md](../README.md) 可得知其使用方法

### 一个简单的例子

```
/demo/common
/demo/subsiteA
/demo/subsiteB
```

构造一个例子，其中包含三个模块，每一个模块对应是一个 FIS3 的项目。每一个模块对应一个 SVN 仓库。

> 业务小时，可以只包含一个模块；这三个模块也可以放到一个 SVN 仓库中。
>> 假设版本管理工具选择的是 SVN，当然也可以是 GIT 或其他，下同。

- common 模块包含公用的一些 widget 或 layout 以及可能的一些测试数据
- subsite* 子站模块
    
    > 当站点包含的代码量很大时，就需要考虑拆成子站来单独维护，这样互相上线不会受到干扰，而且也减轻了 SVN merge 的出错几率。

    举个例子，假设 [知道](https://zhidao.baidu.com) 站点，首页为一个模块、分类页作为一个模块、问题页作为一个模块等。

每一个模块的目录结构如下；

```
<module>/widget # 放一些 widget 我们暂定叫它组件
<module>/page   # 放一些页面，子站可能有多个页面
<module>/plugin # 有一些 Smarty 的插件放入这个目录，当然一般只需要一个模块拥有即可，比如 common
<module>/test   # 测试数据，放一些模拟数据
<module>/server.conf     # 本地测试的 URL 转发规则配置文件
<module>/smarty.conf     # 本地测试的 Smarty 引擎的配置文件
```