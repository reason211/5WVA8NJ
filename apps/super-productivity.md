# Super Productivity

- 项目主页：https://github.com/super-productivity/super-productivity（MIT 许可），官网 https://super-productivity.com ，文档 https://github.com/super-productivity/super-productivity/wiki
- 作用：免费开源的待办清单 + 时间记录 + 日程规划工具。快速添加任务、把任务拖进日程表、看板和四象限（艾森豪威尔矩阵）分类、番茄钟 / 心流计时 / 倒计时专注、休息提醒、自动记录每个任务花的时间并生成工作记录。数据默认只存在本机，不需要注册账号。
- 支持系统：Windows、macOS（苹果芯片和 Intel）、Linux、安卓、iOS，也有网页版。
- 界面支持简体中文。

## 下载渠道（按优先级）

- **Windows：**
  1. 微软商店（国内可直接访问，推荐）：https://apps.microsoft.com/detail/9nhfvg8361tw ，或在微软商店里搜索「Super Productivity」。
  2. GitHub Releases：https://github.com/super-productivity/super-productivity/releases/latest ，下载 `Super-Productivity-Setup.exe`（安装版）。
- **macOS：**
  1. App Store（中国区可直接下载，推荐）：https://apps.apple.com/cn/app/super-productivity/id1482572463
  2. GitHub Releases：苹果芯片下载 `superProductivity-arm64.dmg`，Intel 芯片下载 `superProductivity-x64.dmg`。
- 写作本教程时的版本是 v19.3.1，文件名以 Releases 页面为准。

## 安装步骤

- **Windows：**
  1. 优先用微软商店：打开商店页面点「获取 / 安装」，装完在开始菜单打开 Super Productivity。
  2. 没有商店时下载 `Super-Productivity-Setup.exe`，双击按提示安装。
- **macOS：**
  1. 优先用 App Store：打开链接点「获取」，需要用户自己确认 Apple ID，不要替用户输入密码。
  2. 用 dmg 时打开后把 Super Productivity.app 拖进「应用程序」。首次打开如果提示无法验证开发者，到「系统设置 → 隐私与安全性」点「仍要打开」。执行前先告诉用户原因。

## 切换中文界面

打开软件后进入「Settings（设置）」→「Language（语言）」，选「中文（简体）」。界面改为中文后告诉用户切换完成。

## 使用方法（告诉用户）

1. 按 `Shift + A`（或点顶部 +）快速添加任务，可以直接写预计时间，如“写作业 1h”。
2. 左侧「日程」里把任务拖到对应时间段，安排好一天。
3. 左侧「看板」里有「艾森豪威尔矩阵」，按紧急、重要分成四格。
4. 点任务旁的播放按钮开始计时；顶部的专注模式里可选番茄钟、心流计时、倒计时。
5. 每天的任务和用时会自动记下，在「工作记录 / 历史」里查看。

## 验证方法

- 能打开 Super Productivity，看到「今天」任务列表界面。

## 常见问题

- **界面是英文：** 按上面的步骤在设置里切换语言。
- **想在多台设备同步：** 设置里的「同步」支持 WebDAV、Dropbox 或官方 SuperSync，需要用户自己选择和登录，不要替用户填写账号密码。
- 数据默认保存在本机，卸载前如需保留，先在设置里导出备份。
