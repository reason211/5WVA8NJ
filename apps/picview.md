# PicView

- 项目主页：https://github.com/Ruben2776/PicView（GPL-3.0 许可），官网 https://picview.org
- 作用：看图软件。打开快、没有广告弹窗、不收集数据；常见图片、动图、SVG、HEIC、PSD、相机 RAW、漫画压缩包（CBZ/CBR）等七十多种格式都能直接看。按 G 打开缩略图墙，按 C 裁剪，还能批量改尺寸、转格式、压缩，在标题栏直接重命名。
- 支持系统：Windows 10/11（64 位，x64 和 ARM 都有）、macOS（Apple 芯片和 Intel 都有）。

## 下载渠道（只用官方）

1. GitHub Releases：https://github.com/Ruben2776/PicView/releases/latest
   - Windows 安装版：`Setup-PicView-v<版本>-win-x64.exe`（ARM 电脑用 `win-arm64.exe`）
   - Windows 免安装版：`PicView-v<版本>-win-x64.zip`（ARM 电脑用 `win-arm64.zip`）
   - macOS：Apple 芯片下载 `PicView-<版本>-macOS-arm64.dmg`，Intel 芯片下载 `PicView-<版本>-macOS-x64.dmg`
2. 官网下载页：https://picview.org/download （同样是上面这些安装包）
- README 里列的第三方镜像站不要用。

## 安装步骤

- Windows：双击 `Setup-…exe`，按提示完成安装，开始菜单里会出现 PicView。用免安装版时，解压 zip 后运行里面的 `PicView.exe`。
- macOS：打开 dmg，把 PicView 拖进「应用程序」。
- 想双击图片就用 PicView 打开：在 PicView 设置的「File associations」里勾选格式，或在系统的「默认应用」里把图片的打开方式改成 PicView。改默认应用前先问用户。
- 界面语言默认跟随系统；不是中文时，在设置的「Language」里选简体中文。

## 验证方法

- 打开任意一张图片能正常显示；按 G 能打开缩略图墙，按 C 能进入裁剪。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
