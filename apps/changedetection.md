# changedetection.io

- 上游项目：https://github.com/dgtlmoon/changedetection.io （Apache-2.0），官网 https://changedetection.io
- 作用：盯住你关心的网页，页面一有变化就发通知。适合蹲商品降价、补货，看官网公告、学校通知、招聘页和软件更新有没有新内容。能按字、按行对比改了什么，商品页可以画价格曲线、设置低于多少钱才提醒。
- 通知通过 Apprise 发送，支持邮箱、Telegram、Discord、钉钉、飞书、企业微信群机器人、Bark 等一百多种方式。
- 本地网页服务，装好后用浏览器打开 `http://127.0.0.1:5000`。官方另有付费托管版，本教程只装开源版到用户自己的电脑。

## 先说明并取得同意

需要安装 Python 3.11 或更新版本（已装就复用）。安装前告诉用户会装什么、装在哪里。不创建系统服务，不设置开机自启，不把服务开放到公网。

## 安装步骤（推荐 Python pip，按官方 Windows wiki）

1. 检查 `python --version`（macOS/Linux 用 `python3`），低于 3.11 时从 https://www.python.org/downloads/ 安装官方版本。Windows 安装时勾选“Add python.exe to PATH”。
2. 新建数据目录，例如 Windows 的 `%USERPROFILE%\changedetection-data`，macOS/Linux 的 `~/changedetection-data`。
3. 建议在虚拟环境里安装，避免影响用户已有的 Python 包：
   - Windows：`python -m venv %USERPROFILE%\changedetection-venv`，然后 `%USERPROFILE%\changedetection-venv\Scripts\pip install changedetection.io`
   - macOS/Linux：`python3 -m venv ~/changedetection-venv && ~/changedetection-venv/bin/pip install changedetection.io`
4. 启动（端口默认 5000）：
   - Windows：`%USERPROFILE%\changedetection-venv\Scripts\changedetection.io -d %USERPROFILE%\changedetection-data -p 5000`
   - macOS/Linux：`~/changedetection-venv/bin/changedetection.io -d ~/changedetection-data -p 5000`
5. 浏览器打开 `http://127.0.0.1:5000`。

也可以用官方 Docker：`docker run -d --restart always -p "127.0.0.1:5000:5000" -v datastore-volume:/datastore --name changedetection.io docker.io/dgtlmoon/changedetection.io`。用户已有 Docker 时可选，没有就用上面的 pip 方式，不为此额外安装 Docker。

## 验证和交付

- 浏览器能打开 `http://127.0.0.1:5000`，看到顶部的“Web page URL”输入框。
- 告诉用户：访问地址、数据目录、启动命令；关掉命令行窗口服务就会停止，下次用同一条命令启动。
- 简单教用户用：把网址粘进输入框点 “Watch”；商品页在 “Edit → Restock & Price Detection” 里设置补货和价格提醒；在 “Notifications” 填通知地址（如 `mailto://`、`tgram://`、`dingtalk://`、`feishu://`、`bark://`，格式见 https://appriseit.com/services/ ）。

## 常见问题

- **端口 5000 被占用：** 换一个端口，例如 `-p 5050`，再打开 `http://127.0.0.1:5050`。
- **有的网页抓不到内容：** 默认抓取方式不运行网页里的 JavaScript。需要时按官方 wiki “Fetching pages with WebDriver” 配置 Chrome 抓取，先向用户说明再装。
- **使用边界：** 只监控你有权访问的页面，遵守网站的服务条款和 robots 规则，检查间隔不要设得太短。
