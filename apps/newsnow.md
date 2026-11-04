# NewsNow

- 上游项目：https://github.com/newsnext/newsnow （MIT，原 `ourongxing/newsnow` 跳转到该仓库）
- 作用：在一个网页集中看常见平台热榜，切换最热/实时，关注常看的来源；更新频率随来源和缓存不同，不是全部榜单每2分钟更新。
- 本地网页服务；官方 Docker 配置端口为4444。

## 先说明并取得同意

已有 Docker 则复用；需要安装 Docker Desktop 或启动容器时先说明用途和资源占用。不创建系统级服务，不设置业务开机自启，不把服务直接开放到公网。

## 本地部署

1. 读取上游仓库的 README 和 `docker-compose.yml`，从官方镜像 `ghcr.io/ourongxing/newsnow:latest` 部署。
2. 将端口映射设置为 `127.0.0.1:4444:4444`，保留上游持久化卷 `newsnow_data:/usr/app/.data`。
3. 容器内部环境沿用官方配置：`HOST=0.0.0.0`、`PORT=4444`、`NODE_ENV=production`、`INIT_TABLE=true`、`ENABLE_CACHE=true`。基础浏览不需要替用户注册GitHub OAuth应用；需要账号跨设备同步时再按上游文档配置，凭据由用户在本机提供。
4. 用户同意后，在该目录运行 `docker compose up -d`。若同名容器已存在，先核对是不是本项目实例，不覆盖或删除别人的服务。
5. 浏览器打开 `http://127.0.0.1:4444`。

也可按上游“Development”使用 Node.js 20+ 和 pnpm；复用已有环境，避免不必要的全局安装。

## 验证和交付

- 本地页面能打开，至少一个可用来源正常显示；能进入最热/实时页面。对网络失败的来源如实说明，不伪造内容或宣称所有源都已验证。
- 说明本地网址、项目目录、启动/停止方式；本地关注与账号云同步区分说明。
- 停止本项目：`docker compose stop`。保留数据卷，不擅自删除用户的关注、数据库或配置。
