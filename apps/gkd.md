# GKD

- 项目主页：https://github.com/gkd-kit/gkd（GPL-3.0 许可），官网 https://gkd.li
- 作用：安卓上的自定义屏幕点击工具。按规则在指定界面自动点击（如跳过开屏广告、关闭弹窗、自动确认电脑登录）。GKD 本身不带规则，需要用户自己添加规则或订阅。
- 支持系统：Android。

## 下载渠道（按优先级）

1. 官网下载页：https://gkd.li/guide/
2. GitHub Releases：https://github.com/gkd-kit/gkd/releases/latest ，文件名 `gkd-v版本号.apk`
3. Google Play：https://play.google.com/store/apps/details?id=li.songe.gkd

## 安装步骤

1. 把 APK 下载到电脑上，告诉用户文件位置。
2. 把 APK 传到手机（数据线、局域网传输或聊天软件的文件传输都可以），在手机上点开安装。安卓可能提示“允许安装未知来源应用”，按提示允许即可。
3. 如果手机已用数据线连接并开启了 USB 调试，也可以在用户同意后用 `adb install gkd-v版本号.apk` 直接安装。

## 首次使用

- 打开 GKD 后按提示开启无障碍服务。
- 在「订阅」页添加规则：可以自己写本地规则，也可以添加订阅链接（第三方订阅列表：https://github.com/topics/gkd-subscription）。

## 验证方法

- 首页「服务状态」显示已开启，「订阅」页能看到已添加的规则。

## 常见问题

- 先看官方疑难解答：https://gkd.li/guide/faq
