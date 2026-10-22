# it-tools：部署到本机的网页工具箱（进阶）

- 项目主页：https://github.com/CorentinTh/it-tools（GPL-3.0 许可）
- 作用：80 多个实用小工具（二维码生成、JSON 格式化、时间戳转换、密码生成、颜色转换等），部署后在浏览器里离线使用。
- 支持系统：Windows / macOS / Linux。
- 难度：没有安装包，需要用命令行部署。执行每一步前都要向用户说明。

## 需要的运行环境

- **Node.js 18 或更高版本**（项目 `.nvmrc` 指定 18.18.2）。
- **pnpm**（项目使用 pnpm 9）。

先检查：在终端运行 `node -v` 和 `pnpm -v`。

- 没有 Node.js：征得用户同意后，从官网 https://nodejs.org 下载 LTS 版安装包安装。macOS 已有 Homebrew 时也可用 `brew install node`。
- 没有 pnpm：征得用户同意后运行 `npm install -g pnpm`。

## 部署步骤

1. **准备目录：** 征求用户同意，在用户的文档目录下新建 `it-tools` 文件夹。
2. **获取源码（二选一）：**
   - 已安装 git：`git clone --depth 1 https://github.com/CorentinTh/it-tools.git`
   - 没有 git：下载 https://github.com/CorentinTh/it-tools/archive/refs/heads/main.zip 并解压。
3. **（可选）使用国内 npm 镜像加速依赖下载：** 依赖下载很慢时，征得用户同意后，在项目目录执行 `pnpm config set registry https://registry.npmmirror.com`。这是国内公开的 npm 镜像，只影响依赖下载速度。
4. **安装依赖：** 进入项目目录，运行 `pnpm install`。
5. **启动：** 运行 `pnpm dev`，终端会显示本地地址（默认 http://localhost:5173）。
6. 用浏览器打开这个地址。

## 验证方法

- 浏览器打开 http://localhost:5173 能看到 it-tools 首页和工具列表。
- 随便打开一个工具（例如「二维码生成」），能正常使用。

## 常见问题

- **`pnpm install` 很慢或超时：** 按第 3 步切换国内镜像后重试。
- **Node 版本过低：** 安装 Node.js LTS 新版后重试。
- **端口被占用：** `pnpm dev` 会自动换一个端口，以终端显示的地址为准。
- **以后怎么再打开：** 进入项目目录运行 `pnpm dev`。关闭终端窗口即停止。
- **怎么卸载：** 删除 `it-tools` 文件夹即可。
