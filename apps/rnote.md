# Rnote

- 项目主页：https://github.com/flxzt/rnote（GPL-3.0 许可），官网 https://rnote.flxzt.net
- 作用：手写笔记和画图。用手写笔（数位板、触屏笔）在电脑上记笔记，有压感，下笔越重线越粗；画布可以设成固定页、向下无限延伸或四面无限；能导入 PDF 和图片直接在上面批注；框选后能移动、旋转、缩放；多个笔记用标签页同时打开；能导出成 PDF、SVG、PNG、JPEG。面向学生和老师。
- 支持系统：Windows 10/11（64 位）、macOS（Apple 芯片和 Intel，由官方 README 推荐的打包版提供）、Linux（Flathub）。

## 下载渠道（只用官方 README 列出的渠道）

1. Windows：GitHub Releases https://github.com/flxzt/rnote/releases/latest ，下载 `rnote-win-installer-<版本>-x86_64.exe`。
2. macOS：官方 README 指向的打包版 https://gitlab.com/dehesselle/rnote_macos/-/releases/permalink/latest ，Apple 芯片下载 `Rnote-<版本>_arm64.dmg`，Intel 芯片下载 `Rnote-<版本>_x86_64.dmg`。
3. Linux：Flathub https://flathub.org/apps/details/com.github.flxzt.rnote 。

## 安装步骤

- Windows：双击安装包，按提示完成安装，开始菜单里会出现 Rnote。
- macOS：打开 dmg，把 Rnote 拖进「应用程序」。
- Linux：`flatpak install flathub com.github.flxzt.rnote`。

## 验证方法

- 打开 Rnote，用鼠标或手写笔在画布上画一笔能看到笔迹；点左上角的「+」能新建标签页。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
- **文件格式提醒：** 官方说明 `.rnote` 格式还在变化，新旧版本之间可能打不开。重要笔记建议同时导出一份 PDF。
