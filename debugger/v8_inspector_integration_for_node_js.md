
V8 的检查器集成可以附加 Chrome 的开发者工具到 Node.js 实例以用于调试和性能分析。
它使用了 [Chrome开发者工具协议]。

当启动一个 Node.js 应用时，V8 检查器可以通过传入 `--inspect` 标志启用。
也可以通过该标志提供一个自定义的端口，如 `--inspect=9222` 会在 9222 端口接受开发者工具连接。

要想在应用代码的第一行断开，可以传入 `--inspect-brk` 标志而不是 `--inspect`。

```txt
$ node --inspect index.js
Debugger listening on 127.0.0.1:9229.
To start debugging, open the following URL in Chrome:
    chrome-devtools://devtools/bundled/inspector.html?experiments=true&v8only=true&ws=127.0.0.1:9229/dc9010dd-f8b8-4ac5-a510-c1a114ec7d29
```

（在上面的例子中，URL 后面的 UUID dc9010dd-f8b8-4ac5-a510-c1a114ec7d29 是在运行时生成的，在不同的调试会话中是不一样的。）

