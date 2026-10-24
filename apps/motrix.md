# Motrix

- 项目主页：https://github.com/agalwood/Motrix ，官网 https://motrix.app
- 作用：全功能下载管理器，支持 HTTP、FTP、BT 种子、磁力链接；仪表板显示速度和任务；多套限速模式；重启后自动恢复未完成任务；下载完成系统通知；浏览器扩展（Chrome、Edge、Firefox）一键把网页下载交给 Motrix；深色模式；简体中文界面。
- 支持系统：Windows、macOS、Linux。
- 只下载你有权获取的内容。

## 下载渠道

- GitHub Releases：https://github.com/agalwood/Motrix/releases/latest
  - Windows：安装版 `Motrix-Setup-版本号.exe`（ARM 电脑选 `-arm64.exe`），或免安装的 `Motrix-版本号-win.zip`
  - macOS：Apple 芯片选 `Motrix-版本号-arm64.dmg`，Intel 选 `Motrix-版本号-x64.dmg`
  - Linux：`.AppImage` / `.flatpak` / `.pacman` 等

## 安装步骤

- Windows：运行 `Motrix-Setup-版本号.exe` 按提示安装；免安装版解压到固定目录后运行 `Motrix.exe`。
- macOS：打开 `.dmg`，把 Motrix 拖进「应用程序」。
- Linux：`.AppImage` 加执行权限后运行。

## 首次使用

- 从 1.x 升级的用户：先备份旧版配置和下载文件，再按应用内迁移助手操作（见仓库 `docs/legacy-migration.md`）。
- 浏览器扩展：https://github.com/motrixapp/motrix-extension

## 验证方法

- 打开后能看到「仪表板」，引擎状态显示「就绪」。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
