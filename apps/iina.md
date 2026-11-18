# IINA

- 项目主页：https://github.com/iina/iina（GPL-3.0 许可），官网 https://iina.io
- 作用：专为 macOS 设计的现代开源视频和音频播放器，支持几乎所有常见影音格式、外挂字幕匹配与样式调节、画面比例裁切与色调调整、倍速播放、画中画、音频均衡器以及独立音乐模式。
- 支持系统：仅 macOS（macOS 11.0 及以上，通用版同时支持 Apple Silicon 与 Intel 芯片）。
- **注意：** 这款软件只支持 macOS。用户是 Windows 时，如实说明，不要尝试安装。

## 下载渠道（按优先级）

1. GitHub Releases：https://github.com/iina/iina/releases/latest
   - 通用安装包：`IINA.v*.dmg`
2. 官网下载：https://iina.io/download/

## 安装步骤

1. 下载最新版的 `IINA.v*.dmg` 安装镜像。
2. 双击打开 `.dmg`，将 `IINA.app` 拖入「应用程序（Applications）」文件夹。
3. 从「应用程序」或启动台打开 IINA。

## 验证方法

- 打开 IINA 主界面，确认能正常拖入本地 MP4/MKV 等视频或音频文件流畅播放，且右侧边栏可以调节画面比例、播放速度与字幕样式。

## 常见问题

- **macOS 提示无法验证开发者或来自不明开发者：** 确认文件来自上面列出的官方渠道后，到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
- **如何开启硬件解码与色彩管理：** 打开 IINA「设置 → 视频」，将硬件解码器保持为「自动（Auto）」并开启 ICC 色彩配置文件加载即可。
