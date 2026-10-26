# PDFMathTranslate（pdf2zh）

- 项目主页：https://github.com/PDFMathTranslate/PDFMathTranslate（AGPL-3.0 许可）
- 作用：英文论文等 PDF 全文翻译成中文，公式、图表、目录和批注保留原排版；输出纯中文版和双语对照版两个 PDF。
- 支持系统：Windows（官方打包版，解压即用）/ macOS、Linux（Python 安装，浏览器里使用图形界面）
- 默认翻译服务是谷歌翻译，不用填密钥；DeepL、OpenAI、Ollama 等服务需要用户自己的密钥或本地模型。

## 下载渠道（按优先级）

1. GitHub Releases：https://github.com/PDFMathTranslate/PDFMathTranslate/releases/latest
2. PyPI（macOS / Linux）：`pdf2zh` 包，https://pypi.org/project/pdf2zh/
3. 不想安装时可用官方在线版：https://pdf2zh.com/ ，或魔搭社区演示：https://www.modelscope.cn/studios/AI-ModelScope/PDFMathTranslate

按系统选择文件（文件名会随版本变化，以 Releases 页面为准）：

| 系统 | 参考文件名 |
|---|---|
| Windows（推荐，已内置排版模型和字体） | pdf2zh-v1.9.11-with-assets-win64.zip |
| Windows（精简版，首次运行要联网下载模型） | pdf2zh-v1.9.11-win64.zip |

## 安装步骤

- **Windows：**
  1. 下载 `with-assets` 版 zip（约 550 MB），解压到不含中文的目录，例如 `D:\pdf2zh`。
  2. 双击 `pdf2zh.exe`，稍等片刻浏览器会打开 `http://localhost:7860/` 的翻译界面；没有自动打开就手动访问这个地址。
  3. 在桌面给 `pdf2zh.exe` 创建快捷方式，方便以后双击打开。
- **macOS / Linux：**
  1. 需要 Python 3.11–3.12。先 `pip install uv`（或 `brew install uv`），再执行：
     ```bash
     uv tool install --python 3.12 pdf2zh
     ```
  2. 在桌面创建启动脚本 `PDF翻译.command`（Linux 用 `.sh`），内容如下，并 `chmod +x`：
     ```bash
     #!/bin/bash
     export HF_ENDPOINT=https://hf-mirror.com
     pdf2zh -i
     ```
  3. 双击启动脚本，浏览器访问 `http://localhost:7860/` 即可使用。

## 使用方法（告诉用户）

1. 把 PDF 拖进左上角 File 区域（也可以填在线 PDF 链接）。
2. Service 选翻译服务（默认 Google），Translate to 选 Chinese，Pages 选全部或前几页。
3. 点 Translate，完成后右侧预览译文，下方可下载 `translated_…pdf`（纯中文版）和 `dual_…pdf`（双语对照版）。

## 验证方法

- 浏览器能打开 `http://localhost:7860/` 的 PDFMathTranslate 界面。

## 常见问题

- **Windows 双击后打不开或闪退：** 按 README 安装微软运行库 https://aka.ms/vs/17/release/vc_redist.x64.exe 后重试。执行前先告诉用户原因。
- **首次翻译卡在下载模型：** 国内网络下载 Hugging Face 模型可能失败，设置环境变量 `HF_ENDPOINT=https://hf-mirror.com` 后重新运行（Windows 用 with-assets 版可避免）。
- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法验证开发者或无权限运行 .command：** 到「系统设置 → 隐私与安全性」点击「仍要打开」，或对脚本执行 `chmod +x`。执行前先告诉用户原因。
- 只翻译你有权使用的文档。
