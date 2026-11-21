# KDE Connect

- 项目主页：https://github.com/KDE/kdeconnect-kde（GPL-2.0 / GPL-3.0 许可），官网 https://kdeconnect.kde.org
- 作用：跨设备无线互联工具，让手机和电脑在同一局域网下加密直连互通。支持手机当电脑无线触控板与 PPT 翻页遥控器、手机电脑剪贴板共享、无线互传文件、电脑端同步查看手机通知与电量，以及一键让静音手机响铃找手机。
- 支持系统：Windows、macOS、Linux、Android、iOS / iPadOS

## 下载渠道（按优先级）

1. 官网下载页：https://kdeconnect.kde.org/download.html
2. Windows：
   - 微软商店（Microsoft Store）：搜索 `KDE Connect`（商店页 `9N93MRMSXBF0`）
   - 官方安装包：`https://download.kde.org/stable/release-service/` 对应版本 `windows/kdeconnect-kde-windows-*.exe`
3. macOS：
   - 官网稳定版 `.dmg`（如 `kdeconnect-kde-macos-clang-arm64.dmg`）
4. 手机端：
   - Android：F-Droid（`org.kde.kdeconnect_tp`）或 Google Play、GitHub/KDE 官方 APK
   - iPhone / iPad：App Store 搜索 `KDE Connect`（`id1580245991`）

## 安装步骤

- **电脑端（Windows / macOS）：** 通过微软商店安装或运行官方 `.exe` 安装包（macOS 打开 `.dmg` 将应用拖入「应用程序」文件夹）。
- **手机端：** 在 Android 或 iPhone 上安装 KDE Connect App，确保手机与电脑连接同一个局域网 Wi-Fi。
- **配对连接：** 两端同时打开 KDE Connect，在列表里看到对方设备名称后发起配对，另一端点击确认即可开始使用（若 Windows 防火墙弹窗提示网络权限，允许专用网络放行）。

## 验证方法

- 打开电脑端与手机端的 KDE Connect，设备状态显示为已配对连接；在手机上点击「远程输入」移动手指可实时控制电脑光标，或点击「发送文件」能将图片直接传到电脑下载目录。

## 常见问题

- **同一个 Wi-Fi 下搜不到设备：** 检查手机和电脑是否连在同一个路由器子网（避免一个连访客 Wi-Fi），或临时确认 Windows 防火墙未拦截局域网 UDP 1714–1764 端口。
- **macOS 提示无法验证开发者：** 若下载未公证版本首次被拦截，向用户说明后到「系统设置 → 隐私与安全性」点击「仍要打开」。
