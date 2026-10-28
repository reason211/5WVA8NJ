# Kodi

- 项目主页：https://github.com/xbmc/xbmc（GPL-2.0 许可，Kodi 的前身叫 XBMC），官网 https://kodi.tv ，官方文档 https://kodi.wiki
- 作用：免费开源的家庭影院 / 媒体中心软件。把自己的电影、剧集、音乐、照片文件夹交给它，自动扫描生成带封面、简介、背景图的媒体库；几乎所有常见的音视频格式都能播放；界面为大屏和遥控器设计，也支持播放列表、照片幻灯片、天气预报和插件。
- 支持系统：Windows、macOS（Intel 和苹果芯片）、Linux、安卓（含电视盒子）、iOS、tvOS。
- **注意：** 工具本身不提供任何影音内容，只播放和管理用户自己有权使用的文件。只用官方插件库（Kodi 自带的 “Kodi Add-on repository”），不要安装来路不明的第三方插件源。

## 下载渠道（按优先级）

- **Windows：**
  1. 微软商店（国内可直接访问，推荐）：https://apps.microsoft.com/detail/9nblggh4t892 ，或在微软商店里搜索「Kodi」。
  2. 官方安装包：官方下载页 https://kodi.tv/download/windows/ ，64 位系统用 `kodi-<版本>-Omega-x64.exe`，直链目录 https://mirrors.kodi.tv/releases/windows/win64/ （会自动跳转到就近镜像）。
- **macOS：** 官方下载页 https://kodi.tv/download/macos/
  - 苹果芯片：https://mirrors.kodi.tv/releases/osx/arm64/ ，下载 `kodi-<版本>-Omega-arm64.dmg`
  - Intel 芯片：https://mirrors.kodi.tv/releases/osx/x86_64/ ，下载 `kodi-<版本>-Omega-x86_64.dmg`
- **安卓手机 / 电视盒子（用户问到时）：** 官方下载页 https://kodi.tv/download/android/ ，64 位设备用 https://mirrors.kodi.tv/releases/android/arm64-v8a/ 里的 `kodi-<版本>-Omega-arm64-v8a.apk`。
- 写作本教程时的稳定版是 21.3（Omega），文件名随版本变化，以下载页为准；只下载稳定版，不下载 nightly、RC 等测试版。

## 安装步骤

- **Windows：**
  1. 优先用微软商店：打开商店页面点「获取 / 安装」，装完在开始菜单打开 Kodi。
  2. 没有商店时下载官方 `.exe` 安装包，双击按默认选项安装。
- **macOS：**
  1. 打开 `.dmg`，把 Kodi.app 拖进「应用程序」。
  2. 首次打开如果提示无法验证开发者，到「系统设置 → 隐私与安全性」点「仍要打开」。执行前先告诉用户原因。
- **安卓：** 把 apk 传到手机或盒子上，点开安装；系统提示“允许安装未知来源应用”时，让用户自己确认。

## 切换中文界面（首次打开后做）

Kodi 默认是英文界面，直接切中文会显示方块，要先换字体：
1. 点左上角齿轮 → Interface（界面）→ Skin → Fonts，选「Arial based」。
2. 回到 Interface → Regional → Language，选「Chinese (Simple)」。
3. 界面变成中文后，告诉用户切换完成。

## 使用方法（告诉用户）

1. 打开 Kodi，左侧选「电影」或「剧集」→「进入文件区」→「添加视频…」，选择自己的影视文件夹。
2. 「设置内容」里把类型选成电影或剧集，信息来源保持默认（The Movie Database），扫描完成后就会出现海报墙、简介和背景图。
3. 照片在「图片」里添加文件夹，选中后可以从这里开始幻灯片播放。
4. 文件夹按“电影名 (年份)”命名，剧集按“剧名/Season 1/剧名 S01E01”命名，更容易匹配到海报和简介。

## 验证方法

- 能打开 Kodi，看到带「电影 / 剧集 / 音乐 / 图片」菜单的主界面。

## 常见问题

- **中文显示成方块：** 先按上面的步骤把字体换成「Arial based」，再切语言。
- **海报没出来：** 等扫描完成；检查文件夹命名，或在该文件夹上「设置内容」重新扫描。
- **Windows 防火墙弹窗：** 只在本机用时可以不允许；要用手机遥控或局域网共享时允许“专用网络”。执行前先告诉用户原因。
- 只播放和管理你有权使用的影音文件。
