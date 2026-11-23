# Gyroflow

- 项目主页：https://github.com/gyroflow/gyroflow（GPL-3.0 许可），官网：https://gyroflow.xyz
- 作用：基于陀螺仪与运动数据的开源视频防抖工具，支持 GoPro、索尼、大疆、Insta360、佳能及手机传感器数据，具备实时零拷贝 GPU 预览、自适应动态裁剪、卷帘快门果冻校正、地平线锁定与多款剪辑软件插件支持（PR/AE、达芬奇、Final Cut Pro）。
- 支持系统：Windows（x64 / ARM64）、macOS（通用安装包 / App Store）、Linux（tar.gz / AppImage）、Android（APK / Google Play）、iOS（App Store）

## 下载渠道（按优先级）

1. GitHub Releases：https://github.com/gyroflow/gyroflow/releases/latest
2. 官网与商店：Windows 可用微软商店，macOS / iOS 可用 App Store，或官网 https://gyroflow.xyz

按系统选择最新安装包（当前最新 v1.7.1）：

| 系统 | 参考文件名 / 渠道 |
|---|---|
| Windows x64 | `Gyroflow-windows64.zip`（解压即用） |
| Windows ARM64 | `Gyroflow-windows-arm64.zip` |
| macOS 通用版 | `Gyroflow-mac-universal.dmg` |
| Linux x64 | `Gyroflow-linux64.tar.gz` 或 `Gyroflow-linux64.AppImage` |
| Android | `Gyroflow.apk` |
| iOS | App Store 搜索 `Gyroflow` |

## 安装步骤

- **Windows：** 解压 `Gyroflow-windows64.zip` 后直接运行里面的 `Gyroflow.exe`（免安装绿色版；如提示缺少 `VCRUNTIME140.dll`，需安装微软 VC++ 运行库）。
- **macOS：** 打开 `.dmg`，将 `Gyroflow` 拖入「应用程序」。
- **Linux / Android：** Linux 解压 `.tar.gz` 运行 `./Gyroflow`；Android 将 `Gyroflow.apk` 传到手机点击安装。

## 验证方法

- 打开 Gyroflow 主窗口，拖入带陀螺仪数据的相机或手机录制的测试视频，可见左下角自动识别镜头预设并绘制三轴运动波形图，点击播放可实时预览稳像效果。

## 常见问题

- **Windows 提示缺少运行库：** 到微软官网下载安装 Visual C++ Redistributable x64。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
- 若使用本身不带内嵌陀螺仪的老相机拍摄，需配合手机传感器记录 App（如 Sensor Logger）或外置记录仪保存运动日志后导入同步。
