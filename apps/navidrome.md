# Navidrome

- 项目主页：https://github.com/navidrome/navidrome（GPL-3.0 许可），官网与文档 https://www.navidrome.org
- 说明：自建音乐服务器。把电脑里的音乐文件夹扫成曲库，在浏览器里直接播放；手机上用支持 Subsonic/OpenSubsonic 的播放器 App 连上它，就能随时听电脑里的歌。支持 FLAC 等常见格式、边播边转码、歌词、多用户各自的歌单和收藏，新放进文件夹的歌会自动入库。
- 支持系统：Windows、macOS、Linux（也提供 Docker 镜像和树莓派版本）。
- **注意：** 它是一个本地服务程序，装好后通过浏览器访问；只用来播放用户自己有权使用的音乐文件。

## 下载渠道

- GitHub Releases：https://github.com/navidrome/navidrome/releases/latest
  - Windows 64 位：`navidrome_<版本>_windows_amd64_installer.msi`（推荐，安装后自动作为系统服务运行）
  - macOS：`navidrome_<版本>_darwin_arm64.tar.gz`（Apple 芯片）或 `darwin_amd64.tar.gz`（Intel）
  - Linux：`linux_amd64.tar.gz` / `.deb` / `.rpm`

## 安装步骤

1. 先问用户音乐放在哪个文件夹（例如 `D:\Music`），没有就建一个。
2. **Windows：** 下载 `windows_amd64_installer.msi` 并运行。安装向导会询问端口和目录：端口保持 `4533`，音乐目录填第 1 步的文件夹，其余保持默认。装完后服务会自动启动（安装需要管理员确认，先向用户说明）。
3. **macOS / Linux：** 解压到固定目录（如 `~/navidrome`），在该目录新建 `navidrome.toml`，写入 `MusicFolder = "<音乐文件夹>"`，然后运行 `./navidrome -c navidrome.toml`，日志显示在 4533 端口监听、没有报错即启动成功。
4. 浏览器打开 `http://127.0.0.1:4533`，第一次进入会让用户创建管理员账号（用户名和密码由用户自己填写，不要替用户设置）。
5. 把访问地址告诉用户；手机端可在官网 https://www.navidrome.org/apps/ 里挑一款播放器 App，服务器地址填电脑的局域网 IP 加 `:4533`。

## 验证方法

- 浏览器打开 `http://127.0.0.1:4533` 能看到 Navidrome 页面；登录后「专辑」里出现音乐文件夹里的歌。

## 常见问题

- **扫描不到歌：** 确认音乐目录填对了；在页面右上角点刷新按钮手动扫描一次。
- **端口被占用：** 修改安装目录下 `navidrome.ini`（Windows）或 `navidrome.toml` 里的 `Port`，再重启服务。
- **手机连不上：** 手机和电脑要在同一个 Wi-Fi；Windows 防火墙需要放行 4533 端口（先向用户说明再操作）。
