# PDFsam

- 项目主页：https://github.com/torakiki/pdfsam（AGPL-3.0 许可），官网 https://pdfsam.org
- 作用：PDF 合并与拆分（安装的是免费开源的 PDFsam Basic）。把多个 PDF 拖进去合成一份，可只挑指定页码、保留书签；按页码、书签或文件大小拆分；还能旋转页面、抽取页面、交替混排、插入页面。全程在本机处理，不上传文件，不加水印。
- 支持系统：Windows、macOS（Intel 和 Apple 芯片）、Linux。

## 下载渠道（只用官方）

1. GitHub Releases：https://github.com/torakiki/pdfsam/releases/latest
   - Windows 64 位：`pdfsam-basic-<版本>-windows-x64.msi`
   - macOS Apple 芯片：`pdfsam-basic-<版本>-macos-arm64.dmg`；Intel：`pdfsam-basic-<版本>-macos-x64.dmg`
   - Linux：`pdfsam-basic_<版本>-1_amd64.deb` 或 `pdfsam-basic-<版本>-linux-x64.tar.gz`
2. 官网下载页：https://pdfsam.org/download-pdfsam-basic/
- 只装 PDFsam Basic。官网上的 PDFsam Enhanced、PDFsam Visual 是收费产品，不要下载或安装。

## 安装步骤

- Windows：双击 `.msi`，按提示完成安装，开始菜单里会出现 PDFsam Basic。安装包已自带运行环境，不需要另装 Java。
- macOS：先用「关于本机」确认芯片类型，下载对应的 `.dmg`，打开后把 PDFsam Basic 拖进「应用程序」。
- Linux：Debian/Ubuntu 用 `sudo apt install ./pdfsam-basic_<版本>-1_amd64.deb`；其他发行版解压 tar.gz 后运行目录里的 `bin/pdfsam.sh`。
- 界面语言默认跟随系统；不是中文时，在左侧「Settings → Language」里选「中文 (简体)」，重启后生效。

## 验证方法

- 打开 PDFsam Basic，左侧能看到 Merge、Split、Rotate 等工具；点 Merge，把两个 PDF 拖进列表，点 Run 后显示 Completed。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
- **启动时弹出新闻或升级提示：** 这是官方的公告面板，直接关闭即可，不影响免费功能。
