# Loop

- 项目主页：https://github.com/MrKai77/Loop（GPL-3.0 许可）
- 作用：Mac 窗口管理和分屏。按住触发键（默认 fn）把鼠标往某个方向一甩，窗口就移到左半屏、右上角等对应位置；松手前会先框出窗口要去的位置；同一个快捷键连按能在几种位置之间轮换；不用的窗口可以藏到屏幕边上，鼠标靠过去再出来；圆环和预览框的样式、颜色都能改。
- 支持系统：macOS 13 及以上（Apple 芯片和 Intel）。

## 下载渠道（只用官方 README 列出的渠道）

1. GitHub Releases：https://github.com/MrKai77/Loop/releases/latest ，下载 `Loop.zip`。
2. Homebrew：`brew install loop`（电脑已装 Homebrew 时可用）。

## 安装步骤

1. 解压 `Loop.zip`，把 `Loop.app` 拖进「应用程序」。
2. 打开 Loop，按提示到「系统设置 → 隐私与安全性 → 辅助功能」里打开 Loop 的开关（Loop 需要这个权限才能移动其他窗口）。执行前先告诉用户原因。
3. 菜单栏出现 Loop 图标即表示在运行。

## 验证方法

- 随便打开一个窗口，按住 fn 键把鼠标往左移一点再松开，窗口应贴到屏幕左半边。

## 常见问题

- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
- **按住 fn 没反应：** 确认「辅助功能」里 Loop 已打开；也可以在 Loop 设置的 Behavior 页把触发键换成别的键。
