# Handy

- 项目主页：https://github.com/cjpais/Handy（MIT 许可），官网 https://handy.computer
- 作用：完全离线、开源免费的跨平台语音转文字桌面工具。按住或点按快捷键说话，本地 Silero VAD 过滤静音后交由本地 Whisper、Qwen3-ASR、Fun-ASR 或 Parakeet 等离线语音模型识别，直接把文字打进当前任意软件输入框，不上传录音到云端；也支持拖入音视频文件本地转写。
- 支持系统：Windows（x64 / ARM64）、macOS（Apple Silicon / Intel）、Linux（x64 / ARM64）

## 下载渠道（按优先级）

1. GitHub Releases（推荐）：https://github.com/cjpais/Handy/releases/latest
   - Windows 64 位安装版：`Handy_<版本>_x64-setup.exe`（或 `.msi`）
   - Windows ARM64 安装版：`Handy_<版本>_arm64-setup.exe`
   - macOS（Apple Silicon / Intel）：`Handy_<版本>_aarch64.dmg` / `Handy_<版本>_x64.dmg`
   - Linux：`Handy_<版本>_amd64.AppImage` / `.deb` / `.rpm`
2. 官网下载：https://handy.computer
3. 包管理器：Windows `winget install cjpais.Handy` / macOS `brew install --cask handy`

## 安装步骤

- **Windows：** 下载 `Handy_*_x64-setup.exe`，双击安装即可（如提示未签名警告，确认来自官网或 GitHub Releases 后点「更多信息 → 仍要运行」，操作前先向用户说明）。
- **macOS：** 打开 `.dmg` 将 `Handy.app` 拖入「应用程序」，首次打开按提示授权「麦克风」与「辅助功能」权限（用于全局快捷键和自动上屏）。
- **首次使用配置：** 打开 Handy 后进入 Models 页面下载推荐语音模型（如识别中文可选 `Qwen3-ASR` 或 `Fun-ASR Nano`，也可按设备性能选 `Whisper` 或 `Parakeet V3`），在 Settings 确认快捷键和触发方式（按住说话或按一下开关）。

## 验证方法

- 打开任意记事本或聊天输入框，按住设定的快捷键说一句话并松开，等待识别悬浮窗走完后文字自动打进光标位置。

## 常见问题

- **中文识别或简繁切换：** 模型列表中选择支持中文的模型（如 `Qwen3-ASR` / `Fun-ASR Nano` / `Whisper`），可在设置里配置输出语言及简体/繁体中文选项。
- **macOS 蓝牙耳机降噪或音质变低：** 蓝牙麦录音会触发双向通话模式，如在意音乐音质可把麦克风输入切回电脑内置麦或外接麦。
