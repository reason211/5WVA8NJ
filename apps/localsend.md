# LocalSend：手机电脑互传文件

- 项目主页：https://github.com/localsend/localsend（Apache-2.0 许可）
- 作用：同一个 Wi-Fi 下，在手机、电脑之间互传文件和文字。不经过任何服务器，不限大小，不压缩，不用注册登录。
- 支持系统：Windows 10 及以上、macOS 11 及以上、安卓 7 及以上、iOS 13 及以上、Linux。

## 下载渠道（按优先级）

| 系统 | 首选 | 备选 |
|---|---|---|
| Windows | 微软商店搜索「LocalSend」（应用 ID：9NCB4Z0TZ6RR） | GitHub Releases 里的 `LocalSend-版本号-windows-x86-64.exe`（arm 电脑用 `windows-arm-64.zip`） |
| macOS | Mac App Store 搜索「LocalSend」 | GitHub Releases 里的 `.dmg` 文件 |
| iPhone / iPad | App Store 搜索「LocalSend」 | — |
| 安卓 | 官网 https://localsend.org/download 下载 APK | GitHub Releases 里的 `android-arm64v8.apk` |

GitHub Releases 地址：https://github.com/localsend/localsend/releases/latest

## 安装步骤

1. 按上表为用户的系统选择渠道。应用商店安装最省事，优先使用。
2. 用安装包安装时：Windows 双击 `.exe` 按提示安装；macOS 打开 `.dmg`，把 LocalSend 拖进「应用程序」。
3. 安装完成后打开 LocalSend。

## 验证方法

- LocalSend 能正常打开，首页显示本机的设备名。
- 让用户在手机上也装好 LocalSend，连同一个 Wi-Fi，电脑端「发送」页能看到手机设备。

## 常见问题

- **Windows 搜不到其他设备：** 把当前网络设为「专用网络」（设置 → 网络和 Internet → 当前网络 → 网络配置文件类型 → 专用）。修改前先征得用户同意。
- **macOS / iOS 搜不到设备：** 到「系统设置 → 隐私与安全性 → 本地网络」里打开 LocalSend 的权限。
- **安卓传输偏慢：** 官方 README 列出的已知问题，属于正常现象。
- 手机和电脑必须连同一个局域网。
