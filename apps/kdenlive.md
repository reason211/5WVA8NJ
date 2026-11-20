# Kdenlive

- 项目主页：https://github.com/KDE/kdenlive（GPL-3.0 许可），官网 https://kdenlive.org
- 作用：免费开源、无水印的多轨非线性视频剪辑软件，支持多音视频轨道混剪、语音自动生成字幕与样式编辑、三色轮与示波器调色、关键帧特效与转场、多机位同步剪辑，以及代理剪辑。
- 支持系统：Windows 10 / 11、macOS（Apple 芯片和 Intel）、Linux

## 下载渠道（按优先级）

1. 官网下载页（推荐）：https://kdenlive.org/download/
   - Windows 安装版：`kdenlive-<版本>.exe`（如 `kdenlive-26.08.3.exe`）
   - Windows 便携免安装版：`kdenlive-<版本>_standalone.exe`（自解压压缩包）
   - macOS（Apple 芯片）：`kdenlive-<版本>-arm64.dmg`
   - macOS（Intel 芯片）：`kdenlive-<版本>-x86_64.dmg`
   - Linux：`kdenlive-<版本>-x86_64.AppImage` 或 Flatpak（`org.kde.kdenlive`）
2. Windows 也可用 winget：`winget install KDE.Kdenlive`

## 安装步骤

- **Windows（安装版）：** 从官网下载页获取最新 `kdenlive-<版本>.exe`（或运行 `winget install KDE.Kdenlive`），核对官网页面列出的文件大小或校验信息后，双击按向导完成安装。
- **Windows（便携版）：** 下载 `kdenlive-<版本>_standalone.exe`，解压到不含中文和特殊符号的目录后，运行其中的 `kdenlive.exe`。
- **macOS：** 按芯片类型下载 `arm64.dmg` 或 `x86_64.dmg`，打开后把 `kdenlive.app` 拖进「应用程序」。若首次打开提示无法验证开发者，先向用户说明原因，由用户在「系统设置 → 隐私与安全性」点击「仍要打开」。
- **Linux：** 下载 `.AppImage` 后赋予可执行权限（`chmod +x kdenlive-*.AppImage`）直接运行，或通过 Flatpak 安装。
- **简体中文界面：** 首次打开如为英文，可在顶部菜单 `Settings → Configure Language` 将语言切换为简体中文并重启软件。

## 验证方法

- 打开 Kdenlive 能进入主界面，新建工程后可把一段本地测试视频拖入时间线播放并预览画面。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认安装包来自官网 `kdenlive.org` / `download.kde.org` 后，先向用户说明原因，点击「更多信息 → 仍要运行」。
- **高分辨率素材预览卡顿：** 可在「项目 → 项目设置」中开启代理剪辑（Proxy Clips），先用低分辨率缓存剪辑，导出时仍会使用原始高清素材渲染。
