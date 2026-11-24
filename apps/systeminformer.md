# System Informer

- 项目主页：https://github.com/winsiderss/systeminformer（MIT 许可）
- 作用：Windows 系统进程、资源、网络与硬件实时监控和故障排查工具（原 Process Hacker 续作）。支持彩色树状图查看父子进程关系、按文件名搜索并解除文件占用句柄、暂停（挂起）/恢复进程、查看实时网络与磁盘读写并断开可疑连接，以及 CPU/内存/GPU 显存温度曲线和系统托盘监控。
- 支持系统：Windows 10 / Windows 11（64 位、32 位及 ARM64）
- **注意：** 本软件仅支持 Windows 系统；如果用户的电脑是 macOS 或 Linux，请如实说明，不要尝试安装。

## 下载渠道（按优先级）

1. 官方下载页：https://systeminformer.com/downloads
2. GitHub Releases（推荐稳定版）：https://github.com/winsiderss/systeminformer/releases/latest
   - 安装版：`systeminformer-*-release-setup.exe`
   - 绿色便携版：`systeminformer-*-bin.zip`（约 22 MB，解压即可运行；在同目录新建空文件 `SystemInformer.exe.settings.xml` 可将配置保存在 U 盘）
3. 命令行包管理器（WinGet）：`winget install Winsider.SystemInformer`

## 安装步骤

1. 先确认用户授权安装，说明 System Informer 将从官方渠道下载，部分深入功能（如管理其他用户进程、关闭系统句柄）需要管理员权限；获得同意后再继续。
2. 若从 GitHub Releases 下载，下载完成后在 `https://api.github.com/repos/winsiderss/systeminformer/releases/latest` 核对同名资产的 `digest`（SHA-256），校验一致后再运行。
3. 推荐优先使用绿色便携版 `bin.zip`：解压到常用工具目录（如 `D:\Tools\SystemInformer\`），按平台架构选择 `amd64` 或 `arm64` 目录下的 `SystemInformer.exe`；若选择安装版 `.exe`，按官方安装向导完成。
4. 完成后告知用户软件所在位置及启动方式。

## 验证方法

- 打开 `SystemInformer.exe`，能正常显示彩色进程树、实时 CPU/内存/I/O/GPU 占用；
- 按 `Ctrl+F` 打开「Find Handles or DLLs」输入任意文件名能检索出占用句柄；切换到 `Network` 和 `Disk` 标签能看到实时连接与磁盘读写列表。

## 常见问题

- **为什么有的系统进程需要管理员权限才能操作？** Windows 对高权限或系统服务进程做了访问隔离；在菜单点 `System Informer -> Show details for all processes` 授权后即可查看全部详情。
- **不想开机自启怎么关？** 默认安装或便携版不强制开机自启；如在设置里开启了自启，取消 `Options -> General -> Start when Windows starts` 即可。
