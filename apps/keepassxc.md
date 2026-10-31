# KeePassXC

- 项目主页：https://github.com/keepassxreboot/keepassxc （GPL-2.0 / GPL-3.0），官网 https://keepassxc.org
- 作用：开源免费的密码管理器。所有账号、密码、网址、附件、备注都存在一个离线加密的数据库文件（KDBX 格式）里，用一个主密码解锁；自带密码生成器（长度、字符类型可调，也能生成好记的词组密码）；「数据库报告 → 健康检查」会标出太弱、重复使用的密码；支持自动输入（Auto-Type）、浏览器集成、TOTP 两步验证码；能从 CSV、1Password、Bitwarden 等导入。
- 支持系统：Windows、macOS、Linux。
- 界面支持简体中文。

## 下载渠道（按优先级）

- 官网下载页：https://keepassxc.org/download/
- GitHub Releases：https://github.com/keepassxreboot/keepassxc/releases/latest
- 写作本教程时的版本是 2.8.0，文件名以下载页为准：

| 系统 | 文件 |
|---|---|
| Windows 64 位 | `KeePassXC-<版本>-x64.msi`（安装版）或 `KeePassXC-<版本>-x64.zip`（便携版，解压即用） |
| Windows ARM64 | `KeePassXC-<版本>-ARM64.msi` 或 `KeePassXC-<版本>-ARM64.zip` |
| macOS Apple 芯片（M 系列） | `KeePassXC-<版本>-arm64.dmg` |
| macOS Intel 芯片 | `KeePassXC-<版本>-x86_64.dmg` |

- 先用 `uname -m`（macOS）判断芯片：`arm64` 选 arm64，`x86_64` 选 x86_64。

## 安装步骤

- **Windows：** 双击 `.msi`，按提示点「下一步」完成安装（会弹出用户账户控制，由用户点「是」）。不想安装就用便携版：把 `.zip` 解压到用户目录（如 `%USERPROFILE%\Apps\KeePassXC`），双击 `KeePassXC.exe`。
- **macOS：** 打开 `.dmg`，把 KeePassXC 拖进「应用程序」，从启动台打开。

## 使用方法（告诉用户）

1. 首次打开点「创建新数据库」，起名、选保存位置，设置一个只有自己知道的主密码（主密码丢了无法找回，提醒用户记牢）。
2. 点工具栏的「+」新建条目，填网站、用户名；密码栏旁的骰子按钮打开密码生成器，调长度和字符类型后点「应用」。
3. 「数据库 → 数据库报告 → 健康检查」查看太弱、重复使用的密码。
4. 选中条目按 `Ctrl+Shift+V`（macOS 为 `Cmd+Shift+V`）自动输入账号密码；也可以在「工具 → 设置 → 浏览器集成」里开启浏览器扩展。
5. 数据库文件可以自己备份；每次打开输入主密码解锁。

## 验证方法

- 能打开 KeePassXC，看到「欢迎使用 KeePassXC」页面和「创建新数据库」按钮。

## 常见问题

- **界面是英文：** Tools → Settings → General → Language 选「简体中文」，重启 KeePassXC。
- 主密码只有用户自己知道，不要让智能体代为设置或记录。
