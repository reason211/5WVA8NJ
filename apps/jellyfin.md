# Jellyfin

- 项目主页：https://github.com/jellyfin/jellyfin（GPL-2.0 许可），官网 https://jellyfin.org ，文档 https://jellyfin.org/docs/
- 作用：把电脑里自己的电影、剧集、音乐整理成一个私人影音库。自动匹配海报、简介、演员等信息，记录观看进度，用浏览器、手机、电视客户端都能播放。服务端和官方客户端都免费，没有付费功能。
- 支持系统：服务端支持 Windows、macOS、Linux（也支持 Docker）；官方客户端有安卓、iOS、Android TV、LG WebOS、三星 Tizen 等。
- **注意：** 它是一个本地服务程序，装好后通过浏览器访问 `http://localhost:8096`。工具本身不提供任何影音内容，只管理用户自己有权使用的文件。

## 下载渠道

- 官方下载页：https://jellyfin.org/downloads/server
- 官方文件仓库（下载页的直链来源）：
  - Windows：https://repo.jellyfin.org/files/server/windows/latest-stable/amd64/ ，下载 `jellyfin_<版本>_windows-x64.exe` 安装包
  - macOS：https://repo.jellyfin.org/files/server/macos/latest-stable/ ，苹果芯片进 `arm64/`、Intel 芯片进 `amd64/`，下载 `.dmg`
- 文件名随版本变化，以页面为准；同目录有 `.sha256` 校验文件时，下载后核对。

## 安装步骤

- **Windows：**
  1. 运行下载的 `.exe` 安装包，按默认选项安装（不要选“作为服务安装”，官方不推荐）。
  2. 安装完成后 Jellyfin 会自动在后台运行，任务栏右下角出现托盘图标。
- **macOS：**
  1. 打开 `.dmg`，把 Jellyfin.app 拖进「应用程序」。
  2. 打开 Jellyfin，点菜单栏的 Jellyfin 图标，选择「Launch」。
- **首次设置（两个系统相同）：**
  1. 浏览器打开 `http://localhost:8096`，进入设置向导，语言选「中文（简体）」。
  2. 设置管理员用户名和密码时，请用户自己输入，不要替用户编造或记录密码。
  3. 「媒体库」一步可以先跳过；用户想添加时，点 + 号，内容类型选电影 / 节目 / 音乐，文件夹选用户自己的影视目录。
  4. 元数据语言选「中文」、国家选「中国」，这样海报和简介会尽量用中文。
  5. 网络设置保持默认，不开启“自动端口映射”。
- 在桌面创建一个打开 `http://localhost:8096` 的网页快捷方式，方便以后双击打开。

## 使用方法（告诉用户）

1. 双击桌面快捷方式（或浏览器访问 `http://localhost:8096`），用刚才设置的管理员账号登录。
2. 在「控制台 → 媒体库」添加自己的电影、剧集文件夹，扫描完成后首页会出现海报墙。
3. 手机、电视在同一个 Wi-Fi 下安装官方客户端（见 https://jellyfin.org/downloads/clients ），填写服务器地址 `http://<电脑的局域网 IP>:8096` 登录即可播放。

## 验证方法

- 浏览器能打开 `http://localhost:8096`，看到 Jellyfin 的设置向导或登录页。

## 常见问题

- **打不开 8096 页面：** Windows 看托盘图标是否在运行，没有就从开始菜单打开 Jellyfin；macOS 点菜单栏图标选「Launch」。
- **Windows 防火墙弹窗：** 允许“专用网络”访问，手机和电视才能连上。执行前先告诉用户原因。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点「仍要打开」。执行前先告诉用户原因。
- **海报没有出来：** 等媒体库扫描完成；文件夹按“电影名 (年份)”命名更容易匹配。
- 只管理和播放你有权使用的影音文件。
