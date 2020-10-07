# Docker and  volumes
## First Technique
You need to create the shared volume first and use it in the docker compose file.
### Create a shared volume
```bash
docker volume create --driver local \
    --opt type=none \
    --opt device=/$PWD \
    --opt o=bind shared
```
### Run app1
```bash
docker-compose f docker-compose-first-technique.yml run app1
```
### Run app2
```bash
docker-compose f docker-compose-first-technique.yml run app2
```

## Second Technique
You can create the shared volume within the docker compose file.
### Run app1
```bash
docker-compose f docker-compose-second-technique.yml run app1
```
### Run app2
```bash
docker-compose f docker-compose-second-technique.yml run app2
```
