# docker-destroy

Useful for your local dev environment.

Overview: 

### Have a look at docker system rescource usage
docker system df

### Remove images
docker image prune -a -f

### Remove build cache
docker buildx prune -f

### Remove all volumes
docker volume prune -f

### DESTROY -- tbh, just do this if you mess everything up.
docker system prune -a

### Useful link
https://depot.dev/blog/docker-clear-cache
