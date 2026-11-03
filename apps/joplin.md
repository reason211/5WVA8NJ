# Joplin

- 项目主页：https://github.com/laurent22/joplin
- 作用：免费开源的笔记和待办工具，支持笔记本分类、全文搜索、公式与流程图，以及配置同步后的多端访问。
- 支持 Windows、macOS、Linux、Android 和 iOS。

## 下载渠道

- 桌面版官方安装页：https://joplinapp.org/help/install/ ，选择适合当前系统和架构的稳定版。
- 桌面版官方发布页：https://github.com/laurent22/joplin/releases/latest ，Windows 选择 `Joplin-Setup-<版本>.exe`，苹果芯片 Mac 选择 `Joplin-<版本>-arm64.DMG`，Intel Mac 选择对应 DMG，Linux 选择 AppImage。文件名以发布页为准。
- iPhone / iPad 中国区 App Store：https://apps.apple.com/cn/app/joplin/id1315599797 ，核对开发者 Laurent Cozic。

## 安装步骤

1. 确认用户同意安装，识别系统及架构，检查软件是否已存在；不删除、覆盖或迁移用户原有笔记。
2. 通过桌面官方渠道获取对应稳定版。下载安装包后，从官方发布 API `https://api.github.com/repos/laurent22/joplin/releases/latest` 读取同名资产的 `digest`，计算 SHA-256 并逐字核对；缺少校验值或不一致时停止，不运行安装包。
3. Windows 按安装向导操作；macOS 打开 DMG 并拖入「应用程序」；Linux 按官方说明使用对应 AppImage。需要管理员授权时先说明并由用户确认。iOS 版由用户在 App Store 按提示安装。
4. 打开 Joplin，确认笔记界面可见并告知应用位置。遇安全警告时停止核实，不关闭防护或绕过系统限制。

## 使用与同步

- 使用笔记本分层整理笔记和待办，搜索框可查找内容；笔记支持公式和流程图。
- 多设备同步需用户自行选择同步服务并授权；配置同步或端到端加密前先说明数据会送往哪里，不代用户创建账号、上传现有笔记、改变同步目标或重置加密密钥。
