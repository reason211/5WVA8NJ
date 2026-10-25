# File Converter

- 官方仓库：https://github.com/Tichau/FileConverter
- 官网：https://file-converter.io/ （注意域名是 `.io`；不要使用同名下载站）
- 许可：GPL-3.0，免费开源。
- 用途：在 Windows 资源管理器的右键菜单中转换、压缩单个或多个文件；支持音视频、图片和 PDF，以及自定义转换预设。
- 系统：Windows。先识别用户系统与架构，不在 macOS、Linux 或不受支持的架构上强行安装。

## 官方下载与校验

1. 优先打开 https://file-converter.io/download.html ，或官方 https://github.com/Tichau/FileConverter/releases/latest 。按当前发布说明选择安装包，不使用第三方下载站或来历不明的社区修改版。
2. v2.2 的官方 x64 安装包为 `FileConverter-2.2-x64-setup.msi`，大小 60,522,496 字节；官方 Releases API 提供的 SHA-256：
   ```text
   78bb9755b35a94e59a72f299b6b63b5da472deb5c2b03ce016e5fe9f116a3554
   ```
   用 PowerShell `Get-FileHash -Algorithm SHA256 <安装包路径>` 核对。其他版本须重新获取对应版本的官方校验值，不沿用上面的哈希。
3. 检查文件来源与数字签名。校验不一致、签名异常或安全软件报警时停止，不关闭防护，不自动绕过系统安全警告。官方渠道均无法访问时如实报告，不使用代理、加速或绕过网络限制的方法。

## 安装与打开

1. 说明安装目标、下载位置、安装位置；安装和管理员权限操作先取得用户同意。
2. 运行官方 `.msi`，按安装向导完成安装。不要启动教程以外的软件或改动其他系统设置。
3. File Converter 的主要入口是资源管理器右键菜单，不是常驻主窗口。Windows 11 可先点「显示更多选项」，再找「File Converter」。
4. 设置可从右键菜单的「Configure presets」打开；可修改输出格式、画质、缩放比例和旋转角度。修改前记录原设置，保留原文件，首次使用不启用转换后删除源文件。

## 验证与汇报

- 用一张用户自有的测试图片，保留原件，右键 → File Converter → 选择可用的图片输出格式。
- 确认转换进度完成、新文件存在且能打开，原件仍在；不要覆盖已有同名文件。
- 多选两张测试图片验证批量转换；测试前先说明输入、输出位置。
- 汇报安装目录、右键入口、设置入口、测试结果，以及通过 Windows「设置 → 应用」卸载的方法。
- 若菜单未出现，先查看官方排障文档；重启资源管理器或电脑前说明影响并让用户确认。不要反复重装或关闭系统防护。

## 使用说明

- 只处理自有或获得授权的文件。
- Office 文档转换需要本机已安装并激活 Microsoft Office；不要自动安装、破解或绕过激活。音视频转音频会提取音轨，并非任意格式都支持相互转换。
- 格式列表：https://github.com/Tichau/FileConverter/wiki/Supported-file-formats
- 排障：https://github.com/Tichau/FileConverter/wiki/Troubleshooting
- 项目已报告有冒充官网的第三方站点；始终从官方仓库核对官网域名和下载地址。
