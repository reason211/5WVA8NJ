# BongoCat

- 项目主页：https://github.com/ayangweb/BongoCat （Apache-2.0）
- 作用：开源免费的桌面宠物（桌面陪伴应用）。一只 Live2D 小猫趴在屏幕上，眼睛和爪子跟着鼠标移动；按下键盘、鼠标或手柄按键时，它会做出对应的动作。内置标准（键盘 + 鼠标）、键盘、手柄三种模式，也可以导入自定义模型。离线运行，不联网、不收集数据。
- 支持系统：Windows、macOS（Intel 和 Apple 芯片）。
- 界面支持简体中文。

## 下载渠道

- GitHub Releases：https://github.com/ayangweb/BongoCat/releases/latest
- 写作本教程时的版本是 2.4.1，文件名以 Releases 页面为准：

| 系统 | 文件 |
|---|---|
| Windows 64 位 | `BongoCat_<版本>_x64.exe` |
| macOS Apple 芯片（M 系列） | `BongoCat-<版本>-aarch64.dmg` |
| macOS Intel 芯片 | `BongoCat-<版本>-x64.dmg` |

- 先用 `uname -m`（macOS）判断芯片：`arm64` 选 aarch64，`x86_64` 选 x64。

## 安装步骤

- **Windows：** 双击 `.exe`，按提示完成安装。若出现 SmartScreen「Windows 已保护你的电脑」，先告诉用户原因，再点「更多信息」→「仍要运行」。
- **macOS：** 打开 `.dmg`，把 BongoCat 拖进「应用程序」。首次打开如果提示「已损坏，无法打开」，双击安装包里的 **Fix Damaged App** 按提示修复（作者在 issue #69 给出的官方方法）；也可以在终端执行 `xattr -cr /Applications/BongoCat.app`。执行前先告诉用户原因。
- macOS 首次运行会请求「输入监控」或「辅助功能」权限（小猫需要感知按键），按提示到「系统设置 → 隐私与安全性」里打开 BongoCat 的开关，由用户自己点击确认。

## 使用方法（告诉用户）

1. 打开后小猫出现在屏幕上，随便敲键盘、动鼠标，它就跟着拍桌子、看鼠标。
2. 点托盘（macOS 菜单栏）里的 BongoCat 图标打开设置：「模型库」里切换标准、键盘、手柄模式，也能导入自己的模型。
3. 小猫窗口可以拖到任意位置；「模型窗口」「模型行为」里还有更多显示选项。
4. 插上手柄后切到手柄模式，按手柄按键小猫会同步动作。

## 验证方法

- 屏幕上出现小猫，按键时小猫有动作。

## 常见问题

- **macOS 按键没反应：** 到「系统设置 → 隐私与安全性 → 输入监控 / 辅助功能」打开 BongoCat，然后重启应用。
- 更多模型可以在作者的 Awesome-BongoCat 仓库查看，仅下载你有权使用的模型。
