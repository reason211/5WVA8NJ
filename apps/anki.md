# Anki

- 项目主页：https://github.com/ankitects/anki
- 作用：按遗忘曲线背单词和知识点。每张卡片按用户的记忆情况安排复习时间；卡片能放图片、音频；可以导入别人分享的词库。
- 支持系统：Windows / macOS / Linux（安卓有免费的 AnkiDroid，苹果手机版是官方收费应用）

## 下载渠道（按优先级）

1. 官网：https://apps.ankiweb.net
2. GitHub Releases：https://github.com/ankitects/anki/releases/latest

按系统选择文件（文件名会随版本变化，以 Releases 页面为准）：

| 系统 | 参考文件名 |
|---|---|
| Windows 普通电脑 | anki-26.09.4-win-x64.msi |
| Windows ARM 电脑 | anki-26.09.4-win-arm64.msi |
| Mac 苹果芯片 | anki-26.09.4-mac-apple.dmg |
| Mac Intel | anki-26.09.4-mac-intel.dmg |
| Linux | anki-26.09.4-linux-x86_64.tar.zst（ARM 选 aarch64） |

## 安装步骤

- Windows：运行 `.msi` 安装包，按提示安装。
- macOS：打开 `.dmg`，把 Anki 拖进「应用程序」。
- Linux：解压后按包内说明运行安装脚本。

## 第一次使用

- 第一次打开会让用户选界面语言，选「简体中文」。
- 想直接用别人做好的词库：主界面底部点「获取共享牌组」，在 AnkiWeb 上搜到后下载，双击下载的 `.apkg` 文件就会导入。
- 想在手机上接着背：用户自己注册 AnkiWeb 账号后点「同步」。账号和密码由用户本人填写，不要代填，也不要记录。

## 验证方法

- Anki 能正常打开主界面，能看到牌组列表。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
