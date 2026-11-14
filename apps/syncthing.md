# Syncthing

- 项目主页：https://github.com/syncthing/syncthing（MPL-2.0 许可），官网与文档 https://syncthing.net
- 说明：端到端加密的跨平台文件多端自动同步工具。不经过任何第三方服务器，手机拍的照片、电脑里的文档只要连上网，就会在局域网内跑满千兆网速自动双向同步；出门在外也可自动穿透互联。支持增量传输，改动几个字节只传变动部分。
- 支持系统：Windows、macOS、Linux、Android（iOS 可使用兼容客户端 Möbius Sync）。

## 下载渠道

- 官方下载：https://syncthing.net/downloads/
  - Windows：64 位 Zip 包，或使用社区 Windows GUI（SyncTrayzor）
  - macOS：DMG 镜像或命令行程序
  - Linux：各架构二进制包或 APT 仓库
  - Android：Google Play 或 F-Droid 搜索「Syncthing」
- GitHub Releases：https://github.com/syncthing/syncthing/releases/latest

## 安装步骤

1. **Windows：**
   - 下载 Windows 64 位包解压到固定目录（例如 `D:\Syncthing`）。
   - 双击运行 `syncthing.exe`，会自动在系统托盘启动并在默认浏览器打开 `http://127.0.0.1:8384`。
2. **macOS：**
   - 解压后运行二进制程序，或将应用拖入 Applications 目录，首次运行赋予辅助权限。
3. **Android：**
   - 安装官方客户端，授予文件存储与后台运行权限。
4. **配对与同步：**
   - 在电脑端打开 Web 管理界面（`http://127.0.0.1:8384`），点击右上角「操作」→「显示 ID」查看本机设备标识或二维码。
   - 在手机端点击「添加设备」，扫描电脑端二维码，确认添加。
   - 在文件夹设置中，勾选需要共享的设备（如手机相机相册目录或电脑工作文件夹），点击保存即可开始自动同步。

## 验证方法

- 浏览器打开 `http://127.0.0.1:8384` 能看到 Syncthing 控制台，左侧显示共享文件夹，右侧显示已连接设备。
- 在电脑端共享文件夹新建一个测试文件，手机端对应文件夹在数秒内自动同步出现，状态显示「最新」。

## 常见问题

- **外网连不上：**
  - 确认默认设置中的「NAT 遍历」与「全局发现」已开启，Syncthing 会自动通过官方中继和发现服务器打洞。
- **开机自启：**
  - Windows 用户可在快捷方式放入 `shell:startup` 目录，或配置为 Windows 服务后台静默运行。
