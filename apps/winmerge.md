# WinMerge

- 项目主页：https://github.com/WinMerge/winmerge（GPL-2.0 许可），官网 https://winmerge.org
- 作用：文件和文件夹差异对比合并工具。把两份或三份文档、CSV 表格、图片或整个文件夹并排打开，用颜色标出改过、新增和删掉的位置，一键合并差异。
- 支持系统：仅 Windows
- **注意：** 这款软件只支持 Windows。用户是 macOS 或 Linux 时，如实说明，不要尝试安装。

## 下载渠道（按优先级）

1. GitHub Releases：https://github.com/WinMerge/winmerge/releases/latest
   - 64 位安装版：`WinMerge-<版本>-x64-Setup.exe`（或免管理员 `WinMerge-<版本>-x64-PerUser-Setup.exe`）
   - 64 位便携版：`winmerge-<版本>-x64-exe.zip`
2. 官网下载页：https://winmerge.org/downloads/
3. Windows 也可用 winget：`winget install -e --id WinMerge.WinMerge`

## 安装步骤

- 安装版：运行 `WinMerge-<版本>-x64-Setup.exe` 按提示完成安装。
- 便携版：解压 `winmerge-<版本>-x64-exe.zip` 到本地文件夹后直接运行 `WinMergeU.exe`。

## 验证方法

- 能正常打开 WinMerge 主界面，点击「文件 → 打开」能同时选择两份文件或两个文件夹进行对比。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **想切换成简体中文界面：** 打开软件顶部「Edit → Options → System」，或在安装时勾选简体中文语言包。
