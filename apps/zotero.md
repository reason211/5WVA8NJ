# Zotero

- 项目主页：https://github.com/zotero/zotero（AGPL-3.0 许可），官网 https://www.zotero.org
- 作用：文献管理和读文献。收集、整理论文和电子书，内置阅读器能打开 PDF、EPUB 和网页快照，直接划线、写批注，再把批注一键汇总成笔记；还能按引用格式生成参考文献。
- 支持系统：Windows、macOS、Linux（另有 iOS、安卓版）。

## 下载渠道（只用官方）

1. 官网下载页：https://www.zotero.org/download/ （页面会按当前系统给出对应安装包）
2. 直链（官方稳定版）：
   - Windows 64 位：https://www.zotero.org/download/client/dl?channel=release&platform=win-x64
   - macOS：https://www.zotero.org/download/client/dl?channel=release&platform=mac
   - Linux 64 位：https://www.zotero.org/download/client/dl?channel=release&platform=linux-x86_64
- 只装桌面端即可。下载页上的浏览器插件（Zotero Connector）是可选项，用户没要求就不装；用户想在浏览器里点一下就把论文存进 Zotero（视频里演示的功能）时，再从官网下载页给他当前用的浏览器装上 Connector。

## 安装步骤

- Windows：双击下载的 `Zotero-<版本>_x64_setup.exe`，按提示完成安装，开始菜单里会出现 Zotero。
- macOS：打开下载的 `.dmg`，把 Zotero 拖进「应用程序」，之后可以推出并删除 `.dmg`。
- Linux：解压官方 tarball，在解压目录里运行 `zotero`；想加到启动器，运行目录里的 `set_launcher_icon` 脚本，再把 `zotero.desktop` 软链接到 `~/.local/share/applications/`。
- 第一次打开时界面语言跟随系统，中文系统直接是简体中文；也可以在「编辑 → 设置 → 高级 → 语言」（macOS 是「Zotero → 设置」）里改。

## 验证方法

- 打开 Zotero 能看到“我的文库”；把任意一个 PDF 拖进窗口，双击就能在内置阅读器里打开并划线。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **升级：** Zotero 默认自动更新，也可以在「帮助 → 检查更新」手动升级；直接覆盖安装新版本不会丢数据。
