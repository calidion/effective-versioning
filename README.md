# npmver

npm包安装、管理与版本升级规范

### 基本原则

1. 怀疑一切版本的可兼容性
2. 坚持只使用当前测试通过的版本

### 现存的npm包的版本问题

1. 设定了兼容域，比如小版本API兼容
2. 默认兼容安装包，比如对于npm install --save a后，我们得到的是`'^xx.xx.xx'`这样的版本内容信息。
其中^表示小版本升级兼容。
3. 由于兼容域的存在，从而导致了npm包的不稳定，所以才会有yarn这样的精准版本管理工具的出现。
4. 但是yarn仍然存在不少问题，因为它将当前的地址精确化了，对于使用镜像的情况来说并不友好。

所以下面有一些建议，可以完全避免npm存在的问题。

### 建议

1. 安装npm包时使用

```
npm install --save-exact <packagename>
```

准确保存依赖包。

2. 对于自己维护的包，在node有大版本升级时再全面检查升级可能，否则不必考虑版本升级

3. 不要轻易的升级

4. 如果必须要升级，规定时间做统一升级

5. 放弃保绿的观念

6. 将这种方案告诉更多的人

### 版本号规则

1. 大版本表示你的架构或者理念发生了重大变化
2. 小版本表示特征与接口的调整
3. 补丁版本表示对当前bug的修补或者接口的调整
4. 任何版本都尽量保持接口的稳定，但是允许少量紧急功能的调整

