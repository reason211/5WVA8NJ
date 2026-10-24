# OpenList

- 项目主页：https://github.com/OpenListTeam/OpenList（AGPL-3.0 许可），文档 https://doc.oplist.org
- 说明：AList 的社区维护分支。作用是把多个网盘和存储（百度网盘、阿里云盘、夸克、迅雷、115、OneDrive、WebDAV、本地磁盘等）挂到同一个网页文件列表里，在线预览图片、视频、音频、PDF、Office 文档，可给文件夹加密码。
- 支持系统：Windows、macOS、Linux（也支持 Docker）。
- **注意：** 只挂载用户自己的网盘账号；它是一个本地服务程序，装好后通过浏览器访问。

## 下载渠道

- GitHub Releases：https://github.com/OpenListTeam/OpenList/releases/latest ，按系统选择压缩包（如 `openlist-windows-amd64*.zip`、`openlist-darwin-arm64*.tar.gz`、`openlist-linux-amd64*.tar.gz`）。

## 安装步骤

1. 解压到一个固定目录（例如 `C:\OpenList` 或 `~/OpenList`）。
2. 在该目录运行 `openlist server`（Windows 为 `openlist.exe server`）。看到 `start server @ 0.0.0.0:5244` 即启动成功。
3. 首次运行会输出初始管理员密码；也可以运行 `openlist admin random` 重新生成。把访问地址 `http://127.0.0.1:5244` 和管理员账号密码告诉用户。
4. 用户登录后，在「管理 → 存储」里添加自己的网盘。

## 验证方法

- 浏览器打开 `http://127.0.0.1:5244` 能看到 OpenList 页面并能登录。

## 常见问题

- **端口被占用：** 修改 `data/config.json` 里的端口后重启。
- **想开机自启：** 先说明作用，用户同意后再按文档配置系统服务。
