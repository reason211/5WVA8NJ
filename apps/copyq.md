# CopyQ（剪贴板历史管理）

上游项目：https://github.com/hluk/CopyQ （GPL-3.0）；官网：https://hluk.github.io/CopyQ/ ；文档：https://copyq.readthedocs.io

CopyQ 会在后台记下你复制过的文字、网页和图片，以后可以翻回去找、再粘贴到任何软件里。支持 Windows、macOS 13 及以上、Linux。

## 安装前

先确认用户的系统。告诉用户：CopyQ 会保存他复制过的内容（默认每个标签最多 200 条），如果经常复制密码，建议装好后按下面“隐私设置”处理。

## 安装（只用官方渠道）

最新版在 GitHub Releases：https://github.com/hluk/CopyQ/releases/latest

- Windows：下载 `copyq-<版本>-setup.exe`，双击按提示安装；不想安装就下载 `copyq-<版本>.zip`，解压后运行 `copyq.exe`。
- macOS：Apple 芯片下载 `CopyQ-<版本>-macos-13-m1.dmg`，Intel 芯片下载 `CopyQ-<版本>-macos-13.dmg`，把 CopyQ 拖进「应用程序」。打开时如果提示“已损坏”或“无法打开”，按官方 README 里的说明处理，执行前先告诉用户原因。
- Linux：下载 `CopyQ-<版本>-x86_64.AppImage`，加上可执行权限后运行；也可以用发行版自带的软件源安装。
- `CopyQ-<版本>.tar.gz` 是源码包，普通用户不用下载。

## 第一次使用

- 打开后 CopyQ 常驻在系统托盘（macOS 在屏幕右上角菜单栏），图标是一把带眼睛的小剪刀。点它就能打开历史窗口。
- 界面语言可以在「File → Preferences → General → Language」里改成简体中文。
- 想用快捷键呼出历史，在「Preferences → Shortcuts」里给“显示/隐藏主窗口”设一个全局快捷键，由用户自己挑按键。

## 隐私设置（建议告诉用户）

- 不想记录密码软件里复制的内容：按官方 FAQ（https://copyq.readthedocs.io/en/latest/faq.html ）添加“Ignore *Password* window”这类自动命令。
- 想给整个历史加密：在「Preferences」勾选 **Encrypt Tabs**，密码由用户本人设置，不要代填，也不要记录。

## 验收与交付

确认 CopyQ 已在运行、托盘里能看到图标；请用户随便复制一段文字，历史窗口里出现这一条就算装好了。告诉用户软件装在哪里、怎么打开、怎么退出和卸载。没有实际完成的设置，不要报告为已完成。
