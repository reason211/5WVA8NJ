# Stirling-PDF

- 项目主页：https://github.com/Stirling-Tools/Stirling-PDF（核心代码 MIT 许可，部分目录为专有许可），官网 https://stirling.com
- 作用：PDF 工具箱。50 多种工具：编辑、合并、拆分、压缩、转换、签名、遮挡敏感信息、OCR 文字识别、加密码、加水印等；界面支持 40 多种语言（含简体中文）。
- 支持系统：Windows、macOS、Linux 桌面版；也可以用 Docker 部署成网页版。

## 下载渠道（按优先级）

1. GitHub Releases：https://github.com/Stirling-Tools/Stirling-PDF/releases/latest
   - Windows：`Stirling-PDF-windows-…` 安装包
   - macOS：`Stirling-PDF-macos-universal.dmg`
   - Linux：`.AppImage` / `.deb` / `.rpm`
2. 官方文档的安装说明：https://docs.stirlingpdf.com

普通用户优先装桌面版，不需要 Docker。

## 安装步骤

- Windows：运行安装包按提示安装。
- macOS：打开 `.dmg`，把应用拖进「应用程序」。
- Linux：`.AppImage` 加执行权限后运行，或用系统包管理器安装 `.deb` / `.rpm`。

## 验证方法

- 打开后能看到 PDF 工具列表（合并、压缩、转换等），能添加一个 PDF 文件。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
