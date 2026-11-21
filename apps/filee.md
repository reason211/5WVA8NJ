# Filee

- 项目主页：https://github.com/KnifeLemon/Filee（MIT 许可），官网 https://filee.sh/zh-cn/
- 作用：本地离线多格式文件转换工具，支持 260 多种格式（图片、PDF、Word、Excel、PPT、电子书、音视频、压缩包、CAD、3D 模型等）。按住 Ctrl（macOS 按住 Option）拖动文件即可在光标旁弹出环形格式菜单，拖到目标格式松手就能完成本地转换，无需上传云端，也无需安装 Office。
- 支持系统：Windows 10 / 11（含 ARM64）、macOS 13 及以上、Linux（x64 / ARM64）

## 下载渠道（按优先级）

1. GitHub Releases（推荐）：https://github.com/KnifeLemon/Filee/releases/latest
   - Windows 64 位安装版：`Filee-<版本>-win-Setup.exe`
   - Windows 64 位便携版：`Filee-<版本>-win-Portable.zip`
   - Windows ARM64 安装版：`Filee-<版本>-win-arm64-Setup.exe`
   - Windows ARM64 便携版：`Filee-<版本>-win-arm64-Portable.zip`
   - macOS（Apple Silicon / Intel）：`Filee-<版本>-osx-arm64.dmg` / `Filee-<版本>-osx-x64.dmg`
   - Linux（x64 / ARM64）：`Filee-<版本>-linux-x64.tar.gz` / `Filee-<版本>-linux-arm64.tar.gz`
2. Windows 包管理器 winget：`winget install KnifeLemon.Filee`
3. 微软商店（Microsoft Store）：搜索并安装 `Filee`（商店页 `XPDCN05L89WS0C`）

## 安装步骤

- **Windows（安装版）：** 下载对应架构的 `Filee-*-Setup.exe`（或通过 winget / 微软商店安装），双击运行按提示完成即可（可选开启资源管理器右键菜单与开机自启）。
- **Windows（便携版）：** 下载对应 `win-Portable.zip` 解压后直接双击运行 `Filee.exe`。
- **macOS：** 打开对应芯片架构的 `.dmg`，将 `Filee.app` 拖入「应用程序」文件夹（也可下载 `.tar.gz` 解压后运行 `./install.sh` 顺带安装 `filee` 命令行）。
- **Linux：** 解压对应 `.tar.gz` 后在目录内运行 `./install.sh`（无需 root，需 Python 3）。

## 验证方法

- 打开 Filee 主界面（默认随系统显示简体中文），将任意文件拖入首页拖放区，或在文件夹中按住 Ctrl（macOS 按 Option）拖动文件，光标旁弹出格式圆环并成功在原文件旁生成转换后的文件。

## 常见问题

- **macOS 提示无法验证开发者：** 因应用尚未公证，首次打开被拦截时到「系统设置 → 隐私与安全性」点击「仍要打开」即可。先向用户说明原因再操作。
- **老版本 Windows 10 无法启动：** 若遇到无报错闪退，官方建议安装最新 Windows 累积更新，或在向用户说明后为 `Filee.exe` 关闭系统硬件强制堆栈保护。
