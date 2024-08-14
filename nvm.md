# nvm 备忘清单

## nvm 快速使用

```shell
# 下载并安装 Node.js 20 版本
nvm install 20
# 验证环境中的 Node.js 版本是否正确
node --version # 应该打印“v20.11.1”
# 验证环境中是否存在正确的 NPM 版本
npm --version # 应该打印“10.2.4”
```

## nvm 展示当前使用版本

```shell
nvm current
```

## nvm 安装指定版本的 node 程序

<!--rehype:wrap-class=row-span-2-->

version 设置为 `latest` 安装最新版本或者设置为 "lts" 安装最近的 LTS（长期支持）版本。

```shell
nvm install <version> [arch]
```

`arch` 可以指定 `32` 或者 `64` 位版本（默认跟随系统），设置为 `all` 同时安装 32 和 64 位版本。在命令最后添加 `--insecure` 将跳过远程下载服务器的 SSL 验证。

## nvm 切换使用指定版本

```shell
nvm use <version> [arch]
```

## nvm 列出 node.js 已安版本

可选输入 available 显示可获取的版本下载列表。

```shell
nvm list [available]
```

## nvm 卸载指定版本

<!--rehype:wrap-class=row-span-2-->

```shell
# <version> 可选设置 latest/lts/newest
nvm uninstall <version>
```

启用 `newest` 指定最近安装版本。

```shell
nvm use <arch> # 可选指定32/64位架构
```

将继续使用当前版本，但是将切换为指定架构程序。

## nvm 查看 node 运行模式

```shell
nvm arch [32|64]
```

查看 node 程序是运行在 `32` 位还是 `64` 位模式下，指定 `32` 或者 `64` 覆盖默认运行架构模式

## nvm 检查 NVM4W 进程已知问题

```shell
nvm check
```

## nvm 启用/关闭 node.js 版本管理

```shell
nvm on  # 启用
nvm off # 关闭 - 不会执行任何卸载操作
```

## nvm 设置下载代理

```shell
nvm proxy [url]
```

可选 url 留空查看当前使用代理，设置为 "none" 移除代理设置。

## nvm 设置版本存储目录

设置 nvm 储存不同版本的 node.js 的目录。如果未设置 path，将展示当前存储目录。

```shell
nvm root <path>
```

## nvm 展示当前 nvm 使用版本

```shell
nvm version
```

## nvm 指定 node 镜像

```shell
nvm node_mirror <node_mirror_url>
```

## nvm 指定 npm 镜像

```shell
nvm npm_mirror <npm_mirror_url>
```
