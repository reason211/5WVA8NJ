# Shutter Encoder

- 项目主页：https://github.com/paulpacifico/shutter-encoder（GPL-3.0 许可），官网 https://www.shutterencoder.com
- 作用：视频、音频、图片的压缩和格式转换（基于 FFmpeg 的图形界面）。在「File size」里填想要的文件大小，它会自动算出码率来压；支持 H.264、H.265、AV1、ProRes 等常见编码，能裁剪画面、调亮度对比度和颜色、加字幕或水印，还能把多个文件排队批量处理。
- 支持系统：Windows（64 位）、macOS（Intel 和 Apple 芯片）、Linux。

## 下载渠道（只用官方）

1. 官网下载区：https://www.shutterencoder.com/#downloads （页面列出当前版本的各平台安装包）
   - Windows：`Shutter Encoder <版本> Windows 64bits.exe`
   - macOS Apple 芯片：`Shutter Encoder <版本> Apple Silicon.pkg`；Intel：`Shutter Encoder <版本> Mac 64bits.pkg`
   - Linux：`Shutter Encoder <版本> Linux 64bits.deb` 或 `.AppImage`
- GitHub Releases 页面只有源码，没有安装包，以官网为准。
- 官网的捐赠按钮是自愿的，不付费也能直接下载使用。

## 安装步骤

- Windows：双击 `.exe`，按提示完成安装，开始菜单里会出现 Shutter Encoder。
- macOS：先用「关于本机」确认芯片类型，双击对应的 `.pkg`，按提示安装到「应用程序」。
- Linux：Debian/Ubuntu 用 `sudo apt install ./"Shutter Encoder <版本> Linux 64bits.deb"`；其他发行版给 AppImage 加执行权限后直接运行。
- 界面语言默认跟随系统；不是中文时，点窗口左上角齿轮进入设置，在语言里选中文，重启后生效。

## 验证方法

- 打开 Shutter Encoder，把一个视频拖进左侧「Choose files」，在「Choose function」里选 H.264，点「Start function」，进度条走到 100% 后在原文件旁边能看到新文件。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
- **安装包较大（约 150 MB）：** 里面自带 FFmpeg 等组件，下载时间稍长属于正常。
