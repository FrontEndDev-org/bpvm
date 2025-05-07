# bpvm

一个基于 Proxy 的浏览器沙箱，确保动态运行的代码，不会污染全局环境。

## 安装

```sh
$ pnpm add bpvm
```

### 使用

```ts
import { runInNewContext } from 'bpvm'

window.globalVar = 3

const context = {
  globalVar: 1,
}

runInNewContext('globalVar *= 2', context)

console.log(context)
// Prints: { globalVar: 2 }

console.log(window.globalVar)
// Prints: 3
```

## 本地启动

1. 使用 **vscode** 打开项目
2. 进入到子模块的 `samples` 目录
3. 打开需要运行的示例文件
4. 点击侧边栏的 **运行和调试** 按钮
5. 运行 `Run Files`

## License

MIT
