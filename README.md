# Docker and  volumes

## Create a shared volume
```bash
docker volume create --driver local \
    --opt type=none \
    --opt device=/ \
    --opt o=bind shared
```
## Run app1
```bash
docker-compose run app1
```
## Run app2
```bash
docker-compose run app2
```

## Add a file in app1 @ /tmp
```bash
touch /tmp/test.txt
```
You will then be able to see the file ùin app2 @ /tmp