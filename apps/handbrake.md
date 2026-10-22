# HandBrake

- 项目主页：https://github.com/HandBrake/HandBrake
- 作用：视频太大 一键压缩。几乎所有格式都能读；设备预设一键选；H.265 · AV1 高压缩。
- 支持系统：Windows / macOS（部分还有 Linux、手机版）

## 下载渠道（按优先级）

1. 官网：https://handbrake.fr
2. GitHub Releases：https://github.com/HandBrake/HandBrake/releases/latest

按系统选择文件（文件名会随版本变化，以 Releases 页面为准）：

| 系统 | 参考文件名 |
|---|---|
| Windows | HandBrake-1.11.2-arm64-Win_GUI.exe、HandBrake-1.11.2-arm64-Win_GUI.zip、HandBrake-1.11.2-x86_64-Win_GUI.exe |
| Mac 苹果芯片 | HandBrake-1.11.2.dmg、HandBrakeCLI-1.11.2.dmg |

## 安装步骤

- Windows：运行安装包按提示安装；免安装版解压后直接打开。
- macOS：打开 `.dmg`，把应用拖进「应用程序」。

## 验证方法

- HandBrake 能正常打开主界面。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
