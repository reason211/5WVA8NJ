# Sunshine + Moonlight（电脑游戏串流到手机、平板、电视）

- 上游项目：
  - 电脑端 Sunshine：https://github.com/LizardByte/Sunshine （GPL-3.0），文档 https://docs.lizardbyte.dev/projects/sunshine/latest/
  - 手机、平板、电视端 Moonlight：https://moonlight-stream.org （GPL-3.0），安卓 https://github.com/moonlight-stream/moonlight-android ，电脑客户端 https://github.com/moonlight-stream/moonlight-qt
- 作用：把电脑上的游戏画面和声音串流到手机、平板、电视盒子或另一台电脑，手机上的虚拟按键或手柄操作会传回电脑。Moonlight 官方说明支持最高 4K、120 帧、HDR 和 7.1 环绕声，可连接 PS、Xbox 和安卓手柄，最多 16 个手柄；在家用局域网或外网都能连。哪家商店买的游戏都能串，Sunshine 默认带“桌面”和“Steam 大屏模式”两个入口。
- 本教程在用户的电脑上安装 Sunshine（主机端），再告诉用户在手机等设备上怎么装 Moonlight 并配对。

## 先说明并取得同意

安装前告诉用户：会在电脑上安装 Sunshine，它作为后台服务运行（安装过程需要管理员授权），设置页面只在本机 `https://localhost:47990` 打开。不改路由器，不做端口转发，不把服务开放到公网；外网串流需要用户以后自己按官方文档配置。

## 安装步骤

### Windows（推荐）

1. 优先用 WinGet：`winget install LizardByte.Sunshine`。WinGet 不可用时，从官方发行版下载 `Sunshine-Windows-AMD64-installer.msi`（ARM 电脑用 `Sunshine-Windows-ARM64-installer.msi`）：https://github.com/LizardByte/Sunshine/releases/latest ，下载后核对文件来自 `github.com/LizardByte/Sunshine`，再双击安装。发行版里有四十多个文件，只下载上面这一个，不下载 debuginfo 或其他系统的包。
2. 安装完成后 Sunshine 会自动启动。用浏览器打开 `https://localhost:47990`。证书是本机自签的，浏览器提示不安全时选择“继续访问 localhost”。
3. 首次打开时让用户自己设置用户名和密码（提醒用户记下来），不要替用户设置或保存密码。

### macOS / Linux

- macOS：下载官方发行版的 `Sunshine-macOS-arm64.dmg`（Apple 芯片）或 `Sunshine-macOS-x86_64.dmg`（Intel），按提示授予“屏幕录制”和“辅助功能”权限。
- Linux：按官方文档 Getting Started 选择对应发行版的包（Flatpak、rpm、deb 等）。

## 手机、平板、电视端（告诉用户自己装）

- iPhone、iPad、Apple TV：在 App Store 搜索 “Moonlight Game Streaming”（开发者 Diego Waxemberg）。
- 安卓手机、平板、电视盒子：从 https://github.com/moonlight-stream/moonlight-android/releases 下载 `app-nonRoot-release.apk` 传到设备安装，或在 F-Droid 安装。
- 另一台电脑：从 https://github.com/moonlight-stream/moonlight-qt/releases 安装 Moonlight PC。

## 配对和验证

1. 手机和电脑连同一个 Wi-Fi（推荐 5GHz，电脑最好用网线）。
2. 打开 Moonlight，点出现的电脑名；没出现时点“Add Host”输入电脑的局域网 IP。
3. Moonlight 显示 4 位 PIN 码，用户在电脑的 Sunshine 页面点顶部 “PIN”，输入 PIN 和设备名后回车。
4. 配对成功后，在 Moonlight 里点 “Desktop” 或 “Steam Big Picture” 开始串流。

## 交付

告诉用户：Sunshine 设置页地址 `https://localhost:47990`、用户名由用户自己保管；手机端 Moonlight 的下载方式；配对时在 Sunshine 页面的 “PIN” 里输入手机显示的数字。

## 常见问题

- **Moonlight 找不到电脑：** 确认在同一个局域网，Windows 防火墙允许 Sunshine；可以手动输入电脑 IP。
- **画面卡顿：** 在 Moonlight 设置里先把分辨率降到 1080p、帧率 60，再逐步调高；电脑尽量用网线连路由器。
- **只玩自己拥有的游戏：** Sunshine 只串流电脑上已经安装的游戏和桌面，不提供游戏内容。
