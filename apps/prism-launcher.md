# Prism Launcher

- 项目主页：https://github.com/PrismLauncher/PrismLauncher （GPL-3.0），官网 https://prismlauncher.org
- 作用：免费开源的《我的世界》（Minecraft Java 版）启动器。可以同时管理多个游戏实例，每个实例有自己的版本、模组和设置；内置 Modrinth、CurseForge 等平台，直接搜索安装整合包和单个模组，并能检查、一键更新；轻量（Qt 编写，不内嵌浏览器），支持自定义主题。
- 支持系统：Windows、macOS、Linux。
- 界面支持简体中文。
- 与 Mojang、微软无关联；进入游戏需要用户自己的、已购买 Minecraft Java 版的微软账号。

## 下载渠道（按优先级）

- 官网下载页：https://prismlauncher.org/download/windows （macOS 见同页「macOS」标签）
- GitHub Releases：https://github.com/PrismLauncher/PrismLauncher/releases/latest
- Windows 也可以用 WinGet：`winget install --exact PrismLauncher.PrismLauncher`
- 写作本教程时的版本是 11.1.1，文件名以下载页为准：

| 系统 | 文件 |
|---|---|
| Windows 64 位 | `PrismLauncher-Windows-MSVC-Setup-<版本>.exe`（安装版）或 `PrismLauncher-Windows-MinGW-w64-Portable-<版本>.zip`（便携版） |
| Windows ARM64 | `PrismLauncher-Windows-MSVC-arm64-Setup-<版本>.exe` |
| macOS | `PrismLauncher-macOS-<版本>.zip` |

## 安装步骤

- **Windows：** 双击 Setup `.exe`，按提示点「下一步」完成安装。装完在开始菜单或桌面打开 Prism Launcher。安装版缺少 Visual C++ 运行库时，改用 MinGW 版（不需要运行库）。
- **macOS：** 解压 `.zip`，把 Prism Launcher.app 拖进「应用程序」。首次打开如果提示无法验证开发者，到「系统设置 → 隐私与安全性」点「仍要打开」。执行前先告诉用户原因。
- 首次打开会出现设置向导：语言选「简体中文」；Java 页面按提示让启动器自动下载合适的 Java；其余保持默认，点「完成」。

## 使用方法（告诉用户）

1. 右上角「账户」→「管理账户」→ 添加微软账号并登录（账号需要已购买 Minecraft Java 版，登录由用户自己完成）。
2. 点「添加实例」：选「原版」可以直接挑游戏版本；左侧选 Modrinth 或 CurseForge 可以搜索整合包，选中点「确定」自动下载安装。
3. 选中实例 →「编辑」→「模组」→「下载模组」，在线搜索单个模组，勾选后点「检查并确认」一起下载。
4. 同一页面点「检查更新」，会列出每个模组的新旧版本，勾选要升级的点「确定」。
5. 不同游戏版本各建一个实例，模组和设置互不影响；选中实例点「启动」进入游戏。

## 验证方法

- 能打开 Prism Launcher 主界面，看到顶部「添加实例」按钮和实例列表。

## 常见问题

- **界面是英文：** 「Settings（设置）」→「Launcher（启动器）」→ Language 选「简体中文」。
- **启动游戏提示找不到 Java：** 设置 → Java，按提示自动下载合适版本。
- 本软件只是启动器，不提供游戏本体，请使用正版账号。
