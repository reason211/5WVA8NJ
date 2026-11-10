# AdGuard Home

- 项目主页：https://github.com/AdguardTeam/AdGuardHome（GPL-3.0 许可），官方文档 https://adguard-dns.io/kb/adguard-home/getting-started/
- 说明：装在家里一台常开的电脑上的 DNS 服务器。装好后把路由器（或单台设备）的 DNS 改成这台电脑的局域网地址，全家的电视、手机、平板上网时，广告和跟踪域名就会被拦下，设备本身不用装软件。后台有中文界面：内置 64 份可选拦截清单（含中文规则）、139 个可一键屏蔽的常见 App 和网站、按设备单独设置和定时放开、家长控制、安全搜索和统计仪表盘。
- 支持系统：Windows、macOS、Linux（也支持 Docker、路由器等）。
- **注意：** 这台电脑要保持开机；DNS 要用 53 端口，首次运行需要管理员权限。执行任何需要管理员权限或 sudo 的命令前，先向用户说明作用并征得同意。

## 下载渠道

- GitHub Releases：https://github.com/AdguardTeam/AdGuardHome/releases/latest ，下载页共 27 个文件，按系统选一个：
  - Windows（大多数电脑）：`AdGuardHome_windows_amd64.zip`；ARM 电脑选 `AdGuardHome_windows_arm64.zip`
  - macOS：Apple 芯片选 `AdGuardHome_darwin_arm64.zip`，Intel 芯片选 `AdGuardHome_darwin_amd64.zip`
  - Linux：一般选 `AdGuardHome_linux_amd64.tar.gz`
  - 其余 freebsd、openbsd、mips、armv5/6/7 等是给路由器和特殊设备用的，普通电脑不用下载；`AdGuardHome_frontend.tar.gz`、`checksums.txt` 也不用下。

## 安装步骤

### Windows

1. 把压缩包解压到固定目录，例如 `C:\AdGuardHome`。
2. 征得用户同意后，以管理员身份打开 PowerShell，进入该目录运行 `.\AdGuardHome.exe -s install`，注册成系统服务（开机自动运行）。
3. 浏览器打开 `http://127.0.0.1:3000`，进入初始化向导：网页管理端口可用 80（被占用就用 3000 或其他空闲端口），DNS 端口用 53；按向导设置管理员用户名和密码。
4. 把后台地址、管理员账号密码，以及这台电脑的局域网 IP（向导最后一页会显示）告诉用户。

### macOS

1. 把压缩包解压到 `/Applications/AdGuardHome`（官方要求 macOS 10.15 以后放在 `/Applications` 下）。
2. 征得用户同意后，在终端进入该目录运行 `sudo ./AdGuardHome -s install`。
3. 浏览器打开 `http://127.0.0.1:3000` 完成初始化向导，同 Windows 第 3、4 步。

### Linux

1. 解压后进入 `AdGuardHome` 目录，征得同意后运行 `sudo ./AdGuardHome -s install`。
2. 浏览器打开 `http://<这台电脑的IP>:3000` 完成初始化向导。

## 让全家设备用上

- 推荐改路由器：登录路由器后台（常见地址 `http://192.168.0.1` 或 `http://192.168.1.1`），在 DHCP/DNS 设置里把 DNS 改成这台电脑的局域网 IP。改完后连这个 Wi-Fi 的设备都会自动生效。
- 只想管单台设备：在该设备的 Wi-Fi 设置里把 DNS 改成这台电脑的 IP。
- 后台「设置指导」页有路由器、Windows、macOS、Android、iOS 的图文步骤，可以直接让用户照着做。路由器设置由用户自己操作，不要替用户改路由器密码。

## 验证方法

- 浏览器打开后台地址能登录，仪表盘「DNS 查询」数字在增长。
- 在已改 DNS 的电脑上运行 `nslookup doubleclick.net <这台电脑的IP>`，返回 `0.0.0.0` 说明拦截生效。

## 常见问题

- **53 端口被占用：** Windows 上多半是别的 DNS/代理软件占用，先告诉用户是哪个程序，由用户决定是否关闭。
- **某个网站被误拦：** 后台「查询日志」里找到这条记录，点「放行」即可。
- **暂时不想拦：** 仪表盘上点「禁用保护」，可选暂停一段时间。
- **卸载：** 管理员身份运行 `AdGuardHome -s uninstall`，再把路由器或设备的 DNS 改回原来的值。
