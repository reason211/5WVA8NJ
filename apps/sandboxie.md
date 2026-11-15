# Sandboxie

- 项目主页：https://github.com/sandboxie-plus/Sandboxie（官网 https://sandboxie-plus.com）
- 作用：Windows 沙盒隔离工具。把陌生软件或测试程序放进隔离沙盒里运行，程序对文件和注册表的修改全部重定向进独立沙盒目录，不改坏原系统；支持单程序联网防火墙、一键清空沙盒残留、选择性恢复有用文件，以及同软件多开。
- 支持系统：Windows 7 及以上（x64 / ARM64）
- **注意：** 这款软件只支持 Windows。用户是 macOS 或 Linux 时，如实说明，不要尝试安装。

## 下载渠道（只用官方）

1. GitHub Releases：https://github.com/sandboxie-plus/Sandboxie/releases/latest
2. 官网下载：https://sandboxie-plus.com/downloads/
- 发布页按架构选择：64 位系统选 `Sandboxie-Plus-x64-v<版本>.exe`，ARM64 选 `Sandboxie-Plus-ARM64-v<版本>.exe`。不要下载带 Classic 的旧版。

## 安装步骤

1. 双击官方安装包，语言选择「简体中文」，按向导提示点击下一步完成安装（需要用户确认管理员权限以安装沙盒驱动）。
2. 安装完成后打开「Sandboxie-Plus（SandMan）」，首次向导保持默认设置即可。
3. 使用方法：鼠标右键点击任意想隔离运行的程序，选择「在沙盒中运行」。

## 验证方法

- 主界面能正常打开，右键菜单出现「在沙盒中运行」选项；尝试在沙盒里运行记事本，窗口标题栏显示 `[#]` 标记与黄色边框。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认安装包来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **沙盒里保存的文件如何拿出来：** 在沙盒列表中右键对应沙盒，选「恢复」或「清空内容」，可只把需要的文件恢复到桌面或指定目录。
