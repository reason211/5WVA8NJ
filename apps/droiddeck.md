# DroidDeck

- 项目主页：https://github.com/Droid-Deck/DroidDeck（GPL-3.0 许可），官网 https://droid-deck.dev
- 说明：开源的安卓游戏掌机前端与运行环境，把 SteamOS 体验带到安卓设备。无需电脑远程串流或修改系统，支持在安卓手机/平板/掌机上直接运行 Steam 游戏模式、整合 Epic / GOG / Xbox 游戏库、外接双手柄本地分屏、连接 AR 智能眼镜，并可一键切换完整 Linux 桌面。
- 支持系统：Android 9 及以上（推荐高通 Adreno 730+ 或 8xx 机型；安装运行需预留约 4.1 GB 可用空间）。

## 下载渠道

- GitHub Releases（推荐）：https://github.com/Droid-Deck/DroidDeck/releases/latest
  - 下载 `DroidDeck-<版本>.apk` 主安装包。
- 官方主页：https://droid-deck.dev

## 安装步骤

1. **下载安装包：**
   - 从 GitHub Releases 下载最新版的 `DroidDeck-*.apk` 到电脑或手机本地目录。
2. **传输并安装到安卓设备：**
   - 将 APK 文件传输到安卓手机或掌机后，在文件管理器中点击安装（如提示允许安装未知来源应用，确认允许即可）。
3. **初始化运行环境：**
   - 首次打开 DroidDeck，按引导下载内置运行环境（约 3 GB 运行时，如需桌面与模拟器再加约 1.1 GB）。
   - 若为 Android 14 及以上系统，在手机「开发者选项」中开启「停用子进程限制（Disable child process restrictions）」；Android 12/13 在首次启动 Steam 时界面会弹出「Fix it for me」引导按钮。
   - 点击 **Play** 登录 Steam（或绑定 Epic / GOG / Xbox）即可开始游玩。

## 验证方法

- 在安卓设备上打开 DroidDeck，确认能正常进入主界面并加载游戏库（All / Steam / GOG / Epic / Xbox 分类可切换）。
- 运行任意轻度游戏或从电源菜单点击「Switch to Desktop」，确认能流畅切出桌面环境与退出返回。

## 常见问题

- **进入游戏后画面黑屏或子进程被系统杀掉：**
  - Android 14+ 务必前往系统「开发者选项」开启「停用子进程限制」。
- **需要删除桌面环境或重装运行时：**
  - 参考项目仓库 `docs/desktop-uninstall.md` 或在 DroidDeck 设置内清理运行时缓存目录后重新初始化。
