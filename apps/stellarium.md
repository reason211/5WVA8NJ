# Stellarium

- 项目主页：https://github.com/Stellarium/stellarium（GPL-2.0 许可），官网 https://stellarium.org
- 作用：电脑上的天文馆（星空模拟）。按所在地点和时间显示真实星空：默认 60 多万颗星、8 万多个深空天体，有星座连线、星座图和真实的银河；能模拟日出日落、流星、日食，调到任意日期看行星位置；还能模拟望远镜目镜里看到的样子。
- 支持系统：Windows 10 及以上（Windows 7 用 Qt5 版）、macOS 11 及以上、Linux。

## 下载渠道（只用官方）

1. GitHub Releases：https://github.com/Stellarium/stellarium/releases/latest
   - Windows 64 位：`stellarium-<版本>-qt6-win64.exe`（Windows 7/8 用 `qt5-win64.exe`，ARM 电脑用 `qt6-arm64.exe`）
   - macOS：`Stellarium-<版本>-qt6-macOS.zip`
   - Linux：`Stellarium-<版本>-qt6-x86_64.AppImage`
2. 官网首页下载区：https://stellarium.org （同样是上面这些安装包）
- 官网上的 Stellarium Web、手机版 Stellarium Mobile 是另外的产品，不需要装。

## 安装步骤

- Windows：双击 `.exe`，按提示完成安装，开始菜单里会出现 Stellarium。
- macOS：解压 zip，把 Stellarium 拖进「应用程序」。
- Linux：给 AppImage 加执行权限后直接运行。
- 界面语言默认跟随系统；不是中文时，按 F2 打开「设置」，在「主设置 → 语言」里选中文（程序语言和天空文化语言各一项）。
- 第一次打开会按网络大致定位；位置不对时按 F6 打开「位置」窗口手动选城市。

## 验证方法

- 打开 Stellarium 能看到地平线和星空；按 C 显示星座连线，按 R 显示星座图。

## 常见问题

- **Windows 提示“Windows 已保护你的电脑”：** 确认文件来自上面的官方渠道后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **macOS 提示无法验证开发者：** 到「系统设置 → 隐私与安全性」点击「仍要打开」。执行前先告诉用户原因。
- **打开后黑屏或闪退：** 多是显卡驱动太旧，先更新显卡驱动；Windows 上也可以改用 Qt5 版安装包。
