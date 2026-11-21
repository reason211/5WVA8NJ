# Aerial

- 项目主页：https://github.com/pengchujin/aerial-tv （MIT 协议），官网 https://aerial.qust.me
- 作用：给小米、TCL、雷鸟、索尼、创维、海信等国产 Android TV 电视和盒子换上参照 Apple tvOS 设计的极简干净桌面，去掉首页信息流与会员推荐弹窗，自带 114 段航拍屏保与每日壁纸，支持开机自启、主页键接管与手机扫码排序，不用 root、不动系统应用、随时可还原。
- 支持系统：Android TV 5.0 及以上安装完整版（`aerial-standard.apk` 或 `aerial-guard.apk`）；Android 4.0–4.4 老电视安装 `aerial-lite.apk`（测试版）。电脑端支持 Windows / macOS / Linux 通过局域网 ADB 安装（也可把 APK 拷进 U 盘在电视本地安装）。

## 下载渠道（按优先级）

1. 官方最新发布与下载页：
   - GitHub Releases（最新版 v2.13）：https://github.com/pengchujin/aerial-tv/releases/latest
   - 官网直链：
     - 完整版（Android 5.0+ 首选）：https://aerial.qust.me/download/aerial-standard.apk
     - 守护版（当系统禁止安装第三方桌面类 App 时使用）：https://aerial.qust.me/download/aerial-guard.apk
     - 老电视测试版（Android 4.0–4.4）：https://aerial.qust.me/download/aerial-lite.apk
   - 官方安装脚本与指南：https://aerial.qust.me/install.sh 、https://aerial.qust.me/agent.md

## 安装与使用步骤

- **1. 打开电视的 ADB 调试：**
  - 电脑和电视连同一个局域网 Wi-Fi，在电视里记录局域网 IP（设置 → 网络 → 已连接的网络）。
  - 小米 / Redmi：设置 → 关于 → 连续按「产品型号」进入开发者模式，再到「设置 → 账号与安全」打开「ADB 调试」与「安装未知来源的应用」。
  - TCL / 雷鸟：设置 → 关于 → 本机信息，快速按遥控器「上下左右」，在底部「更多」里打开 ADB。
  - 索尼 / 其他原生 Android TV：设置 → 设备偏好设置 → 关于 → 连按「内部版本号」7 次，再到开发者选项里打开「USB 调试」或「无线调试」。
  - 只有「无线调试」的 Android 11+ 机型（如部分索尼/TCL 新系统）：先在无线调试里选「使用配对码配对设备」，记住配对屏 IP:端口与 6 位配对码，再按 `adb pair` 后 `adb connect`。
- **2. 电脑端准备 ADB 并安装（需用户确认电视端调试授权弹窗）：**
  - 检查 `adb version`（若无 adb，macOS 可用 `brew install android-platform-tools`，Windows 可下载 Google 官方 `platform-tools-latest-windows.zip`）。
  - 下载 `aerial-standard.apk`（若系统提示不允许安装桌面类 App 则改用 `aerial-guard.apk`），连接并安装：
    ```bash
    adb connect <电视IP>:5555
    adb install -r aerial-standard.apk
    adb shell pm grant app.orchard.tv android.permission.WRITE_SECURE_SETTINGS
    adb shell cmd notification allow_listener app.orchard.tv/app.orchard.tv.guard.RevivalListener
    adb shell appops set app.orchard.tv SYSTEM_ALERT_WINDOW allow
    adb shell am start -n app.orchard.tv/.MainActivity
    adb shell cmd package compile -m speed -f app.orchard.tv
    ```
  - 也可直接用 macOS / Linux 一行安装脚本（自动识别系统版本并配置待机保活）：
    ```bash
    curl -fsSL https://aerial.qust.me/install.sh | KEEP_ADB=1 TV=<电视IP> bash
    ```
  - 若家里没有电脑操作，也可将 APK 拷入 U 盘插到电视，用电视文件管理器安装后从「我的应用」打开 Aerial，按弹窗指引在电视设置里开启「桌面守护（无障碍）」与「通知使用权」。
- **3. 随时还原原有桌面：**
  - 电脑执行还原命令：`curl -fsSL https://aerial.qust.me/install.sh | TV=<电视IP> bash -s restore`（追加 `--uninstall` 可同时卸载 Aerial）；或从应用列表随时点回电视原有桌面。

## 验证方法

- 在电视上按遥控器「主页（Home）」键后直接进入 Aerial 清爽桌面（顶部时钟天气、底部玻璃底板 App 栏），不跳回原厂广告首页；
- 电脑端可执行验收命令确认桌面状态：
  ```bash
  adb shell "dumpsys window | grep mCurrentFocus"
  ```
  输出包含 `app.orchard.tv` 即表示已成功接管主屏幕。

## 常见问题

- **原厂会员、小爱同学、有线电视和系统设置还在吗？**
  都在。Aerial 不卸载任何系统应用，原来装的视频 App 和系统桌面都能在应用网格里正常打开。
- **按主页键后又跳回原桌面：**
  请在电视设置中确认已授予 Aerial 无障碍「桌面守护」与「通知使用权」权限，或按官方 `install.sh` 补全授权命令。
- **提示「不允许安装桌面类应用」：**
  改下载并安装 `aerial-guard.apk`（无需声明 HOME 桌面权限，通过桌面守护自动接管主页键与开机）。
