# Lift Docker Base

**Version:** 0.1.0-alpha

### What is this?
This is a repository starter for local WordPress development using Docker.

### Requirements
- Docker for Mac/Windows

### What's Inside
- nginx:latest
- phpfpm:latest (php7)
- mysql:latest
- memcached (with a d) object cache
- mailhog
- xdebug
- composer
- wp-cli

### Getting started
1. Clone this Repo
2. cd into the cloned directory and run `docker-compose up -d`
3. Navigate to http://localhost:8080
4. Complete WordPress setup

## Theme Development
1. Add a new theme folder to `code/themes`
2. Activate it from the admin
3. Make an awesome theme!

### Useful Commands
- List containers: `docker ps -a`
- SSH into a container: `docker exec -it nginx /bin/bash`
- Bring the environment down: `docker-compose down`
- Restart a container: `docker-compose restart nginx`
- Rebuild containers: `docker-compose up -d --build`

### Other Commands
_Use these at your own risk_
- Stop all containers: `docker stop $(docker ps -aq)` _All containers, not just this environment's_
- Kill all containers: `docker kill $(docker ps -aq)`
- Destroy all container images: `docker rmi -f $(docker images -q)`
- Destroy all mounted volumes: `docker volume rm $(docker volume ls |awk '{print $2}')`

### Todo
- Create a workflow where full project manifests are stored in a composer.json
- Add PHPunit container attached to a separate mysql container
- Add node.js container with npm and webpack and preconfigured build scripts
- Add PHP CodeSniffer
- Add deploy scripts
- Add CI scripts