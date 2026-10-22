# openGym：自托管的健身记录

- 项目主页：https://github.com/DuarteSantos8/openGym（AGPL-3.0 许可）
- 作用：健身和体重记录，规划训练计划、记录每组数据、肌群热力图，无订阅、无广告，数据存在自己的服务器上。
- 两种用法：
  1. **先试用：** 浏览器打开官方在线演示 https://opengym.ch/demo/ ，不用安装。
  2. **长期使用：** 需要一台自己的服务器或常开的电脑运行服务端（Docker），手机再安装安卓 App 或用浏览器连接。这一步需要一定动手能力。

## 下载渠道

- 安卓 App：GitHub Releases https://github.com/DuarteSantos8/openGym/releases/latest 里的 `openGym-版本号.apk`
- 服务端部署说明：项目里的 `docs/SELF_HOSTING.md`

## 在电脑上部署服务端（进阶，每一步先征得用户同意）

1. 确认电脑已安装 Docker（运行 `docker -v`）。没有的话，告诉用户需要先安装 Docker Desktop，并说明它会占用一定的磁盘和内存，由用户决定是否继续。
2. 获取源码：`git clone --depth 1 https://github.com/DuarteSantos8/openGym.git`
3. 进入项目目录，按 `docs/SELF_HOSTING.md` 准备配置文件，然后运行 `docker compose pull` 和 `docker compose up -d`。
4. 按文档里给出的地址用浏览器打开，确认能看到登录页。

## 常见问题

- 只想记录训练、不想折腾服务器：直接用在线演示体验，或告诉用户这个项目需要自建服务端，可能不适合他。
