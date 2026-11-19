# Feishin

- 项目主页：https://github.com/jeffvli/feishin（GPL-3.0 许可）
- 作用：连接 Navidrome、Jellyfin、Subsonic 等自建音乐库的现代桌面播放器，支持 MPV 无损解码、实时歌词与智能歌单。
- 支持系统：Windows / macOS / Linux / Web

## 下载渠道（按优先级）

1. GitHub Releases：https://github.com/jeffvli/feishin/releases/latest
2. Web 托管版：https://feishin.vercel.app

按系统选择文件（文件名会随版本变化，以 Releases 页面为准）：

| 系统 | 参考文件名 |
|---|---|
| Windows（64位安装版/便携版） | Feishin-1.17.0-win-x64.exe、Feishin-1.17.0-win-x64.zip |
| Windows（ARM64） | Feishin-1.17.0-win-arm64.exe、Feishin-1.17.0-win-arm64.zip |
| Mac 苹果芯片 | Feishin-1.17.0-mac-arm64.dmg |
| Mac Intel 芯片 | Feishin-1.17.0-mac-x64.dmg |
| Linux | Feishin-linux-x86_64.AppImage、Feishin-linux-amd64.deb |

## 安装步骤

- Windows：运行 `.exe` 安装包按提示安装；便携版解压 `.zip` 后直接运行。
- macOS：打开 `.dmg`，把 Feishin 拖进「应用程序」。若首次打开提示“已损坏或无法验证”，可在终端执行 `xattr -cr /Applications/Feishin.app` 或在「系统设置 → 隐私与安全性」点击「仍要打开」（执行前先向用户说明）。
- Linux：赋予 `.AppImage` 可执行权限后直接运行，或使用 `sudo dpkg -i` 安装 `.deb`。

## 验证方法

- Feishin 能正常打开主界面，可进入设置选择或添加 Navidrome / Jellyfin / Subsonic 服务器地址。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的 GitHub Releases 官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **无法连接自建音乐库：** 确认服务器地址（含 `http://` 或 `https://` 与端口号）填写正确，且服务器与当前设备网络互通。
- 本工具仅作为自建音乐库播放客户端，请只播放你有合法权限的音频内容。
