# BentoPDF

- 项目主页：https://github.com/alam00000/bentopdf（AGPL-3.0 / 商业双许可），官网 https://www.bentopdf.com
- 作用：隐私优先的浏览器端 PDF 工具箱。内置 50 多种工具：合并、拆分、压缩、编辑文字、签署、加水印、OCR 识别，以及 Word/Excel/PPT/WPS/EPUB/图片与 PDF 互转；所有处理全部在本地浏览器内完成，文件不上传服务器。
- 支持系统：Windows、macOS、Linux、Android、iOS（任意现代浏览器即可使用；本地部署版需 Node.js 或 Docker）。

## 下载渠道（按优先级）

1. GitHub Releases（静态离线包）：https://github.com/alam00000/bentopdf/releases/latest
   - `dist-simple-…zip`：自托管无营销版静态包（推荐个人本地使用）
   - `dist-…zip`：完整静态包
2. Docker / Podman 容器部署：
   - `docker run -p 3000:8080 ghcr.io/alam00000/bentopdf-simple:latest`
3. 官方公开网页版（免安装直接用）：https://www.bentopdf.com

## 安装步骤（本地部署）

- 下载 GitHub Releases 中的 `dist-simple-*.zip` 并解压到一个本地目录。
- 在解压目录下运行静态服务器（例如 `npx http-server -c-1 -p 8080`，或使用 Docker 启动容器），然后在浏览器打开 `http://localhost:8080/`（或 `http://localhost:3000`）。
- 注：如需使用 Office 转 PDF（LibreOffice WASM）功能，请通过 `http://localhost` 或带 HTTPS 的安全上下文访问。

## 验证方法

- 浏览器打开本地地址（如 `http://localhost:8080/`），能看到中文工具箱列表（合并 PDF、分割 PDF、压缩 PDF、Word 转 PDF 等），点击任意工具能选择本地 PDF 并直接完成处理下载。

## 常见问题

- **本地打开报错 `npx` 未找到：** 先安装 Node.js（v18 及以上），或改用 Python 静态服务器 / Docker 镜像启动。
- **局域网 IP 访问提示缺少 `SharedArrayBuffer`：** 使用 `http://localhost` 本机访问，或配置 HTTPS 安全上下文。
