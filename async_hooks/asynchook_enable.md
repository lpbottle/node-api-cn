
* 返回 {AsyncHook} 一个 `asyncHook` 的引用.

激活指定 `AsyncHook` 实例的回调. 如果没有传输回调参数，那么这个方法将会是一个空操作。

`AsyncHook` 实例默认是被禁用的. 如果 `AsyncHook` 实例想要在创建之后立刻被激活，以下这种形式可以被使用。

```js
const async_hooks = require('async_hooks');

const hook = async_hooks.createHook(callbacks).enable();
```

