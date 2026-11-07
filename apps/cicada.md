# 知了 Cicada（实时双语字幕、同声传译、会议纪要）

- 项目主页：https://github.com/wquguru/cicada（Apache-2.0 许可），官网 https://cicada.indaloop.app
- 作用：读取电脑正在播放的声音（腾讯会议、飞书、Zoom、X Spaces、YouTube 直播等），实时出双语字幕、边听边写纪要（总结、议题、结论、待办、人名术语）；按住说话键说中文，对方在会议里听到翻译后的语音；会议记录、录音保存在本机，可导出 Markdown、Word、SRT。
- 支持系统：macOS 14.4+（Apple 芯片 / Intel）、Windows 10 2004+（x64 / ARM64）、Ubuntu 22.04/24.04 桌面版、Android 10+。
- **需要用户自己的 AI 服务 key 的情况（告诉用户）：** Apple 芯片 Mac 不填 key 也能用实时字幕和翻译；Intel Mac、Windows、Linux、Android 需要 Ling（蚂蚁集团大模型服务）key，或在设置里换成 OpenRouter、ZenMux 等兼容服务。官方说明 Ling 每月赠送 10 元额度，约够 10–50 小时会议。key 由用户本人申请和粘贴，不代为注册、不读取其它应用的凭据。

## 下载渠道（只用官方）

- GitHub Releases：https://github.com/wquguru/cicada/releases/latest
- 官网下载页：https://cicada.indaloop.app/download/
- 发布页文件较多，按系统选择：
  - Windows x64（大多数电脑）：`Cicada-<版本>-Windows-x64.exe` 或 `Cicada-Setup.exe`；骁龙笔记本选 ARM64 版本。
  - Mac Apple 芯片：`Cicada-<版本>-macOS-AppleSilicon.dmg`；Intel Mac：`Cicada-<版本>-macOS-Intel.dmg`。
  - Linux：`Cicada-<版本>-Linux.tar.gz`；Android：`Cicada-<版本>-Android.apk`（下载到电脑后传到手机安装）。
- 下载后用同一发布页的 `checksums.txt` 核对 SHA-256（Windows：`certutil -hashfile 文件 SHA256`；Mac：`shasum -a 256 文件`）。

## 安装步骤

- Windows：双击安装包即可，不需要管理员权限。安装程序暂无代码签名，SmartScreen 拦截时点“更多信息 → 仍要运行”。执行前先告诉用户原因。
- Mac：打开 dmg，把知了拖进“应用程序”。应用尚未经苹果公证，第一次打开被拦时到“系统设置 → 隐私与安全性”点“仍要打开”。执行前先告诉用户原因。
- Linux：`tar xzf Cicada-<版本>-Linux.tar.gz && cicada-linux/install.sh`。
- 同声传译需要虚拟麦克风（Windows 为 VB-Cable，Mac 为 BlackHole 2ch），由知了的引导在用户同意后安装；不要静默安装驱动。

## 首次使用（告诉用户）

1. 打开知了，跟着首次引导：授权系统声音、播放示例会议看字幕效果。
2. 需要 key 的平台：在引导或“设置 → AI 服务”粘贴自己的 key 并点“保存并检查”。
3. 开会或看直播时，字幕和纪要会自动出现；同声传译按住右 Ctrl（Windows）或右 Option（Mac）说话。

## 验证方法

- 知了能正常打开，示例会议能显示双语字幕。
- 需要 key 的平台，“保存并检查”显示 key 可用。

## 常见问题

- **没有字幕：** 确认电脑确实在出声、已授予录制系统声音权限；Windows 版确认 key 已通过检查。
- **对方听不到翻译：** 检查会议软件的麦克风是否选了知了引导安装的虚拟麦克风。
- 使用时遵守会议参与方的约定与当地法律，录音与纪要只保存在本机，不要在未告知他人的情况下传播会议内容。
