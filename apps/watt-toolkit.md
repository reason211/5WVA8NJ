# Watt Toolkit（原名 Steam++）

- 项目主页：https://github.com/BeyondDimension/SteamTools（GPL-3.0 许可），官网 https://steampp.net
- 作用：开源跨平台的游戏工具箱。本地网络加速（让 Steam 商店、社区等游戏网站更快打开）、多平台游戏账号一键切换、Steam 库存游戏管理、本地令牌。大部分功能需要电脑上已经装了 Steam。
- 支持系统：Windows 10（1809）及以上、Windows 11；macOS 10.15 及以上；Ubuntu 20.04、Debian 11、Fedora 37、Deepin 20 及以上；Android 5.0 及以上。

## 下载渠道（按优先级）

1. 官网：https://steampp.net（国内下载快）
2. 码云发行版：https://gitee.com/rmbgame/SteamTools/releases
3. GitHub Releases：https://github.com/BeyondDimension/SteamTools/releases/latest
   - Windows：`Steam++_v版本号_win_x64.exe`（安装版）或 `.7z`（免安装）
   - macOS：`Steam++_v版本号_macos.dmg`
   - Linux：`Steam++_v版本号_linux_x64.tgz`
4. 也可以从 Microsoft Store、Steam 商店安装（README 下载渠道里列出）。

## 安装步骤

- Windows：运行 `.exe` 按提示安装；免安装版解压后运行 `Steam++.exe`。
- macOS：打开 `.dmg`，把应用拖进「应用程序」。
- Android：在手机上安装官网提供的 APK，或把 APK 传到手机安装。

## 首次使用

- 网络加速需要安装本地证书并修改 hosts，这是软件的正常机制。执行前先告诉用户原因，用户同意后再在软件里点「一键加速」。

## 验证方法

- 能打开主界面，左侧有「网络加速」「账号切换」「库存游戏」「本地令牌」等入口。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
