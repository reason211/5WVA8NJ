# Boring Notch

- 项目主页：https://github.com/TheBoredTeam/boring.notch（GPL-3.0 许可）
- 作用：把 MacBook 的刘海变成“灵动岛”。鼠标移上去展开，显示正在播放的音乐和控制按钮、日历、电量；可以把文件拖进去暂存，用隔空投送发出。
- 支持系统：仅 macOS，需要 macOS 14 Sonoma 或更高版本，Apple 芯片和 Intel 芯片的 Mac 都支持
- **注意：** 这款软件只支持 macOS。用户是 Windows 时，如实说明，不要尝试安装。

## 下载渠道（按优先级）

1. GitHub Releases：https://github.com/TheBoredTeam/boring.notch/releases/latest（文件名 `boringNotch.dmg`）
2. Homebrew：`brew install --cask TheBoredTeam/boring-notch/boring-notch`（会自动处理下面的安全提示）

## 安装步骤

- macOS：打开 `.dmg`，把 Boring Notch 拖进「应用程序」。

## 首次打开

项目目前没有苹果开发者签名，第一次打开会提示“无法验证开发者”。这是项目 README 里说明的正常情况，处理方法按 README 推荐：

```bash
xattr -dr com.apple.quarantine "/Applications/Boring Notch.app"
```

执行前先告诉用户这条命令的作用（去掉这个应用的隔离标记，只影响这一个应用），用户同意后再执行。然后正常打开应用。

## 验证方法

- 打开后，把鼠标移到屏幕顶部的刘海处，刘海会展开。
- 菜单栏出现星星图标，点开能进入设置。

## 常见问题

- **Mac 没有刘海：** 也能用，会在屏幕顶部中间显示。
- **系统低于 macOS 14：** 无法安装，如实告诉用户。
