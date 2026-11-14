# Espanso

- 项目主页：https://github.com/espanso/espanso（GPL-3.0 许可），官网与文档 https://espanso.org
- 说明：跨平台快捷输入文本展开神器，使用 Rust 编写。在任意软件里输入自定义的简写代码（如 `:email`、`:date`），瞬间自动替换为完整的文本、模版、发票抬头或客服回复；支持快捷键 Alt+Space 搜索模版，支持表单弹窗输入变量。纯本地配置文件，安全离线，不偷传按键记录。
- 支持系统：Windows、macOS、Linux。

## 下载渠道

- 官方下载：https://espanso.org/install/
  - Windows：安装版（Installer）或绿色免安装便携版（Portable）
  - macOS：DMG 镜像（包含 Intel 与 Apple Silicon 版本）
  - Linux：AppImage 或 DEB / RPM 包
- GitHub Releases：https://github.com/espanso/espanso/releases/latest

## 安装步骤

1. **Windows：**
   - 推荐下载 `Espanso-Win-Installer-x86_64.exe` 双击安装；安装完成后会在系统托盘常驻运行。
2. **macOS：**
   - 下载 DMG 并将应用拖入 Applications 目录；首次启动需在系统「设置」→「隐私与安全性」中授予「辅助功能」权限（用于监听按键与注入文本）。
3. **Linux：**
   - 下载 `.AppImage` 并赋予可执行权限后运行。
4. **自定义模版配置：**
   - 在终端运行 `espanso path` 查看配置文件目录。
   - 打开 `match/base.yml`，在 matches 下添加自己的触发词：
     ```yaml
     matches:
       - trigger: ":email"
         replace: "your_name@example.com"
       - trigger: ":date"
         replace: "{{mydate}}"
         vars:
           - name: mydate
             type: date
             params:
               format: "%Y-%m-%d"
     ```
   - 保存文件后，在任意聊天窗口或文档中输入 `:email` 即可测试瞬间替换。

## 验证方法

- 打开记事本或任意输入框，输入 `:date`，文本立即自动替换为当天的年月日格式，说明 Espanso 监听与替换正常。
- 按下快捷键 `Alt + Space`，屏幕中央弹出搜索框，能正常搜索并插入模版。

## 常见问题

- **按键没有替换反应：**
  - macOS 用户检查辅助功能（Accessibility）与输入监控（Input Monitoring）权限是否已开启。
  - Windows 用户检查安全杀毒软件是否拦截了模拟按键（退格与粘贴）。
