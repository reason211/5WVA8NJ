# LocalSend

- 项目主页：https://github.com/localsend/localsend（Apache-2.0 许可），官网 https://localsend.org
- 作用：在同一局域网内的设备之间互传文件和消息，不需要互联网，不经过外部服务器，HTTPS 加密传输。
- 支持系统：Windows、macOS、Linux、Android、iOS。

## 下载渠道（按优先级）

- Windows：Microsoft Store、Winget（`winget install LocalSend.LocalSend`），或 GitHub Releases 的 EXE 安装包 / 便携版 ZIP
- macOS：App Store、Homebrew（`brew install --cask localsend`），或 GitHub Releases 的 DMG
- Linux：Flathub、Snap、DEB、AppImage 等
- Android：Google Play、F-Droid，或 GitHub Releases 的 APK
- iOS：App Store
- GitHub Releases：https://github.com/localsend/localsend/releases/latest

官方建议优先用应用商店或包管理器安装，因为应用本身没有自动更新。

## 安装步骤

- 电脑端：按上面的渠道安装后打开 LocalSend。
- 手机端：告诉用户在手机应用商店搜索 “LocalSend” 安装（或把 APK 传到安卓手机安装）。

## 首次使用

- 手机和电脑连同一个 Wi-Fi，两边都打开 LocalSend，就能在「发送」页看到对方。
- 首次运行时系统可能询问是否允许局域网访问 / 防火墙放行，需要允许。执行前先告诉用户原因。

## 验证方法

- 电脑端「接收」页显示本机名字（如 “Fast Papaya”），手机端能在「发送」页看到这台电脑。
