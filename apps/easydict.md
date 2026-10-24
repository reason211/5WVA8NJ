# Easydict

- 项目主页：https://github.com/tisfeng/Easydict（GPL-3.0 许可）
- 作用：macOS 上的查词和翻译工具。选中文字弹出翻译，快捷键输入查词，截图识别文字并翻译；可同时使用 20 多个词典、翻译和 AI 服务（苹果词典、DeepL、谷歌、必应等）。
- 支持系统：仅 macOS。最新版需要 macOS 13 或更高版本；更老的系统用 2.7.2 版（https://github.com/tisfeng/Easydict/releases/tag/2.7.2）。
- **注意：** 这款软件只支持 macOS。用户是 Windows 时，如实说明，不要尝试安装。

## 下载渠道（按优先级）

1. Homebrew：`brew install --cask easydict`（README 推荐方式）
2. GitHub Releases：https://github.com/tisfeng/Easydict/releases/latest（文件名 `Easydict.dmg`，附带 `SHA256SUMS.txt` 校验值）

## 安装步骤

- macOS：打开 `.dmg`，把 Easydict 拖进「应用程序」。下载后用 `shasum -a 256 Easydict.dmg` 和 `SHA256SUMS.txt` 核对。

## 首次使用

- 打开后按提示授予「辅助功能」权限（划词翻译需要）和「屏幕录制」权限（截图翻译需要）。授权前先告诉用户原因。
- 默认快捷键：输入翻译 ⌥ + A，划词翻译 ⌥ + D，截图翻译 ⌥ + S。

## 验证方法

- 按 ⌥ + A 能弹出输入框，输入单词回车后显示查词结果。

## 常见问题

- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
