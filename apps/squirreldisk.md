# SquirrelDisk

- 项目主页：https://github.com/adileo/squirreldisk（AGPL-3.0 许可），官网 https://www.squirreldisk.com
- 作用：看清硬盘空间被谁占了，再安全地清理。整个硬盘画成一张彩色圆环图（也能换成方块图），扫描时圆环边扫边长；点一下扇区钻进文件夹，右侧列表按大小排好；把不要的文件夹拖到底部收集栏，一次性移到废纸篓、彻底删除或先备份再删。系统文件夹、用户主目录和整块磁盘受保护，删不掉。界面有简体中文。
- 支持系统：Windows 10/11、macOS（Apple 芯片和 Intel 通用）、Linux（x86_64）。

## 下载渠道（只用官方）

1. GitHub Releases：https://github.com/adileo/squirreldisk/releases/latest
   - Windows 安装版：`SquirrelDisk-Windows.msi`；免安装版：`squirreldisk-x86_64-pc-windows-msvc.exe`
   - macOS：`SquirrelDisk-macOS.dmg`
   - Linux：`SquirrelDisk-x86_64.AppImage`（或 `SquirrelDisk-Linux-x86_64.tar.gz`）
- 名字里带 `agent` 的文件是给远程服务器扫描用的组件，普通用户不用下载。

## 安装步骤

- Windows：双击 `.msi`，按提示完成安装，开始菜单里会出现 SquirrelDisk。用免安装版时直接双击 `.exe`。
- macOS：打开 dmg，把 SquirrelDisk 拖进「应用程序」。
- Linux：给 AppImage 加执行权限后直接运行。
- 界面语言默认跟随系统；不是中文时在「设置」里把语言改成简体中文。

## 验证方法

- 打开后首页列出电脑上的磁盘，点磁盘旁的「扫描」，能看到圆环图一层层长出来，右侧列出各文件夹大小。

## 使用提醒（告诉用户）

- 删除前看清楚：收集栏里的东西点「删除」后可以选移到废纸篓（能找回）或彻底删除（找不回）。默认建议用户选移到废纸篓。
- 不要替用户决定删哪些文件，只帮他找出大文件夹，由用户自己确认。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法打开：** 先打开一次并关掉提示，再到「系统设置 → 隐私与安全性」点「仍要打开」。如果提示“已损坏”，按官方 README 在终端执行 `xattr -dr com.apple.quarantine /Applications/SquirrelDisk.app` 后再打开。执行前先告诉用户原因。
