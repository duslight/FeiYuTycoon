# 肥鱼大亨 · 网页版

Godot 4.7.2 导出的 HTML5 构建，单线程模板（`web_nothreads_release`）。

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


