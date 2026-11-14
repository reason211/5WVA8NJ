# RetroArch

- 项目主页：https://github.com/libretro/RetroArch（GPL-3.0 许可），官网与文档 https://www.retroarch.com
- 说明：全能开源复古游戏模拟器前端。一个软件整合红白机（FC/NES）、街机（Arcade/MAME/FBNeo）、GBA、PS1 等上百款经典机种模拟核心；手柄即插即用自动映射，支持随时即时存档读档、高级 CRT 扫描线复古滤镜、局域网与网络联机对战（Netplay）。完全开源免费，无任何第三方广告插件。
- 支持系统：Windows、macOS、Linux、Android、iOS、电视盒子。

## 下载渠道

- 官方下载：https://www.retroarch.com/?page=platforms
  - Windows：64 位安装程序（Installer）或绿色便携解压版（7-Zip）
  - macOS：DMG 镜像（包含 Apple Silicon 与 Intel 版本）
  - Android：官网直接下载 APK，或通过 Google Play / 华为应用市场安装
  - Steam：亦可在 Steam 商店免费添加入库
- GitHub Releases：https://github.com/libretro/RetroArch/releases/latest

## 安装步骤

1. **Windows：**
   - 推荐下载 64 位安装包（`RetroArch-*-x86_64-setup.exe`）按提示完成安装；或下载便携版解压到任意英文目录（如 `D:\RetroArch`）。
   - 启动 `retroarch.exe`。
2. **下载游戏核心（Cores）：**
   - 进入主菜单（Main Menu）→「Online Updater」（在线更新器）→「Core Downloader」（核心下载器）。
   - 在列表中选择你想玩的游戏机机种（例如 Game Boy Advance、Nintendo NES、Sony PlayStation 等），点击即可一键自动下载官方核心。
3. **加载游戏开始畅玩：**
   - 点击「Load Content」（载入游戏内容），定位到存放游戏 ROM 的文件夹，选择游戏文件即可启动。
   - 插入 USB 或蓝牙游戏手柄，RetroArch 会在屏幕左下角提示“Controller configured”，按键已全自动适配就绪。

## 验证方法

- 打开 RetroArch，插入手柄，屏幕出现手柄已配置提示；按下手柄方向键能正常控制菜单上下移动。
- 启动任意一款经典游戏，画面流畅渲染，声音清晰无爆音；按下快捷键 `F2` 保存即时状态，按下 `F4` 瞬间读档复原。

## 常见问题

- **界面默认是英文怎么改中文：**
  - 进入「Settings」→「User」→「Language」，选择「Simplified Chinese」（简体中文）即可实时切换。
- **想要复古老电视画面：**
  - 在游戏运行中按 `F1` 呼出快捷菜单，进入「Shaders」（着色器），开启后载入 `crt` 预设，即可一秒拥有老电视显像管扫描线质感。
