# Recordly

- 项目主页：https://github.com/webadderallorg/Recordly（AGPL-3.0），官网 https://www.recordly.dev
- 作用：跨平台开源演示录屏和编辑工具。录屏时自动跟焦放大点击区域，支持光标平滑、动态模糊和点击弹跳，内置摄像头气泡叠加、圆角阴影与壁纸背景、拖拽式时间线剪辑，可直接导出 MP4 或 GIF。
- 支持系统：Windows 10（Build 19041+）、macOS 14.0+、Linux。

## 下载渠道（按优先级）

1. GitHub Releases（官方安装包）：https://github.com/webadderallorg/Recordly/releases/latest
   - Windows：`Recordly-windows-x64.exe`
   - macOS（Apple Silicon）：`Recordly-arm64.dmg`
   - macOS（Intel）：`Recordly-x64.dmg`
   - Linux：`Recordly-linux-x64.AppImage`
2. Arch Linux / Manjaro（AUR）：`yay -S recordly-bin`
3. 官网：https://www.recordly.dev

## 安装步骤

- **Windows：** 从 GitHub Releases 下载 `Recordly-windows-x64.exe`（从 GitHub 下载大文件较慢时可使用国内镜像源加速，并核对 `SHA256SUMS.txt` 校验值），需要用户确认后双击安装并运行。
- **macOS：** 根据芯片架构下载 `Recordly-arm64.dmg`（M 系列）或 `Recordly-x64.dmg`（Intel），打开 DMG 将 Recordly 拖入「应用程序」，首次录屏需在「系统设置 → 隐私与安全性」授予屏幕录制和麦克风权限。
- **Linux：** 下载 `Recordly-linux-x64.AppImage`，赋予可执行权限 `chmod +x Recordly-linux-x64.AppImage` 后直接运行。

## 验证方法

- 打开 Recordly 主界面，点击「+ Record new」能够唤起屏幕/窗口选择框，完成一次短录制后能直接进入带有自动缩放时间线和背景样式调节的编辑器界面并导出 MP4 或 GIF。

## 常见问题

- **macOS 无法录制屏幕画面或音频：** 打开「系统设置 → 隐私与安全性 → 屏幕录制 / 麦克风」，勾选 Recordly 后重启应用。
- **macOS 提示“无法验证开发者”：** 需用户确认后在「系统设置 → 隐私与安全性」底部点击“仍要打开”。
- **Windows 捕获或音频异常：** 确认系统为 Windows 10 Build 19041 及以上版本，以支持原生 Windows Graphics Capture 与 WASAPI 音频捕获。
