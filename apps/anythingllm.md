# AnythingLLM

- 项目主页：https://github.com/Mintplex-Labs/anything-llm（MIT 许可），官网：https://anythingllm.com
- 作用：本地优先的一站式私有文档知识库与 AI 助手桌面客户端，支持拖入 PDF、Word、表格等 30 多种格式本地向量建库、问答附带原文引用、内置本地模型引擎与 40 多种模型后端接入、动态模型路由、无代码 Agent 流程与 MCP 兼容。
- 支持系统：Windows（x64 / ARM64）、macOS（Apple Silicon / Intel）、Linux（AppImage）

## 下载渠道（按优先级）

1. GitHub Releases：https://github.com/Mintplex-Labs/anything-llm/releases/latest
2. 官网下载页：https://anythingllm.com/download

按系统选择最新桌面安装包（当前最新 v1.20.0）：

| 系统 | 参考文件名 |
|---|---|
| Windows x64 | `AnythingLLMDesktop.exe` |
| Windows ARM64 | `AnythingLLMDesktop-Arm64.exe` |
| macOS Apple Silicon | `AnythingLLMDesktop-Silicon.dmg` |
| macOS Intel | `AnythingLLMDesktop.dmg` |
| Linux x64 / ARM64 | `AnythingLLMDesktop.AppImage` / `AnythingLLMDesktop-Arm64.AppImage` |

## 安装步骤

- **Windows：** 运行 `AnythingLLMDesktop.exe` 按向导完成安装并启动桌面端。
- **macOS：** 打开 `.dmg`，将 AnythingLLM 拖入「应用程序」。
- **Linux：** 赋予 `.AppImage` 可执行权限后直接运行。

## 验证方法

- 打开 AnythingLLM 桌面客户端，新建一个工作区（Workspace），把一份本地 PDF 或 TXT 文档拖入工作区并点击入库；在模型设置中选择本地 Ollama / 内置引擎或填入自有 API Key，提问后可看到带 `Sources` 原文引用出处的回答。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认安装包来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
- 请只导入和解析你有权使用的学习资料与工作文档；使用云端模型接口需自备账号或 API Key。
