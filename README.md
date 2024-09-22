# docker-destroy

Useful for your local dev environment. You can copy `docker-destroy` to your home directory and run `./docker-destroy` to wipe your docker environment. 

Overview: 

### Stop all running containers
docker ps -a -q | xargs --no-run-if-empty docker stop

### Remove all containers
docker ps -a -q | xargs --no-run-if-empty docker rm

### Remove all images
docker images -a -q | xargs --no-run-if-empty docker rmi

### Remove all volumes
docker volume ls -q | xargs --no-run-if-empty docker volume rm

### Remove all networks except default ones
docker network ls -q | grep -vE '^(bridge|host|none)$' | xargs --no-run-if-empty docker network rm

### DESTROY
docker system prune -f

