# Upscayl：免费 AI 图片放大

- 项目主页：https://github.com/upscayl/upscayl（AGPL-3.0 许可）
- 作用：用 AI 把模糊、低分辨率的图片放大并变清晰，在本机运行。
- 支持系统：Windows、macOS 12 及以上、Linux。需要支持 Vulkan 的显卡（大多数近几年的电脑都支持）。

## 下载渠道（按优先级）

1. 官网：https://upscayl.org/#download
2. GitHub Releases：https://github.com/upscayl/upscayl/releases/latest
   - Windows：`upscayl-版本号-win.exe`
   - macOS：`upscayl-版本号-mac.dmg`
   - Linux：`upscayl-版本号-linux.AppImage`
3. macOS 也可以用 Homebrew：`brew install --cask upscayl`（仅当用户电脑已经装有 Homebrew 时使用）。

## 安装步骤

- Windows：双击 `.exe`，按提示安装。
- macOS：打开 `.dmg`，把 Upscayl 拖进「应用程序」。

## 验证方法

- 打开 Upscayl，选择一张图片，点击「Upscayl」，能输出放大后的图片。

## 常见问题

- **macOS 提示“无法验证开发者”：** 确认来自官方渠道后，到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
- **提示显卡不支持：** 说明这台电脑的显卡不支持 Vulkan，如实告诉用户。
- 只处理用户有权使用的图片。
