# optimizerDuck：Windows 优化工具

- 项目主页：https://github.com/itsfatduck/optimizerDuck
- 作用：免费开源的 Windows 优化工具，按需选择性能、隐私、精简等优化项，每一项都可以撤销。
- 支持系统：**仅 Windows 10 / 11。** macOS 和 Linux 不支持，请改装清单里的其他软件。
- 风险提示：它会修改系统设置。作者建议改动前先创建系统还原点。

## 下载渠道

- GitHub Releases：https://github.com/itsfatduck/optimizerDuck/releases/latest
  - 普通电脑（Intel / AMD）：`optimizerDuck-Windows-x64-版本号.exe`
  - ARM 电脑：`optimizerDuck-Windows-arm64-版本号.exe`

## 使用步骤

1. 下载对应的 `.exe`，放到用户指定的文件夹（例如「下载」）。它不需要安装，双击就能运行。
2. **先征得用户同意，再创建系统还原点**（开始菜单搜索「创建还原点」）。
3. 打开 optimizerDuck 后，**不要替用户选择或执行任何优化项**。把各优化项的作用说明给用户，由用户自己决定选哪些、什么时候应用和重启。

## 验证方法

- optimizerDuck 主界面能正常打开。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **想撤销某项优化：** 在 optimizerDuck 里对应的优化项上选择撤销；也可以用之前创建的系统还原点恢复。
