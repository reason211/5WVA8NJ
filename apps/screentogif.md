# ScreenToGif

- 项目：https://github.com/NickeManarin/ScreenToGif（MS-PL 许可）
- 用途：录制选定屏幕区域、摄像头或手绘过程，逐帧编辑，导出 GIF、APNG、视频等。
- 支持系统：Windows 10 / 11；不支持 macOS 或 Linux，不在这些系统上尝试安装。

## 官方下载渠道

1. 微软商店：https://apps.microsoft.com/detail/9n3sqk8pds8g （中国区可尝试打开，核对名称 ScreenToGif、作者 Nicke Manarin）。
2. 作者的 ScreenToGif 专页：https://nicke.tech/screentogif 。旧域名可能跳到同作者的另一款产品 N-Studio，不要误装。
3. 官方发布：https://github.com/NickeManarin/ScreenToGif/releases/latest 。不要用第三方下载站或镜像，不修改 hosts、不关闭安全防护。

## 安装步骤

1. 确认用户授权安装、Windows 版本、x64 / ARM64 / x86 架构及安装目录；检查是否已有 ScreenToGif，避免重复安装。
2. 优先打开微软商店的官方条目，请用户完成商店确认；不代填账号或验证码。
3. 商店不可用时，从官方 Releases 选对应架构的完整便携版 `ScreenToGif.<版本>.Portable.<架构>.zip`。不要误选 `Light`（需要另装 .NET 运行时）、`Setup` 或其他架构。以当前发布页为准。
4. 校验下载：从 GitHub 官方 release API 对应 asset 读取 `size` 与 `digest`；用 PowerShell `Get-FileHash -Algorithm SHA256` 核对 SHA-256。若官方未提供 digest，至少核对大小与来源，并核查签名状态；无法确认来源就停止。禁止执行未校验的文件。
5. 解压到用户同意的新目录（如 `%LOCALAPPDATA%\Programs\ScreenToGif`），保留已有文件，不覆盖同名目录。说明可执行文件位置，请用户打开 `ScreenToGif.exe`。需要管理员权限、运行环境或安全警报时，先停下说明原因，不自动绕过。
6. 截至 2026-10-26，官方最新版本为 2.43.2。x64 完整便携包为 `ScreenToGif.2.43.2.Portable.x64.zip`，大小 73035883 字节，SHA-256 为 `42a0b53d67ecae22698b4881ffb2c9c7a9049663f5fbdd2edb779e1971000664`；版本变化时重新读取官方 API，不套用旧校验值。

## 验证与汇报

- 主界面显示录屏、摄像头、白板、编辑器入口。
- 经用户同意，用不含隐私的自有内容录制约 2 秒，停止后进入逐帧编辑器，另存 GIF 并预览；不覆盖原文件。
- 汇报软件版本、目录、可执行文件、测试 GIF 路径、打开方法及卸载方式。商店版通过系统卸载；便携版退出后经用户确认删除对应目录，先备份项目。
- 未实际完成操作时不声称已安装或已验证。所有官方渠道均不可达时说明原始错误并停止。

## 安全与版权

只录制自有或获授权内容，录制前清理账号、通知和聊天信息。遇到杀毒软件拦截时不要添加例外、关闭防护或点“仍要运行”，先停止并核实官方来源与校验值。
