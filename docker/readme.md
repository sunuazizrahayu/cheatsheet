# docker command

### remove `<none>` TAG images
```
# https://stackoverflow.com/questions/33913020/docker-remove-none-tag-images
docker image prune --filter="dangling=true"
```
