# Immich

- 项目主页：https://github.com/immich-app/immich （AGPL-3.0）；官方文档：https://docs.immich.app/ 。
- 作用：在自己的电脑或 NAS 上运行照片管理服务，手机可选择相册上传；支持人物聚类、地点浏览和共享相册。
- 手机客户端有 Android 与 iOS 版本。自建服务通过 Docker Compose 运行；部署和首次创建管理员是单独步骤，不要承诺装好即自动配置完成。
- 重要：同步或自建相册不是唯一备份。保留手机原件和独立备份，确认可恢复前不要删除原件；遵循项目 README 的 3-2-1 备份建议。

## 官方渠道

- 官方安装文档：https://docs.immich.app/install/docker-compose/ ，以当前稳定版说明为准。
- 官方稳定版及文件校验：https://github.com/immich-app/immich/releases/latest ，不要使用 main 分支的 Compose 文件替代当前发行版文件。
- iPhone / iPad 中国区 App Store：https://apps.apple.com/cn/app/immich/id1613945652 ，发行者 FUTO Holdings, Inc.；Android 从 https://immich.app/download/ 指向的官方渠道取得。
- 官方 Docker 文档：https://docs.docker.com/ 。Immich 可选择付费支持开发，不擅自购买。

## 部署步骤

1. 先确认用户是否同意安装、准备好长期运行的电脑或 NAS、可用空间及独立备份；识别系统和架构，检查是否已有 Docker 与 Compose。安装 Docker、需要管理员授权或修改防火墙时，先解释并征得同意；不要绕过安全提示。
2. 确认已有 Immich、同名容器、2283 端口及目标目录是否冲突。若存在已有服务或数据，先停下确认，不覆盖、删除或重建。新建用户同意的独立目录；将照片存储和数据库设置到专用位置，数据库不要放在不受支持的网络文件系统上。
3. 按官方安装文档下载**同一稳定发行版**的 `docker-compose.yml` 和 `example.env`，逐一核对官方 GitHub Release API 同名资产的 SHA-256 `digest`；缺失或不匹配就暂停。将环境模板按文档复制为 `.env`，不读取、输出或上传用户已有的密钥和照片。
4. 按官方文档设置独立的 `UPLOAD_LOCATION`、`DB_DATA_LOCATION` 和强随机 `DB_PASSWORD`；密码不得写进聊天或日志，限制配置文件访问权限。核对容器、端口和目录后，经用户同意再运行 `docker compose up -d`。不执行 `docker compose down -v`、清理卷或任何会删除现有数据的命令。
5. 默认不要把服务暴露到公网；如手机需要连接，先与用户确认受信任的局域网访问方式、监听范围和防火墙设置。完成后给用户实际可访问地址，请用户在浏览器自行创建管理员账号；不要声称预先生成了管理员密码。
6. 手机端由用户自行安装官方 App，并在用户授权后连接该地址和选择要备份的相册。首次只用少量自有照片测试；确认照片可查看、独立备份可恢复后，才说明如何按人物、地点或共享相册整理。不要自动删除手机原图或把私人照片发送给第三方。

## 验收和汇报

- 核对服务容器的真实运行状态；浏览器实际打开的是新部署的 Immich 首次设置页，不能用示意图冒充部署成功。
- 汇报服务地址、部署目录、照片与数据库存储位置、后续启动方法和未完成项；不展示密码、会话令牌或私人照片。
