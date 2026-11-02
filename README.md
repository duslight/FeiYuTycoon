# 肥鱼大亨 · 网页版

Godot 4.7.2 导出的 HTML5 构建，单线程模板（`web_nothreads_release`）。

## 重要：必须经 http(s) 打开

双击 `index.html` 用 `file://` 协议打开会报 **`Failed to fetch`**——浏览器禁止 `file://` 下的 `fetch`，而引擎需要 `fetch` 加载 `index.wasm` / `index.pck`。

本地预览：

```powershell
python -m http.server 8100 --directory .
# 浏览器打开 http://127.0.0.1:8100/index.html
```

## 内容

| 文件 | 说明 |
|---|---|
| `index.html` | 入口壳（默认模板） |
| `index.js` | 引导器 |
| `index.wasm` | 引擎本体 37.68 MB（固定大小，与游戏内容无关） |
| `index.pck` | 游戏资源 6.24 MB |
| `index.png` / `index.icon.png` / `index.apple-touch-icon.png` | 加载图与图标 |
| `index.audio.worklet.js` / `index.audio.position.worklet.js` | 音频 worklet |

## 已知限制

- 单线程模板：不需要 COOP/COEP 响应头，普通静态托管即可
- 浏览器要求**首次点击**后才允许出声（自动播放策略），进入主菜单后点一下画面音乐才会起来
- `index.pck` 引用的是固定文件名，发布新版本建议换目录或用缓存清除策略
