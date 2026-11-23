# AB Download Manager

- 项目主页：https://github.com/amir1376/ab-download-manager（Apache-2.0 许可），官网：https://abdownloadmanager.com
- 作用：轻量高速多线程下载器，支持默认 8 线程并发与动态分片接力、断点续传、队列与定时调度、全局限速、浏览器扩展接管及多套深浅主题，无广告弹窗。
- 支持系统：Windows（x64 / ARM64）、macOS（Apple 芯片 / Intel）、Linux（x64 / ARM64）、Android（通用 APK）

## 下载渠道（按优先级）

1. GitHub Releases：https://github.com/amir1376/ab-download-manager/releases/latest
2. 官网下载页：https://abdownloadmanager.com

按系统选择最新安装包（当前最新 v1.11.4）：

| 系统 | 参考文件名 |
|---|---|
| Windows x64 | `ABDownloadManager_*_windows_x64.exe`（安装包）或 `.zip`（免安装绿色版） |
| Windows ARM64 | `ABDownloadManager_*_windows_arm64.exe` 或 `.zip` |
| macOS 苹果芯片 | `ABDownloadManager_*_mac_arm64.dmg` |
| macOS Intel | `ABDownloadManager_*_mac_x64.dmg` |
| Linux x64 / ARM64 | `ABDownloadManager_*_linux_x64.tar.gz` / `linux_arm64.tar.gz` |
| Android | `ABDownloadManager_*_android_universal.apk` |

## 安装步骤

- **Windows：** 运行官方 `.exe` 安装向导完成安装，或直接解压 `.zip` 绿色版打开主程序。
- **macOS：** 打开 `.dmg`，将 AB Download Manager 拖入「应用程序」。
- **Linux / Android：** Linux 解压 `.tar.gz` 后运行；Android 传到手机点 `.apk` 安装。
- **浏览器接管（可选）：** Chrome/Edge 或 Firefox 安装对应的官方 `AB Download Manager` 扩展即可接管网页下载。

## 验证方法

- 主程序能够正常打开下载列表界面，点击左上角 `Add URL` 可填入测试下载链接并查看分块进度与速度。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认安装包来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
- 请只下载你有权获取的内容，支持正版资源。
