# trial-verdaccio

[Vercaccio 官方文档](https://verdaccio.org/docs/docker)

# 下载默认配置文件到 conf 目录

```shell
curl -o conf/config.yaml https://raw.githubusercontent.com/verdaccio/verdaccio/5.x/conf/docker.yaml
```

# 配置路径并启动 Docker

```shell
V_PATH=~/trial-verdaccio; docker run --name verdaccio --restart always -d \
  -p 4873:4873 \
  -v $V_PATH/conf:/verdaccio/conf \
  -v $V_PATH/storage:/verdaccio/storage \
  -v $V_PATH/plugins:/verdaccio/plugins \
  verdaccio/verdaccio

# 文件操作权限
sudo chown -R 10001:65533 $V_PATH
```

# 通过 nrm 配置注册源

```shell
pnpm add -g nrm
nrm add verdaccio [Verdaccio Web URL]
nrm use verdaccio
```
