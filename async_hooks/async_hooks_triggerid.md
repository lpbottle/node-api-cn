
* {number} 返回负责调用当前正被执行的回调函数的资源ID.

例如:

```js
const server = net.createServer((conn) => {
  // The resource that caused (or triggered) this callback to be called
  // was that of the new connection. Thus the return value of triggerId()
  // is the asyncId of "conn".
  async_hooks.triggerId();

}).listen(port, () => {
  // Even though all callbacks passed to .listen() are wrapped in a nextTick()
  // the callback itself exists because the call to the server's .listen()
  // was made. So the return value would be the ID of the server.
  async_hooks.triggerId();
});
```

