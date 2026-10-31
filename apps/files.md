# Files

- 项目主页：https://github.com/files-community/Files （MIT），官网 https://files.community
- 作用：开源的 Windows 文件管理器，和系统自带的资源管理器并存，不替换、不改动原有文件夹。像浏览器一样开多个标签页；双栏并排打开两个文件夹、直接拖动文件；给文件贴颜色标签（工作、照片等）并在侧栏按标签查看；分栏布局；命令面板；压缩包按 Ctrl+Shift+E 智能解压；文件列表直接显示文件夹大小；自定义工具栏和背景图。
- 支持系统：Windows 10、Windows 11（64 位或 ARM64）。
- 界面支持简体中文。

## 下载渠道（按优先级）

- 官网下载页：https://files.community/download → 「Other ways to install」→「Install from」选「Classic installer」→「Download installer」。这种方式免费。
  - 直接链接：https://files.community/appinstallers/Files.stable.appinstaller （用 Windows 自带的「应用安装程序」打开）
- WinGet（第三方维护）：`winget install -e --id FilesCommunity.Files`
- 微软商店版本（9NGHP3DX8HDX）是付费支持开发者的渠道，和免费安装版是同一个软件；用户没要求就用免费的 Classic installer。
- 写作本教程时的稳定版本是 4.3.0.0。

## 安装步骤

1. 下载 `Files.stable.appinstaller`，双击，用「应用安装程序」打开，点「安装」。安装器会自动下载软件和依赖（需要联网，Windows 更新和传递优化服务要开着）。
2. 如果双击 `.appinstaller` 没反应或报错，改用 WinGet 命令安装。
3. 装完在开始菜单搜索「Files」打开。

## 使用方法（告诉用户）

1. 顶部「+」新建标签页，`Ctrl+T` 也可以；`Ctrl+Shift+T` 恢复误关的标签页。
2. 点左上角的操作按钮选择添加窗格（或按 `Ctrl+Shift+S`）打开双栏，两个文件夹并排，文件可以直接拖到另一边。
3. 右键文件 → 展开「编辑标签」，选一个颜色标签；点侧栏「标签」下的标签名，能看到所有贴了它的文件。
4. 选中压缩包按 `Ctrl+Shift+E`：只有一个文件时直接解压到当前位置，多个文件会自动新建文件夹。
5. 在设置里打开显示文件夹大小（或对单个文件夹点「查看大小」），列表里就能看到每个文件夹占多大。

## 验证方法

- 能打开 Files 主界面，看到顶部标签栏和左侧的侧栏。

## 常见问题

- **界面是英文：** Settings → General → Language 选「简体中文」，重启 Files。
- **安装报错 “Cannot open app package” 等：** 确认 Windows 更新、传递优化服务已开启，重启电脑后重试；精简版或改过的 Windows 系统官方不支持。
