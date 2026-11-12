# LunaTranslator（日文游戏实时翻译）

- 项目主页：https://github.com/HIllya51/LunaTranslator （GPL-3.0）
- 官方文档：https://docs.lunatranslator.org/zh/
- 作用：玩日文视觉小说等游戏时，从游戏里读出台词并实时翻译成中文；读不到的可以截图识别（OCR）；还支持假名注音、语音朗读、生词加进 Anki。
- 支持系统：Windows 10（1803 及以上）/ Windows 11

## 下载渠道（按优先级）

1. GitHub Releases：https://github.com/HIllya51/LunaTranslator/releases/latest
2. 官方文档下载页：https://docs.lunatranslator.org/zh/README.html

普通电脑下载 `LunaTranslator_x64.zip`。`_x64_win7` 和 `_x86_winxp` 是给旧系统的兼容版，官方不建议普通用户使用。

## 安装步骤

1. 把压缩包解压到一个普通文件夹，例如 `D:\LunaTranslator`。**不要**放到 `C:\Program Files` 这类系统目录，否则可能无法保存设置。
2. 双击 `LunaTranslator.exe` 启动。

## 第一次使用

- 先打开游戏，再在 LunaTranslator 的工具栏里点“选择进程”，选中游戏进程；或者直接把游戏的 exe 拖到 LunaTranslator 窗口里。
- 让游戏显示几句台词，在“选择文本”窗口里勾选和游戏台词一致的那一行，就开始翻译。
- 翻译源在设置里选。百度、有道、DeepL 等官方 API 需要用户自己申请密钥，由用户本人填写，不要代填，也不要记录。

## 验证方法

- LunaTranslator 能正常启动，工具栏显示出来。

## 常见问题

- **杀毒软件报毒或提示“找不到重要组件”：** 官方文档说明，为了从游戏里读出文字，软件要把 DLL 注入游戏进程，所以容易被误报。确认文件来自上面的官方渠道后，把 LunaTranslator 文件夹加入杀毒软件的排除项，再重新解压。执行前先告诉用户原因。
- **部分游戏读不到文字：** 文档说部分游戏需要用 `LunaTranslator_admin.exe`（管理员模式）启动才能读取；或改用 OCR 模式框选台词区域。
