# Sherlock

- 项目主页：https://github.com/sherlock-project/sherlock（MIT 许可）
- 作用：输入一个用户名，自动查它在 400 多个网站上有没有被注册，列出查到的网站和主页链接。可以一次查多个用户名；写成 `名字{?}123` 会自动试 `_`、`-`、`.` 三种拼法；结果可存成 txt，也能导出 CSV、Excel 表格。
- 支持系统：Windows / macOS / Linux（需要 Python 3.9 及以上）。本身是命令行程序，本教程会在桌面创建双击启动器，用户不用敲命令。
- **使用范围：** 只查询用户自己的用户名，或已获授权的用户名（如自己的品牌名），用来自查用户名是否被抢注、隐私是否外泄。不要用来追踪、骚扰他人。

## 下载渠道（按优先级）

1. PyPI 官方包 `sherlock-project`：https://pypi.org/project/sherlock-project/
2. macOS 也可用 Homebrew：`brew install sherlock`
3. 官方安装文档：https://sherlockproject.xyz/installation

## 安装步骤

1. **检查 Python：** 运行 `python --version`（Windows 也可用 `py --version`）或 `python3 --version`，需要 3.9 及以上。没有时从 Python 官网 https://www.python.org/downloads/ 安装（Windows 安装时勾选「Add python.exe to PATH」）。安装运行环境前先告诉用户并得到同意。
2. **用 pipx 安装 Sherlock（官方推荐）：**
   - Windows：
     ```bat
     py -m pip install --user pipx
     py -m pipx ensurepath
     py -m pipx install sherlock-project
     ```
   - macOS：`brew install pipx && pipx ensurepath && pipx install sherlock-project`（没有 Homebrew 时用 `python3 -m pip install --user pipx`，再执行 `python3 -m pipx ensurepath` 和 `python3 -m pipx install sherlock-project`）
   - Linux：`python3 -m pip install --user pipx && python3 -m pipx ensurepath && python3 -m pipx install sherlock-project`
   - 下载慢时可加国内镜像：`pipx install sherlock-project --pip-args="-i https://pypi.tuna.tsinghua.edu.cn/simple"`。
3. **在桌面创建双击启动器**（结果统一存到桌面的「Sherlock结果」文件夹）：
   - Windows：桌面新建 `Sherlock查用户名.bat`，以 UTF-8 编码保存：
     ```bat
     @echo off
     chcp 65001 >nul
     set "OUT=%USERPROFILE%\Desktop\Sherlock结果"
     if not exist "%OUT%" mkdir "%OUT%"
     set /p U=请输入要查询的用户名（多个用空格隔开）：
     sherlock %U% --txt --folderoutput "%OUT%" --timeout 15
     echo.
     echo 查询完成，结果已保存在桌面的「Sherlock结果」文件夹。
     pause
     ```
     如果提示找不到 `sherlock`，把其中的 `sherlock` 改成 `py -m pipx run --spec sherlock-project sherlock`。
   - macOS：桌面新建 `Sherlock查用户名.command`，执行 `chmod +x` 赋予运行权限（Linux 用 `.sh`）：
     ```bash
     #!/bin/bash
     export PATH="$HOME/.local/bin:/opt/homebrew/bin:/usr/local/bin:$PATH"
     OUT="$HOME/Desktop/Sherlock结果"; mkdir -p "$OUT"
     read -p "请输入要查询的用户名（多个用空格隔开）：" U
     sherlock $U --txt --folderoutput "$OUT" --timeout 15
     echo; echo "查询完成，结果已保存在桌面的「Sherlock结果」文件夹。"
     read -p "按回车键关闭…"
     ```

## 使用方法（告诉用户）

1. 双击桌面的「Sherlock查用户名」，输入用户名后回车，等 1–3 分钟。
2. 绿色 `[+]` 开头的行，是查到这个用户名已被注册的网站和主页链接；每个用户名的结果另存为 `用户名.txt`。
3. 多个用户名用空格隔开一起查；拿不准拼法时写成 `名字{?}123`，会自动试 `名字_123`、`名字-123`、`名字.123`。
4. 想要表格：在启动器里 `--txt` 后面加上 `--csv` 或 `--xlsx`。

## 验证方法

- 终端运行 `sherlock --version` 能显示版本号。
- 双击桌面启动器能出现「请输入要查询的用户名」的提示。

## 常见问题

- **提示找不到 sherlock 命令：** 执行 `pipx ensurepath`（Windows 为 `py -m pipx ensurepath`）后关掉终端重开；或按上面的说明改用 `pipx run --spec sherlock-project sherlock`。
- **部分网站显示超时或报错：** 多为网络原因，属正常现象；可把 `--timeout` 调大，或稍后重试。
- **macOS 双击 .command 提示无权限或无法打开：** 对脚本执行 `chmod +x`，或到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
- 只查询你自己或已获授权的用户名。
