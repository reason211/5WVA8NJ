# PhotoCraft

- 项目主页：https://github.com/storytold/photocraft（MIT / Apache-2.0 双许可），官网 https://getartcraft.com/apps/photocraft
- 说明：纯 Rust 从零编写的开源图像编辑与修图软件，主打轻量、无订阅、离线处理。支持原生打开与保存分层 PSD/PSB 文件，自带 69 种修图与选区工具、16 种非破坏性调整图层（曲线、色阶、色相饱和度、LUT 等）、图层样式、自由变换、矢量形状以及导出预览。
- 支持系统：Windows、macOS、Linux、FreeBSD、Web（浏览器 WebAssembly 版）。

## 下载渠道

- GitHub Releases（推荐）：https://github.com/storytold/photocraft/releases/latest
  - Windows：`photocraft-<版本>-windows-x64.msi`（安装版）或 `photocraft-<版本>-windows-x64-portable.zip`（便携免安装版）；ARM64 电脑选 `windows-arm64` 版本
  - macOS：`photocraft-<版本>-macos-universal.dmg`（通用版，已签名公证）
  - Linux：提供 `.AppImage`、`.deb`、`.rpm`、`.flatpak` 与 `.tar.gz`
  - 网页版：`photocraft-web-<版本>.zip`（静态网页包，可本地启动静态服务在浏览器运行）
- 官网页面：https://getartcraft.com/apps/photocraft

## 安装步骤

1. **Windows：**
   - 推荐下载 `photocraft-*-windows-x64.msi` 安装版，双击按提示完成安装；若需要免安装直接运行，可下载 `windows-x64-portable.zip`，解压后双击目录内的 `photocraft.exe` 即可启动。
2. **macOS：**
   - 下载 `photocraft-*-macos-universal.dmg`，双击打开后将 PhotoCraft 图标拖入「应用程序（Applications）」文件夹，从启动台或应用程序中打开。
3. **Linux：**
   - Ubuntu / Debian 可用 `sudo apt install ./photocraft-*-linux-x86_64.deb`；或下载 `.AppImage`，执行 `chmod +x photocraft-*.AppImage` 后直接运行。

## 验证方法

- 启动 PhotoCraft，确认进入主编辑界面。
- 通过「File → Open」打开一张 JPG、PNG 或分层 PSD 文件，查看右侧「Layers」面板能正确显示图层。
- 在右侧「Adjustments」中添加曲线（Curves）或色阶（Levels）调整图层，拖动曲线或滑块能实时看到画面亮度和色彩变化。
- 点击「File → Export As」，确认可预览画质与预估文件大小并正常导出。

## 常见问题

- **拖放文件进窗口打不开（Linux Wayland 环境）：**
  - 可改用菜单「File → Open」打开文件，或在文件管理器复制图片后用 `Ctrl+V` 粘贴；也可按提示在 Preferences → Performance 中把显示模式切换为 X11。
- **如何把界面改成浅色或深色主题：**
  - 点击右上角主题切换图标或进入设置，可在深色 Pro、浅色 Studio 等主题之间切换。
- **命令行批处理或连接 AI 智能体：**
  - 随附的 CLI 工具支持通过 `photocraft-cli run` 进行无头批处理或 `photocraft-cli mcp` 启动 MCP 服务。
