# ONLYOFFICE Desktop Editors

- 项目主页：https://github.com/ONLYOFFICE/DesktopEditors （AGPL-3.0）
- 作用：免费开源的办公套件，一个窗口处理文档、表格、演示文稿和 PDF；支持编辑 PDF 文字、表格公式与图表、演示文稿导出，以及文件密码保护。
- 支持 Windows、macOS、Linux；可离线编辑本地文件。

## 下载渠道

- Windows 微软商店（中国区）：https://apps.microsoft.com/detail/xpdlh3xbzxqv23?hl=zh-CN&gl=CN ，核对应用名 ONLYOFFICE、发布者 Ascensio Systems Inc.，从商店安装。
- 官方下载页：https://www.onlyoffice.com/zh/download-desktop ，按系统和处理器选择桌面版安装包。
- 官方稳定版：https://github.com/ONLYOFFICE/DesktopEditors/releases/latest ，下载与系统匹配的资产，不选预发布版。Windows x64 为 `DesktopEditors_x64.exe`，Windows ARM64 为 `DesktopEditors_arm64.exe`；苹果芯片 Mac 为 `ONLYOFFICE-arm.dmg`，Intel 芯片 Mac 为 `ONLYOFFICE-x86_64.dmg`。Linux 的 DEB、RPM 和 AppImage 也在官方发布页。
- 官方安装说明：https://helpcenter.onlyoffice.com/desktop/installation/desktop-install-windows.aspx 、https://helpcenter.onlyoffice.com/desktop/installation/desktop-install-macos.aspx

## 安装步骤

1. 先确认用户授权安装，判断系统和处理器架构；检查软件是否已经安装。不要覆盖或删除用户文档。
2. Windows 可通过上面的微软商店安装，其他系统从官方渠道下载对应稳定版。若通过 GitHub Releases 下载，在官方发布 API `https://api.github.com/repos/ONLYOFFICE/DesktopEditors/releases/latest` 找到同名资产的 `digest`，计算下载文件的 SHA-256 并逐字核对；缺少校验值或不一致时停止，不运行安装包。
3. Windows 商店版按商店提示安装；安装包版打开对应的 EXE，按安装向导完成；需要管理员授权时先说明并由用户确认。macOS：打开对应的 DMG，将 ONLYOFFICE 拖入「应用程序」。Linux：按官方页面选择发行版和架构对应的软件包，并依照官方安装说明操作。
4. 安装后打开 ONLYOFFICE Desktop Editors，确认能看到首页，并告知用户应用位置；遇到安全警告时暂停核实，不关闭防护或绕过系统限制。

## 使用方法

- 从首页新建或打开文档、表格、演示文稿和 PDF；多个文件可在窗口标签之间切换。
- 表格中可以使用公式和图表；演示文稿可导出为常见格式；PDF 可编辑文字。
- 需要保护文件时使用软件提供的密码保护功能，并妥善保存密码。
