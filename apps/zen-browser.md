# Zen Browser

- 项目主页：https://github.com/zen-browser/desktop（官网 https://zen-browser.app ，文档 https://docs.zen-browser.app ）
- 作用：基于 Firefox 的开源专注浏览器。支持垂直标签栏、最多 4 个标签同屏分屏、Glance 悬停小窗预览链接、工作区隔离、鼠标靠近才弹出的紧凑隐藏模式，以及 78 款开源界面扩展（Zen Mods），无内置广告与弹窗推荐。
- 支持系统：Windows 10+（x64 / ARM64）、macOS（Apple Silicon / Intel 通用版）、Linux（AppImage / tar.xz / Flatpak）

## 下载渠道（按优先级）

1. 官网下载：https://zen-browser.app/download
2. GitHub Releases：https://github.com/zen-browser/desktop/releases/latest
3. 命令行包管理器：
   - Windows（WinGet）：`winget install Zen-Team.Zen-Browser`
   - macOS（Homebrew）：`brew install --cask zen`

按系统选择安装包（以 Releases 页面为准，当前最新 `1.24.3b`）：
- Windows：64 位电脑下载 `zen.installer.exe`，ARM64 设备下载 `zen.installer-arm64.exe`。
- macOS：下载 `zen.macos-universal.dmg`。
- Linux：下载 `zen-x86_64.AppImage` 或 `zen.linux-x86_64.tar.xz`（ARM64 选对应 `aarch64` 包）。

## 安装步骤

1. **Windows**：双击 `zen.installer.exe`，按向导完成安装即可（无需复杂配置；若弹出 SmartScreen 提示，核实来源为官方 Releases 后点「更多信息 → 仍要运行」）。
2. **macOS**：打开 `zen.macos-universal.dmg`，将 Zen 拖进「应用程序」文件夹，首次打开按系统提示允许运行即可。
3. **Linux**：给 `.AppImage` 添加可执行权限（`chmod +x zen-x86_64.AppImage`）后直接启动，或使用 Flatpak 安装 `app.zen_browser.zen`。
4. 首次打开后可在向导中选择从 Chrome / Edge / Firefox 一键导入书签与密码。

## 验证方法

- 打开 Zen Browser，左侧出现垂直标签栏；按 `Ctrl+Alt+C`（macOS 为 `Option+Cmd+C`）切换紧凑隐藏模式，侧栏自动收起，鼠标移至屏幕左侧边沿自动滑出。
- 选中两个标签拖到一起或右键选「分屏」，页面一分为二同屏显示；按住 `Alt` 点击网页链接可直接在居中 Glance 悬浮小窗预览。

## 常见问题

- **支持哪些插件？** 基于 Firefox Gecko 内核，可直接打开扩展管理安装 Firefox 官方扩展商店里的插件（如 uBlock Origin 等广告拦截或翻译扩展）。
- **如何调整外观和布局？** 在设置 →「Zen Mods」中可直接浏览并一键开启社区界面样式扩展，也可切换不同工作区配色。
