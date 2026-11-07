# Stretchly

- 项目主页：https://github.com/hovancik/stretchly（BSD-2-Clause 许可），官网 https://hovancik.net/stretchly
- 作用：电脑休息提醒。默认每 10 分钟弹出 20 秒的短休息，每 30 分钟一次 5 分钟的长休息，休息时给出放松眼睛、伸展身体的小建议；休息前先发通知，可推迟或跳过；人离开电脑或开启勿扰模式时自动暂停。
- 支持系统：Windows、macOS（13 及以上）、Linux。

## 下载渠道（只用官方）

1. GitHub Releases：https://github.com/hovancik/stretchly/releases/latest
2. Windows 也可用 winget：`winget install -e --id Stretchly.Stretchly`
3. macOS 也可用作者的 Homebrew tap：`brew install --cask hovancik/stretchly/stretchly`
- 发布页按系统选择：Windows 选安装包 `.exe`（或便携版），macOS 选与芯片（Apple 芯片或 Intel）对应的 `.dmg`，Linux 选 `.AppImage` 或 `.deb`。不要下载 Source code。

## 安装步骤

- Windows：双击安装包按提示安装；便携版解压后直接打开 `Stretchly.exe`。
- macOS：打开 `.dmg`，把 Stretchly 拖进「应用程序」。应用只做了临时签名，第一次打开会被拦：
  - Intel 芯片：到「系统设置 → 隐私与安全性」点击「仍要打开」。
  - Apple 芯片：在终端运行 `sudo xattr -r -d com.apple.quarantine /Applications/Stretchly.app`（需要用户输入开机密码）。执行前先告诉用户原因，取得同意。
- 装好后 Stretchly 常驻在任务栏托盘（macOS 菜单栏），第一次打开会出现欢迎窗口，可在里面把语言改成简体中文。

## 验证方法

- 托盘或菜单栏出现 Stretchly 图标，点开能看到“下次短休息”的倒计时。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **想改休息间隔或时长：** 点托盘图标 → 偏好设置（Preferences），在“计划”（Schedule）里调整。
