# Krita

- 项目主页：https://github.com/KDE/krita（GPL-3.0 许可），官网与中文文档 https://krita.org/zh-cn/
- 说明：专业自由开源数字绘画与插画软件。自带 100+ 种笔刷预设、笔刷防抖（消除手部颤抖）、透视辅助尺、漫画网格与矢量对话框、手绘逐帧动画时间轴，以及 PSD 文件完整读写支持。完全免费开源，没有试用期，没有订阅费，商用不受限制。
- 支持系统：Windows、macOS、Linux、Android。

## 下载渠道

- 官方下载：https://krita.org/zh-cn/download/
  - Windows：64 位安装程序（`.exe`）或免安装便携版（`.zip`）
  - macOS：DMG 镜像（支持 Intel 与 Apple Silicon）
  - Linux：AppImage 格式（赋予执行权限即可直接运行）
- GitHub Releases：https://github.com/KDE/krita/releases/latest

## 安装步骤

1. **Windows：**
   - 优先推荐下载 64 位安装程序（`krita-x64-setup.exe`），双击运行安装向导，按默认路径完成安装。
   - 或下载 Portable 免安装包（`.zip`），解压到固定软件目录（例如 `D:\Krita`），运行 `bin\krita.exe` 即可启动。
2. **macOS：**
   - 下载 DMG 镜像，打开后将 Krita 图标拖入「应用程序」文件夹（Applications）。首次启动如提示未签名或权限提示，在系统「隐私与安全性」中选择允许。
3. **Linux：**
   - 下载 `.appimage` 文件，在终端执行 `chmod +x krita-*.appimage`，双击或直接运行。

## 验证方法

- 启动 Krita 软件，成功进入主界面。
- 点击「文件」→「新建图像」，使用默认尺寸创建画布。
- 在左侧选择画笔工具，右侧选择任意笔刷预设，在画布上画线能够正常响应；在工具选项中开启「笔刷平滑/防抖」，线条平滑无锯齿断触。

## 常见问题

- **数位板没有压感：**
  - 进入「设置」→「配置 Krita」→「数位板设置」。
  - 在「数位板输入 API」中，尝试在 `WinTab` 与 `Windows 8+ Pointer Input (Windows Ink)` 之间切换，重启软件后测试压感。
- **界面默认不是中文：**
  - 点击「Settings」→「Switch Application Language」，选择「简体中文（zh_CN）」，重启软件即可。
- **与 Photoshop 互通：**
  - 在「文件」中直接「打开」或「另存为」`.psd` 格式，图层和混合模式均可完整保留与交互。
