## 启动

```cmd
npm install
```

```cmd
npm start
```

## 调试主进程

```cmd
electron --inspect=5858 main.js
```

在JavaScript 脚本的第一行暂停运行  

```cmd
electron --inspect-brk=5858 main.js
```

## Node原生模块故障排查

* 请先执行 `electron-rebuild`。

* 确保原生模块与Electron应用程序的目标平台和体系结构兼容。

* 确保 `building.gyp`模块中的 `win_delay_load_hook `没有被设置为 `false`。
* 如果升级了 Electron，你通常需要重新编译这些模块。