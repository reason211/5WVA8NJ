# STranslate

- 官方仓库：https://github.com/STranslate/STranslate
- 作者在 README 提供的国内项目入口：https://gitee.com/zggsong/STranslate
- 官网与文档：https://stranslate.zggsong.com/
- 安装说明：https://stranslate.zggsong.com/docs/(un)install.html
- 许可：MIT，开源翻译与 OCR 工具；支持增量划词翻译、多源结果对照、图片翻译和回译。
- 系统：Windows。先核对系统、版本、处理器架构及当前发行说明，不在不兼容的系统上强行运行。

## 下载与校验

1. 从官网进入官方 Releases：https://github.com/STranslate/STranslate/releases/latest 。作者 README 也提供 Gitee 国内项目入口；只有该官方入口实际列出对应发行包时才使用，不把源码压缩包当安装包，不使用第三方下载站。
2. 安装版为 `STranslate-win-Setup.exe`；便携版为 `STranslate-win-Portable.zip`。默认优先便携版，解压到用户同意的新目录，不覆盖已有软件或配置。
3. v2.0.10 官方便携包大小为 55,704,398 字节，SHA-256：
   ```text
   d63f4cef674ae2f6ef782e1c7fa43b2475e62aea0ad31c34b41ab5c9cb58abc5
   ```
   安装版大小为 60,189,153 字节，SHA-256：
   ```text
   f5ac0e0bdc1acfea6df8aa48a1557264f7a7cc9112aad5752379d8263f8c7a1b
   ```
   使用 PowerShell `Get-FileHash -Algorithm SHA256 <文件路径>` 核对。其他版本重新读取官方 Releases API 的 `digest`，不沿用旧哈希。
4. 来源、哈希或数字签名异常时停止；安全软件报警时不关闭防护。官方渠道均不可访问时如实报告，不使用代理、改 hosts、下载加速站等绕过办法。

## 安装与配置

1. 先说明软件、下载和安装目录，取得用户安装授权。便携版解压后双击 `STranslate.exe`；安装版按官方向导操作，默认目录为 `%LOCALAPPDATA%\STranslate`。
2. 如果软件提示缺少 .NET 10，先说明并取得运行环境安装授权，再从微软官网 https://dotnet.microsoft.com/download/dotnet/10.0 下载匹配架构的 **.NET Desktop Runtime**，不下载来历不明的运行库。
3. 按欢迎界面配置所需快捷键和内置服务。优先使用官方内置、无需私钥的服务验证；不要索取、截图、记录或代填用户的 API 密钥。
4. 图片翻译需选择文本识别和翻译服务。将文本发给联网翻译服务前，说明数据流并取得同意；不要上传隐私、试卷、未授权资料。第三方服务可能有额度或费用，以其说明为准，不代开通付费服务。
5. 配置存放：便携版为软件目录的 `PortableConfig`；安装版为 `%APPDATA%\STranslate`。不覆盖已有配置，不改系统安全设置。

## 验证与汇报

- 确认程序能启动，窗口和托盘入口正常。
- 用自写的 `hello world` 测试翻译；确认原文和结果可见，不把模拟或等待中的界面当成完成。
- 用户同意后，用不含隐私的自有截图测试 OCR 或图片翻译，确认文字可读；按官方文档配置增量翻译快捷键后，可用两段自写英文验证连续选词合并。
- 汇报实际软件位置、启动文件、配置位置、测试结果及常用快捷键。某个联网服务失败时先报告原始错误，不反复重装或关闭安全防护。
- 卸载：安装版用 Windows「设置 → 应用」卸载；便携版退出后可移除软件目录。删除配置、目录或用户数据前说明影响并单独取得同意；需保留的配置先备份。
