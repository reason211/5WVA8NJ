# SumatraPDF

- 项目主页：https://github.com/sumatrapdfreader/sumatrapdf （GPL-3.0），官网 https://www.sumatrapdfreader.org
- 作用：免费开源的轻量阅读器，没有广告、不捆绑软件、不需要订阅。打开文档很快、占用内存少；一个软件就能看 PDF、EPUB、MOBI、漫画（CBZ / CBR）、DjVu、XPS、CHM 和图片；多个文档开成标签页切换；看漫画可以双页并排，开「漫画模式」从右往左翻页；`Shift+I` 一键反色，白底变黑底，也能在设置里换深色主题。
- 支持系统：Windows 7 / 8 / 10 / 11（32 位、64 位、ARM64）。
- 界面支持简体中文。

## 下载渠道（按优先级）

- 官网下载页：https://www.sumatrapdfreader.org/download-free-pdf-viewer
  - 64 位安装版：https://www.sumatrapdfreader.org/dl/rel/3.6.1/SumatraPDF-3.6.1-64-install.exe
  - 64 位便携版（免安装，解压即用）：https://www.sumatrapdfreader.org/dl/rel/3.6.1/SumatraPDF-3.6.1-64.zip
  - ARM64 电脑用 `SumatraPDF-3.6.1-arm64-install.exe`，32 位系统用 `SumatraPDF-3.6.1-install.exe`。
- GitHub Releases：https://github.com/sumatrapdfreader/sumatrapdf/releases
- WinGet：`winget install -e --id SumatraPDF.SumatraPDF`
- 写作本教程时的稳定版本是 3.6.1。下载前先打开官网下载页，确认有没有更新的稳定版（不要装 pre-release 预发布版）。

## 安装步骤

1. 先按 `$env:PROCESSOR_ARCHITECTURE` 判断电脑是 AMD64 还是 ARM64，下载对应的安装版。
2. 双击安装包，点「Install SumatraPDF」，装完会自动打开。
3. 用户想免安装时，下载便携版 zip，解压到用户目录（例如 `%USERPROFILE%\Apps\SumatraPDF\`），双击 `SumatraPDF-3.6.1-64.exe` 运行。
4. 装好后告诉用户软件位置（安装版默认在开始菜单搜「SumatraPDF」，便携版就是解压出来的 exe）。

## 使用方法（告诉用户）

1. 把 PDF、EPUB、漫画压缩包（.cbz / .cbr）直接拖进窗口就能看；首页「最近打开」会显示最近看过的文档封面。
2. 每个文档开一个标签页，`Ctrl+Tab` 切换标签页，`Ctrl+W` 关闭，`Ctrl+Shift+T` 恢复刚关掉的。
3. 看漫画：`Ctrl+7` 双页并排，菜单「查看」→「漫画模式」（Manga Mode）从右往左翻页。
4. 晚上看：`Shift+I` 反色，白底变黑底；或在设置 → 主题里换深色主题。
5. `Ctrl+K` 打开命令面板，输入功能名就能找到对应命令。
6. 想把它设成默认 PDF 阅读器：设置 → 选项里勾选，或在 Windows 设置的「默认应用」里选择 SumatraPDF。

## 验证方法

- 能打开 SumatraPDF，看到首页「最近打开」（Recently Opened）界面。

## 常见问题

- **界面是英文：** 菜单 → Settings → Change Language 选「简体中文」。
- **浏览器或杀毒软件提示下载文件不常见：** 只从上面的官网或 GitHub Releases 下载，核对文件名和版本号；不要从第三方下载站下载。
