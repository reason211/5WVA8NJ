# CompactGUI

- 项目主页：https://github.com/IridiumIO/CompactGUI（GPL-3.0 许可）
- 作用：Windows 原生透明文件压缩图形工具。直接调用 Windows 10/11 内置的 WOF（Windows Overlay Filter）透明压缩机制，在不删除文件、不打成压缩包的前提下，将游戏或大型软件目录原地压小（支持 XPRESS4K / XPRESS8K / XPRESS16K / LZX 四档），随时可一键解压还原；自带 12,809 款游戏社区压缩率估算库与后台更新自动重压监听器。
- 支持系统：Windows 10 / Windows 11（64 位及 ARM64）
- **注意：** 本软件仅支持 Windows 系统；且官方说明不建议用于启用了 Windows 11 DirectStorage 技术的游戏。如果用户的电脑是 macOS 或 Linux，请如实说明，不要尝试安装。

## 下载渠道（按优先级）

1. GitHub Releases：https://github.com/IridiumIO/CompactGUI/releases/latest
   - 64 位 Windows 下载 `CompactGUI.exe`（或便携版本体），ARM64 设备下载 `CompactGUI.arm64.exe`
2. 命令行包管理器（WinGet）：`winget install CompactGUI`

## 安装步骤

1. 从官方 Releases 页面下载 `CompactGUI.exe`（免安装绿色单文件，或通过 `winget install CompactGUI` 安装）。
2. 将 `CompactGUI.exe` 放到常用工具目录（如 `D:\Tools\CompactGUI\`），双击启动（如弹出 SmartScreen 提示，核实来源为官方 Releases 后点「更多信息 → 仍要运行」）。
3. 点击左侧「+ 添加文件夹」选中要瘦身的游戏或软件目录，查看四档预估体积，选择 `XPRESS8K`（速度与体积均衡）或 `LZX`（最大压缩率），点「开始压缩」即可；也可勾选后台监控（Watcher），游戏更新后在电脑空闲时自动重压。

## 验证方法

- 打开 CompactGUI，在主界面添加任意测试文件夹后能分析文件数、原始大小以及 4 档预估压缩结果；切换到「Compression DB」可搜索 12,809 款游戏的社区实测压缩比。
- 压缩完成后，游戏或软件目录在资源管理器中仍可正常双击启动运行。

## 常见问题

- **压缩后怎么恢复原样？** 在 CompactGUI 中选中已压缩的文件夹，点击「解压缩」即可恢复未压缩状态，不会损坏文件。
- **哪些文件不建议压？** 视频、图片或已经加密压缩过的媒体文件，软件会自动跳过压缩率低的文件类型，无需手动逐个挑选。
