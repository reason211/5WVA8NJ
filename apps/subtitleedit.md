# Subtitle Edit

- 项目主页：https://github.com/SubtitleEdit/subtitleedit （MIT），官方文档 https://subtitleedit.github.io/subtitleedit/
- 作用：免费开源的字幕编辑器，离线运行，不收集你的字幕和视频内容。导入视频后可以用 Whisper 等语音识别引擎自动生成字幕；下方显示声音波形，对着波形调每句字幕的出现和消失时间；可以一键自动翻译，原文和译文左右对照；能把字幕直接烧进视频（字体、颜色、描边、阴影都能调）；「修复常见错误」能一键修好多余空格、显示时间太短等问题；还支持批量转换字幕格式（SRT、ASS 等）。
- 支持系统：Windows 10（22H2 及以上）/ 11、macOS 12 及以上、Linux。
- 界面支持简体中文。

## 下载渠道（按优先级）

- GitHub Releases：https://github.com/SubtitleEdit/subtitleedit/releases （选标着 Latest 的稳定版，不要装 pre-release 预发布版）
  - Windows 64 位安装版：`SubtitleEdit-Windows-x64-Setup.exe`
  - Windows 64 位便携版（免安装，解压即用）：`SubtitleEdit-Windows-x64.zip`；ARM64 电脑用 `SubtitleEdit-Windows-ARM64.zip`
  - macOS：苹果芯片用 `SubtitleEdit-macOS-ARM64.dmg`，Intel 芯片用 `SubtitleEdit-macOS-x64.dmg`（已签名公证，双击即可打开）
  - Linux：`SubtitleEdit-linux-x64.flatpak`
- 写作本教程时的稳定版本是 5.3.0。下载前先打开 Releases 页确认有没有更新的稳定版。

## 安装步骤

1. 先判断系统和架构：Windows 用 `$env:PROCESSOR_ARCHITECTURE`（AMD64 或 ARM64），Mac 用 `uname -m`（arm64 或 x86_64）。
2. Windows：下载安装版，双击运行，按向导点「下一步」装完；用户想免安装时，下载便携版 zip 解压到用户目录（例如 `%USERPROFILE%\Apps\SubtitleEdit\`），双击里面的 `SubtitleEdit.exe`。
3. macOS：下载对应芯片的 dmg，双击挂载，把 `Subtitle Edit.app` 拖进「应用程序」文件夹，再从启动台打开。
4. 装好后告诉用户软件位置（安装版在开始菜单搜「Subtitle Edit」，便携版就是解压出来的 exe，Mac 在「应用程序」里）。

## 使用方法（告诉用户）

1. 把视频拖进窗口，或「视频」菜单 → 打开视频；字幕文件（.srt / .ass 等）直接拖进来就能编辑。
2. 自动生成字幕：「视频」→「语音转文字」，引擎选 Whisper CPP，选模型和视频语言，点「转录」（Transcribe）。第一次用会提示下载引擎和模型，点确认即可；模型越大越准、越慢。
3. 对时间轴：下方是声音波形，拖动每句字幕块的左右边缘调整出现和消失时间。
4. 自动翻译：「翻译」→「自动翻译」，选翻译引擎和源语言、目标语言，点「翻译」，原文和译文会左右对照显示，确认后点「确定」。
5. 硬字幕：「视频」→「生成带烧录字幕的视频」，设好字体、大小、颜色、描边，点「生成」。
6. 修小错误：「工具」→「修复常见错误」，勾选规则后点下一步，确认要修的项目再应用。

## 验证方法

- 能打开 Subtitle Edit，看到主窗口（上方字幕列表、右侧视频预览、下方波形区域）。

## 常见问题

- **界面是英文：** 在菜单 Options（选项）里找到语言（Language）设置，选「简体中文」（ChineseSimplified）。
- **杀毒软件提示风险：** 只从上面的 GitHub Releases 下载，核对文件名和版本号；维护者对杀软误报的说明见 issue #12837、#13900。不要从第三方下载站下载。
- **语音识别慢：** 换小一点的模型（tiny、base），或有 NVIDIA 显卡时在 Backend 里选 cuBLAS。
