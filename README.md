# PWA Icon Resize

一个纯前端的 PWA 图标尺寸转换工具。上传一张图片后，页面会在浏览器本地完成缩放、预览和打包下载，适合快速生成常见的 PWA / favicon 图标资源。

## 在线地址

- 线上访问：<https://pwa-icon.fengxue.wang>
- 本地入口：[index.html](index.html)

## AI 声明

> [!IMPORTANT]
> 本项目中的页面代码完全来自 AI 生成，核心实现集中在 [index.html](index.html)。本 README 也已按当前仓库状态由 AI 重新编写。

## 功能特性

- 支持上传 `PNG`、`JPG`、`SVG` 图片
- 支持拖拽上传和点击选择文件
- 支持三种缩放模式：`contain`、`cover`、`stretch`
- 支持为导出图标添加背景色
- 支持多尺寸实时预览
- 支持一键打包下载 ZIP
- 所有图像处理均在浏览器本地完成，不上传文件到服务器

## 导出内容

下载的 ZIP 默认包含以下文件：

- `pwa-512-512x512.png`
- `pwa-384-384x384.png`
- `pwa-192-192x192.png`
- `apple-touch-180-180x180.png`
- `apple-touch-152-152x152.png`
- `microsoft-tile-144-144x144.png`
- `icon-128-128x128.png`
- `icon-96-96x96.png`
- `android-72-72x72.png`
- `favicon-32-32x32.png`
- `manifest-icon-example.json`
- `README.txt`

## 使用方式

### 直接在线使用

直接打开 <https://pwa-icon.fengxue.wang> 即可。

### 本地使用

直接用浏览器打开 [index.html](index.html)，或者在项目目录启动一个静态文件服务：

```bash
python3 -m http.server 8000
```

然后访问 `http://localhost:8000`。

## 使用步骤

1. 上传一张 Logo 图片，推荐使用接近 `1024x1024` 的源图。
2. 选择是否添加背景色。
3. 选择缩放模式。
4. 检查各尺寸预览效果。
5. 点击“打包下载所有图标”导出 ZIP。

## 项目结构

```text
.
├── CNAME
├── LICENSE
├── README.md
└── index.html
```

## 域名说明

- 仓库已包含 [CNAME](CNAME)，当前自定义域名为 `pwa-icon.fengxue.wang`
- 如果静态托管平台支持 `CNAME` 约定，部署后可直接使用该域名访问

## 依赖

页面通过 CDN 加载以下第三方库：

- `JSZip 3.10.1`
- `FileSaver.js 2.0.5`

如果访问环境无法连接这些 CDN，页面的 ZIP 打包下载能力会受影响。

## 注意事项

- 这是一个无构建步骤的静态页面项目，不需要安装依赖
- 图像处理和导出逻辑基于浏览器 `Canvas`
- 若想保留真实透明背景，请不要勾选“为图标添加背景色”
- 当前“透明背景（模拟无背景色）”选项的导出效果会带棋盘格示意背景，这是现有实现行为，不是真正的透明导出

## License

本项目采用 [MIT License](LICENSE)。
