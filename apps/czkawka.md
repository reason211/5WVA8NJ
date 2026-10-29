# Czkawka（Krokiet 界面）

- 项目主页：https://github.com/qarmin/czkawka （代码 MIT，整体按 GPL-3.0 分发）
- 作用：免费开源、没有广告的电脑清理工具。找出重复文件、相似图片（分辨率不同、带水印也能认出）、相似视频、重复音乐（按歌名、歌手等标签或按内容比对）、大文件、空文件、空文件夹、临时文件、损坏文件等，勾选后可删除、移动到别处。用 Rust 编写，多线程扫描，第二次扫描有缓存会更快；不联网、不收集用户信息。
- 界面：Krokiet 是作者现在主推的新界面（旧的 Czkawka GTK 界面已停止更新），支持简体中文。
- 支持系统：Windows 10 / 11、macOS（苹果芯片）、Linux；安卓有触屏版 Cedinia。

## 下载渠道

- GitHub Releases：https://github.com/qarmin/czkawka/releases/latest （写作本教程时的版本是 12.0.2，文件名以 Releases 页面为准）
- 按 Releases 页面「Legend」的推荐选文件：

| 系统 | 推荐文件 | 备选（打不开时换） |
|---|---|---|
| Windows | `windows_krokiet_on_windows_skia_opengl.exe` | `windows_krokiet_on_windows_femtovg_wgpu.exe`、`windows_krokiet_on_linux.exe` |
| Mac 苹果芯片 | `mac_krokiet_skia_vulkan_arm64` | `mac_krokiet_arm64` |
| 安卓手机 | `cedinia.apk` | — |

## 安装步骤

Krokiet 是免安装的单个程序，下载后直接运行，不需要管理员权限。

- **Windows：**
  1. 在用户目录建文件夹 `%USERPROFILE%\Apps\Krokiet`，把 exe 下载进去，改名为 `Krokiet.exe`。
  2. 在桌面创建指向它的快捷方式「Krokiet」，方便用户双击打开。
- **macOS（苹果芯片）：**
  1. 在 `~/Applications/Krokiet/` 下载文件，改名为 `krokiet`，执行 `chmod +x krokiet`。
  2. 执行 `xattr -d com.apple.quarantine krokiet` 去掉下载隔离标记（执行前先告诉用户原因：这是从 GitHub 下载的未签名程序，否则系统会拦截）。
  3. 双击 `krokiet` 会在终端里启动界面；也可以在终端执行 `~/Applications/Krokiet/krokiet`。
- **安卓：** 把 `cedinia.apk` 传到手机上点击安装，需要用户自己在手机上允许「安装未知应用」。

## 切换中文界面

打开 Krokiet，点左下角齿轮（设置）→ 语言（Language）选「简体中文（zh-CN）」。切换完成后告诉用户。

## 使用方法（告诉用户）

1. 下方「包含的路径」里点加号，添加要扫描的文件夹（比如 D 盘、下载、图片文件夹）。
2. 左侧选工具：重复文件、大文件、空文件、空文件夹、临时文件、相似图片、相似视频、重复音乐等。
3. 点「扫描」，结果按组列出；右侧可以预览图片。
4. 用「选择」按钮按规则批量勾选（比如每组只保留一份），再点「删除」或「移动」。

## 验证方法

- 能打开 Krokiet 主界面，看到左侧工具列表和下方「包含的路径」。

## 常见问题

- **Windows 提示「Windows 已保护你的电脑」：** 确认文件来自上面的官方 Releases 后，点「更多信息 → 仍要运行」。执行前先告诉用户原因。
- **打开后窗口空白或闪退：** 换上表里的备选文件（不同的渲染后端）。
- **相似视频工具提示缺少 ffmpeg：** 只有这个工具需要 ffmpeg，其他工具不受影响；需要时再按项目 README 安装 ffmpeg。
- **删除前请用户自己确认**，重要数据先备份。不要替用户选择删除哪些文件。
