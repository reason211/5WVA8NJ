# Readest

- 项目主页：https://github.com/readest/readest（AGPL-3.0 许可），官网 https://readest.com
- 作用：开源电子书阅读器。支持 EPUB、PDF、MOBI、AZW3、FB2、CBZ、TXT、Markdown 等格式；划线、笔记、书签；全文搜索；朗读；字体、排版和主题配色可调；阅读进度和笔记可在多个设备间同步。
- 支持系统：Windows、macOS、Linux、安卓、iOS（手机端从官网或应用商店安装）。

## 下载渠道（只用官方）

1. GitHub Releases：https://github.com/readest/readest/releases/latest
2. 官网：https://readest.com
- 发布页文件较多，按系统选择：
  - Windows x64（大多数电脑）：`Readest_<版本>_x64-setup.exe`（安装版）或 `Readest_<版本>_x64-portable.exe`（免安装版）；骁龙笔记本选 `arm64` 版本。
  - macOS（Apple 芯片和 Intel 通用）：`Readest_<版本>_universal.dmg`。
  - Linux：`Readest_<版本>_amd64.AppImage` 或 `.deb`。
- 不要下载 `.sig`、`.zip` 插件包和 Source code。

## 安装步骤

- Windows：双击安装版按提示安装；免安装版直接双击运行。
- macOS：打开 `.dmg`，把 Readest 拖进「应用程序」。
- 装好后打开 Readest，把电子书文件拖进窗口即可加入书库。

## 验证方法

- Readest 能正常打开书库界面，导入一本电子书后能翻页阅读。

## 常见问题

- **Windows 上双击没反应：** 官方说明是系统缺少或损坏了 WebView2 运行库。告诉用户原因，取得同意后从微软官网安装 WebView2 Runtime，再重新打开 Readest。
- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
- 只阅读你有权使用的电子书，软件本身不提供书籍内容。
