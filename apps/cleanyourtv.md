# CleanYourTV

- 项目主页：https://github.com/Gathin23/cleanyourtv（MIT），官网 https://cleanyour.tv
- 作用：通过局域网 Wi-Fi（ADB）连接 Android TV 或 Google TV，备份后按机型清单停用广告、遥测服务与不需要的预装应用（不卸载系统软件、不需 root 或刷机），并安装约 572 KB 的极简桌面替换广告首页，随时可一键恢复。
- 支持系统：电视端需 Android TV / Google TV（桌面 APK 要求 Android 8.0 / API 26 及以上）；电脑端支持 Windows、macOS、Linux（连接同一局域网操作）。

## 下载渠道（按优先级）

1. GitHub 仓库与最新标签：https://github.com/Gathin23/cleanyourtv
   - 克隆或下载仓库：`git clone https://github.com/Gathin23/cleanyourtv.git`
   - 社区机型配置清单：`examples/`（已收录 488 个机型、132 个品牌的停用列表与说明）
2. 官网说明：https://cleanyour.tv

## 安装与使用步骤

- **1. 电视端开启网络调试：** 打开电视「设置 → 设备偏好设置 → 关于」，在「版本号 / Build」上连续按 7 次确定开启开发者模式；返回进入开发者选项，开启 USB 调试和网络（ADB）调试。记录电视局域网 IP（需用户手动在电视遥控器上操作）。
- **2. 电脑端准备环境与备份：** 在电脑克隆仓库并配置 Python 3 虚拟环境（`python3 -m venv tools/venv` 安装 `tools/requirements.txt`），设置 `TV_HOST=<电视IP>` 后运行 `tools/tv.py --probe` 读取机型与固件信息，并保存已安装应用快照（电视弹出调试授权弹窗时，需要用户在电视上点击确认允许）。
- **3. 停用广告服务与安装简洁桌面（需用户确认）：** 核对与自己机型一致的停用清单后运行 `tools/disable.sh examples/<对应机型>/debloat.txt`（仅执行 `pm disable-user`，不删除系统应用）；需要安装并切换极简桌面时，按仓库说明配置 JDK 17 与 Android SDK 34，运行 `launcher/build-and-install.sh`（Windows 用 `launcher\build-and-install.ps1`）。
- **4. 随时恢复原样：** 运行 `tools/restore.sh examples/<对应机型>/debloat.txt` 即可按操作前记录恢复全部停用的组件与原始桌面。

## 验证方法

- 电视重启或按遥控器 Home 键后进入 CleanYourTV 清爽桌面，常用视频应用（如云视听小电视、芒果TV、Kodi 等）与输入源/网络/设置入口正常可用，无首页横幅广告；停用前后的备份记录保存在本地。

## 常见问题

- **部分中国大陆版电视拒绝侧载或替换默认桌面：** 如部分大陆版固件会限制第三方 HOME 桌面或缺少标准 ADB 入口，请先在 `examples/README.md` 和 `docs/devices/` 中核对同型号及固件记录，确认支持后再操作。
- **需要配对码的无线调试（Android 11+）：** 若电视不直接开放 5555 端口，先用 `adb pair` 完成无线调试配对再连接。
- **不小心停用了需要的功能：** 使用 `tools/restore.sh` 一键还原操作前保存的状态即可。
