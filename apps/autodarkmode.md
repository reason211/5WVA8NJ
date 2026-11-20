# Auto Dark Mode

- 项目主页：https://github.com/AutoDarkMode/Windows-Auto-Night-Mode（GPL-3.0 许可），官网 https://autodarkmode.app
- 作用：Windows 自动深浅色模式切换工具。按自定义时间、日出日落时间或环境光自动切换系统和应用主题，支持同步更换壁纸、鼠标指针、系统强调色与任务栏颜色，并可在玩游戏或特定应用运行时自动暂停切换。
- 支持系统：仅 Windows 10（22H2 及以上）和 Windows 11
- **注意：** 这款软件只支持 Windows。如果用户用的是 macOS 或 Linux，如实说明，不要尝试安装。

## 下载渠道（按优先级）

1. GitHub Releases（推荐）：https://github.com/AutoDarkMode/Windows-Auto-Night-Mode/releases/latest
   - Windows 64 位安装版：`AutoDarkMode_Setup_<版本>_x86.exe`
   - Windows 64 位便携版：`AutoDarkMode_<版本>_x86.zip`
   - Windows ARM64 安装版：`AutoDarkMode_Setup_<版本>_ARM64.exe`
   - Windows ARM64 便携版：`AutoDarkMode_<版本>_ARM64.zip`
2. Windows 包管理器 winget：`winget install AutoDarkMode.AutoDarkMode`（或 `winget install autodarkmode`）
3. 微软商店（Microsoft Store）：搜索并安装 `Auto Dark Mode`（商店页 `XP8JK4HZBVF435`）

## 安装步骤

- **Windows（安装版）：** 下载对应架构的 `AutoDarkMode_Setup_<版本>_*.exe`（或通过 winget / 微软商店安装），不需要管理员权限，双击安装包按向导即可完成。
- **Windows（便携版）：** 下载对应 `.zip` 压缩包，解压到固定目录后直接双击运行 `AutoDarkModeApp.exe`。
- **简体中文界面：** 软件内置多语言支持，在系统为中文环境时通常自动显示简体中文，也可在左下角 `Settings` 中调整语言。

## 验证方法

- 打开 Auto Dark Mode 主窗口，在 `Time` 页面打开自动切换开关并设置昼夜时间，或点击托盘图标测试手动切换深浅色主题，桌面、任务栏与应用颜色能立即正常切换。

## 常见问题

- **浏览器或系统弹出安全提醒：** 官方说明因项目未购买商业开发者证书，下载时可能出现浏览器或 SmartScreen 提示。确认文件来自上述官方渠道并核对 Releases 页面提供的 `.sha256` 校验值后，先向用户说明原因，再点击「更多信息 → 仍要运行」。
- **为什么到点没切换：** 检查 `Conditions` 页面是否开启了“玩游戏时不切换”或“特定应用运行时暂停”，或托盘里是否手动勾选了延迟切换。
