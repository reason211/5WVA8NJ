# PowerToys

- 项目主页：https://github.com/microsoft/PowerToys（MIT 许可），官方文档 https://learn.microsoft.com/zh-cn/windows/powertoys/
- 作用：微软官方免费工具箱，三十多个小工具：FancyZones 窗口分区、Image Resizer 右键改图片尺寸、PowerRename 批量重命名（改前预览）、取色器（Win+Shift+C）、Command Palette 快速搜索、文字识别等。
- 支持系统：Windows 10、Windows 11（x64 / arm64）。
- **注意：** 这款软件不支持 macOS。用户是 Mac 时，如实说明并推荐清单里支持 Mac 的软件，不要尝试安装。

## 下载渠道（按优先级）

1. 微软商店（国内可直接访问，推荐）：https://apps.microsoft.com/detail/XP89DCGQ3K6VLD ，或在微软商店里搜索「PowerToys」。
2. WinGet（系统自带的包管理器）：`winget install Microsoft.PowerToys -s winget`
3. GitHub Releases：https://github.com/microsoft/PowerToys/releases/latest

GitHub Releases 按芯片选择“用户级安装包”（文件名随版本变化，以页面为准）：

| 芯片 | 参考文件名 |
|---|---|
| x64（Intel、AMD，大多数电脑） | PowerToysUserSetup-0.102.3001.0-x64.exe |
| arm64 | PowerToysUserSetup-0.102.3001.0-arm64.exe |

## 安装步骤

1. 优先用微软商店：打开商店页面点「获取 / 安装」，装完在开始菜单打开 PowerToys。
2. 没有商店时用 WinGet 命令安装（默认是当前用户范围，不需要管理员权限）。
3. 前两种都不可用时，从 GitHub Releases 下载对应芯片的 `PowerToysUserSetup-…exe`，双击按提示安装。
4. 安装完成后打开 PowerToys，左侧就是各个工具的开关；告诉用户安装位置和几个常用快捷键：
   - 取色器：`Win + Shift + C`
   - FancyZones：拖动窗口时按住 `Shift`，松手贴进分区；`` Win + Shift + ` `` 打开布局编辑器
   - Image Resizer、PowerRename：在资源管理器里选中文件后右键使用

## 验证方法

- 开始菜单能打开 PowerToys 设置窗口，「主页」里能看到各工具的开关。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **右键菜单里看不到 Image Resizer / PowerRename：** 在 PowerToys 里确认对应工具已打开；Windows 11 先点「显示更多选项」。
- **想全员安装（所有用户）：** 需要管理员权限，执行前先说明并得到用户同意；一般用户级安装就够用。
