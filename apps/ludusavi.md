# Ludusavi

- 项目主页：https://github.com/mtkennerly/ludusavi（MIT 许可）
- 作用：跨平台开源 PC 游戏存档备份与恢复工具（基于 PCGamingWiki 19,000+ 款游戏存档规则库，支持自定义游戏）。一键扫描文件存档、Windows 注册表进度与 Steam 截图，支持多版本完整/差异保留、ZIP 压缩、关键进度锁定（Lock）防覆写、路径重定向换盘/换电脑恢复、游戏启动前后自动备份及 rclone 云端/网盘目录防冲突同步；原生内置简体中文界面。
- 支持系统：Windows（64 位 / 32 位绿色便携版）、macOS、Linux、Steam Deck

## 下载渠道（按优先级）

1. GitHub Releases（推荐）：https://github.com/mtkennerly/ludusavi/releases/latest
   - Windows 64 位便携版：`ludusavi-v*-win64.zip`（约 13.2 MB，解压即用）
   - Windows 32 位便携版：`ludusavi-v*-win32.zip`
   - macOS 便携版：`ludusavi-v*-mac.tar.gz`（约 11.0 MB）
   - Linux 便携版：`ludusavi-v*-linux.tar.gz`（约 13.7 MB）
2. 包管理器：
   - Windows：`winget install mtkennerly.ludusavi` 或 `scoop install ludusavi`
   - macOS：下载 Releases `.tar.gz` 解压使用

## 安装步骤

- **Windows：**
  1. 下载 `ludusavi-v*-win64.zip` 解压到固定目录（例如 `D:\Tools\Ludusavi\`），直接双击 `ludusavi.exe` 即可运行，无需安装。
  2. 若首次双击弹出「Windows 已保护你的电脑」提示，确认安装包来自 GitHub 官方 Releases 后，先向用户说明情况，征得同意再点「更多信息 → 仍要运行」。
- **macOS：**
  1. 下载 `ludusavi-v*-mac.tar.gz` 解压得到 `Ludusavi.app`，移入「应用程序」。
  2. 如遇未签名应用提示，向用户说明后在「系统设置 → 隐私与安全性」点「仍要打开」。
- **首次使用配置：**
  1. 打开软件后在右上角设置图标进入 Settings，可将界面语言切为 **简体中文**（Chinese Simplified）。
  2. 确认顶部的备份目标目录（建议设为 D 盘或网盘同步目录），点一次「预览（Preview）」即可查看扫出的游戏清单，确认无误再点「备份（Back up）」。

## 验证方法

- 打开 Ludusavi 主窗口，点击顶部「Preview / 预览」，数秒内能看到系统已安装游戏、存档大小与具体路径列表，即表示安装与清单读取正常。

## 常见问题

- **冷门或非正版路径的游戏没扫到怎么办：** 切到「Custom Games / 自定义游戏」标签页，添加该游戏名和对应存档目录或注册表键路径即可纳入一键备份；也可在「Roots / 根目录」中添加自己的游戏安装盘符或文件夹。
- **重装系统或换电脑后用户名/盘符变了：** 在 Settings 的「Redirects / 重定向」里配置旧路径到新路径的映射规则，恢复时会自动写入新位置。
- **防止关键存档被轮转清理：** 切到「Restore / 恢复」标签页，点对应备份记录右侧的三点菜单，选择锁定（Lock），该版本将不占用保留数量名额且不会被自动清理。
