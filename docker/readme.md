# docker command

### remove `<none>` TAG images
```
# https://stackoverflow.com/questions/33913020/docker-remove-none-tag-images
docker image prune --filter="dangling=true"

# https://forums.docker.com/t/how-to-remove-none-images-after-building/7050/7
docker rmi $(docker images --filter "dangling=true" -q --no-trunc)
```

### check logs
```
#v1
docker container logs <container>

#v2
docker logs <container>
```
