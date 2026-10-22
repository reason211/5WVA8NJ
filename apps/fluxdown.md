# FluxDown：免费开源的多协议下载器

- 项目主页：https://github.com/zerx-lab/FluxDown（AGPL-3.0 许可）
- 作用：类似 IDM 的下载加速器，支持 HTTP/HTTPS、FTP、BT、磁力、eD2K、HLS 等，自带浏览器扩展接管下载。本地使用不需要注册账号。
- 支持系统：Windows（x64 / ARM64）、macOS（Intel / Apple 芯片）、Linux、安卓。

## 下载渠道（按优先级）

1. 官网：https://fluxdown.com/#download（国内可直接打开）
2. GitHub Releases：https://github.com/zerx-lab/FluxDown/releases/latest

按系统选择文件：

| 系统 | 文件名包含 |
|---|---|
| Windows 普通电脑（Intel / AMD） | `windows-x64-setup.exe` |
| Windows ARM 电脑 | `windows-arm64-setup.exe` |
| Mac 苹果芯片（M 系列） | `macos-arm64.dmg` |
| Mac Intel 芯片 | `macos-x64.dmg` |
| 安卓 | `android-universal.apk` |

注意：名字带 `CLI` 或 `Server` 的是命令行版和服务端版，普通用户不要选。

## 安装步骤

- Windows：双击 `setup.exe`，按提示安装。
- macOS：打开 `.dmg`，把 FluxDown 拖进「应用程序」。

## 验证方法

- FluxDown 能打开，在里面新建一个下载任务（例如下载 FluxDown 官网上的任意公开文件）能正常开始。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
- **浏览器扩展：** 需要接管浏览器下载时，再按 FluxDown 应用内的指引安装扩展，先征得用户同意。
- 只下载你有权获取的内容。
