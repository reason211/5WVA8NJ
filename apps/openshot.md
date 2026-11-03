# OpenShot Video Editor

- 项目主页：https://github.com/OpenShot/openshot-qt （GPL-3.0）
- 作用：免费开源的视频编辑器，支持多轨剪辑、关键帧动画、视频特效、调色和导出。
- 支持 Windows、macOS 和 Linux。

## 下载渠道

- 官方下载页：https://www.openshot.org/download/ ，按系统和处理器选择稳定版。官网 Windows 版安装包免费；中国区微软商店版用于支持开发，可能需要付费，购买前须征得用户同意。
- 微软商店中国区：https://apps.microsoft.com/detail/9P6R2PMH4C04?hl=zh-CN&gl=CN ，核对应用名称 OpenShot Video Editor 和发布者 OpenShot Studios。
- 官方稳定版与校验文件：https://github.com/OpenShot/openshot-qt/releases/latest 。选择对应版本的 EXE、DMG 或 AppImage，不使用预发布版；下载地址与文件名以发布页为准。
- macOS 官方下载页提供 Intel 版；苹果芯片电脑如需通过 Rosetta 运行，先向用户说明并取得同意，不自行安装 Rosetta。

## 安装步骤

1. 先确认用户同意安装，判断系统和处理器架构，检查是否已经安装；不要覆盖或删除用户的视频及工程文件。
2. 优先通过上面的官方渠道取得稳定版。下载 GitHub 安装包时，在官方发布 API `https://api.github.com/repos/OpenShot/openshot-qt/releases/latest` 找到同名资产的 `digest`，计算文件的 SHA-256 并核对；缺少校验值或不一致时停止，不运行安装包。
3. Windows 按 EXE 向导或商店提示安装；macOS 打开 DMG，将 OpenShot 拖入「应用程序」；Linux 按官方说明使用与架构匹配的 AppImage。需要管理员授权或额外安装系统组件时，先说明并由用户确认。
4. 打开 OpenShot，确认主界面可见，告知用户软件位置。遇到系统或安全软件警告时暂停核实，不关闭防护或绕过限制。

## 使用方法

- 导入视频、音频和图片，拖到不同轨道进行剪辑。
- 使用关键帧调整位置、旋转和缩放，应用视频特效或调色。
- 使用导出功能保存成片；先确认导出路径，不覆盖用户现有文件。
