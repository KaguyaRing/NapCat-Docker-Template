<div align="center">

![:name](https://count.getloli.com/@NapCat-Docker-Template?name=NapCat-Docker-Template&theme=minecraft&padding=6&offset=0&align=top&scale=1&pixelated=1&darkmode=auto)

# NapCat-Docker-Template

</div>

## 仓库简介

该仓库是 NapCat Docker 镜像的模板，旨在帮助用户快速搭建和部署 NapCat 服务。

## 使用方法

### 安装Docker

运行以下命令安装Docker(如果已经安装Docker可以跳过此步骤)：

```bash
bash <(curl -sSL https://linuxmirrors.cn/docker.sh)
```

随后根据脚本提示完成Docker的安装。

### 下载NapCat Docker Compose文件

你可以使用以下命令将 `docker-compose.yml` 文件下载到你的项目目录中：

```bash
cd /path/to/your/project
curl -o docker-compose.yml https://raw.githubusercontent.com/KaguyaRing/NapCat-Docker-Template/main/docker-compose.yml
```

或者使用Github代理：

```bash
cd /path/to/your/project
curl -sSL-o docker-compose.yml https://gh-proxy.org/https://raw.githubusercontent.com/KaguyaRing/NapCat-Docker-Template/main/docker-compose.yml
```

> 此处的 `/path/to/your/project` 需要替换为你希望存放 `docker-compose.yml` 文件的实际路径。

- `docker-compose.yml` 只部署NapCat服务，如果你需要其他服务，请替换为相应的模板文件名称。

该项目已经提供了NapCat单服务、AstrBot+Napcat等多种模板文件(现只提供两种,如果需要更多模板，请提交issue)，您可以根据需要选择合适的模板文件进行下载。

### 启动服务

只需要在包含该仓库下载的 `docker-compose.yml` 文件的目录下运行以下命令即可启动 NapCat 服务：

```bash
docker compose up -d
```

### 查看日志

你可以使用以下命令查看 NapCat 服务的日志以获取Token登录WebUI：

```bash
docker compose logs napcat
```

### 停止服务

你可以使用以下命令停止所有服务：

```bash
cd /path/to/your/project
docker compose down
```

### 重启服务

你可以使用以下命令重启 NapCat 服务：

```bash
docker compose restart napcat
```

## 对接

NapCat 支持多种对接方式，您可以参考官方文档进行配置：

- [NapCat 对接文档](https://napneko.github.io/use/integration)

## 免责声明

为了确保 NapCat 服务的安全性,此处已经将 `调试端口` 只允许本地访问,如果你需要部署到外网调试您的NapCat，
请手动移除 `docker-compose.yml` 文件中 `napcat` 服务的 `post` 中的 `127.0.0.1`移除，
如果手动移除后遭到任何安全问题,本仓库及作者概不负责。

## 数据

该仓库的模板文件均存储在 `./data/*` 目录下，您可以根据需要进行修改和定制。

## 许可

本项目采用 [MIT](LICENSE)许可，这意味着您可以自由地使用、修改和分发本项目。
如有任何问题，欢迎提交 [issue](https://github.com/KaguyaRing/Template/issues)。

## 贡献

欢迎任何形式的贡献！如果您有任何建议或改进，请随时提交 [pull request](https://github.com/KaguyaRing/Template/pulls)。

## 致谢

致谢以下项目:

- [NapCat](https://github.com/NapNeko/NapCatQQ)

- [AstrBot](https://github.com/AstrBotDevs/AstrBot)
