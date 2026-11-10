# GIMP

- 项目主页：https://gitlab.gnome.org/GNOME/gimp（GitHub 只读镜像 https://github.com/GNOME/gimp，GPL-3.0 许可），官网 https://www.gimp.org
- 作用：免费开源的修图和画图软件。图层、蒙版、选区、曲线和色阶调色、饱和度等滤镜都有；3.0 起滤镜默认挂在图层上（非破坏编辑），之后还能回头改、开关或删除；能打开和导出 PSD 文件，支持 JPEG XL、WebP 等常见图片格式。
- 支持系统：Windows 10 及以上、macOS（Intel 和 Apple 芯片）、Linux。

## 下载渠道（只用官方）

1. 官网下载页：https://www.gimp.org/downloads/ （按系统给出当前稳定版）
   - Windows：`gimp-<版本>-setup.exe`
   - macOS Apple 芯片：`gimp-<版本>-arm64.dmg`；Intel：`gimp-<版本>-x86_64.dmg`
   - Linux：Flathub 的 `org.gimp.GIMP`，或官网的 `GIMP-<版本>-x86_64.AppImage`
2. 安装包都放在官方下载服务器 https://download.gimp.org/gimp/ 上。

## 安装步骤

- Windows：双击 `setup.exe`，选「为所有用户安装」或「仅为我安装」，按提示完成，开始菜单里会出现 GIMP。
- macOS：先用「关于本机」确认芯片类型，打开对应的 `.dmg`，把 GIMP 拖进「应用程序」。
- Linux：`flatpak install flathub org.gimp.GIMP`；或给 AppImage 加执行权限后直接运行。
- 界面语言默认跟随系统，中文系统直接是简体中文；也可以在「编辑 → 首选项 → 界面 → 语言」里改，重启后生效。

## 验证方法

- 打开 GIMP，用「文件 → 打开」打开一张图片，在「颜色 → 曲线」里拖动曲线，画面颜色跟着变化。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
- **第一次启动较慢：** 首次启动要扫描字体和插件，等一两分钟属于正常。
