# NAPS2（文档扫描与 PDF 整理工具）

- 项目主页：https://github.com/cyanfish/naps2 （GPL-2.0 许可），官网：https://www.naps2.com
- 作用：连接扫描仪或直接导入图片、PDF，支持拖拽重排页面顺序、旋转、裁剪与亮度对比度微调，还可开启本地 OCR 让扫描件 PDF 变成可搜索、可复制文字的文件，并支持局域网共享扫描仪。
- 支持系统：Windows 10 / 11、macOS 10.15+、Linux

## 下载渠道（按优先级）

1. 官网下载页：https://www.naps2.com/download
2. GitHub Releases：https://github.com/cyanfish/naps2/releases/latest

## 安装步骤

- **Windows：** 从官网或 GitHub Releases 下载 `naps2-8.6.1-win-x64.exe`（ARM64 电脑选 `win-arm64.exe`，便携需求可选 `win-x64.zip`），双击运行安装程序按提示完成安装。
- **macOS：** 从官网或 GitHub Releases 下载 `naps2-8.6.1-mac-univ.pkg`（通用安装包，兼容 Apple 芯片和 Intel），双击 `.pkg` 按安装向导完成安装。
- **Linux：** 下载对应发行版的 `.deb`、`.rpm` 或 `.flatpak` 安装。

## 第一次使用

- 如果要导入本地图片或现有 PDF 进行整理合并，直接在顶部工具栏点击「Import（导入）」选中文件，拖曳缩略图即可调整顺序，再点击「Save PDF」保存。
- 如果要让扫描出来的 PDF 可以搜索和复制文字，点击顶部「OCR」下载对应语言包（支持简体中文等一百多种语言）并勾选启用即可。

## 验证方法

- NAPS2 能正常打开主界面，顶部工具栏和左侧配置栏完整显示；导入一张图片或 PDF 页面能够正常显示缩略图并执行旋转、保存操作。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认安装包来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
