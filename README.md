# trial-verdaccio

https://verdaccio.org/docs/docker

```shell
V_PATH=~/trial-verdaccio; docker run --name verdaccio --restart always -d \
  -p 4873:4873 \
  -v $V_PATH/conf:/verdaccio/conf \
  -v $V_PATH/storage:/verdaccio/storage \
  -v $V_PATH/plugins:/verdaccio/plugins \
  verdaccio/verdaccio
```
