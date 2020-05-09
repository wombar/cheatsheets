# Docker Cheatsheet

### Containers

`docker ps -a` - list ALL containers

`docker rm -f container_name` - Stop and remove container

`docker exec -it container_name /bin/bash` - Connects with an interactive terminal to the container_name 

`ctrl + p --> ctrl + q` - Exit interactive terminal without stopping container

`docker run -itd --name [CONTAINER_NAME] [IMAGE_NAME]` - Start detached container with name and image

`docker rm -f $(docker ps -a -q --filter "name=aws*")` - Remove all containers with `aws` in the beginning of their name

#### OPTIONS

`--network=[NETWORK]` - Join network (must exist first)

`-p 8000:80` - Expose ports `EXTERNAL NETWORK:INTERNAL NETWORK`

`-v /projects/src:/var/www/html` -- create a volume/share `EXTERNAL:INTERNAL`

`--volume-driver=nfs` - Use for mounting NFS mounts on host system


### Images

`docker image ls` - List all images on a host

`docker rmi $(docker images | grep "^<none>" | awk "{print $3}")` - Remove untagged images


### Container Customisation

#### Build an Image
Run the following command from the directory containing the compose file

`docker build -t [TEMPLATE_NAME] .` - Template name *AND* the dot is needed


### Networks

`docker network create [NETWORK]` - Create new network

`docker network connect [NETWORK] [CONTAINER_NAME]` - Connect container to network


### Volumes

`docker volume rm $(docker volume ls -f dangling=true -q)` - Remove any dangling volumes


### Utility Functions

#### Backup MySQL Database 
`docker exec -i CONTAINER /usr/bin/mysqldump -u root --password=root DATABASE > backup.sql` -- Backup a db from a running mysql docker container

#### Restore MySQL Database
`cat SQL_FILE.sql | docker exec -i CONTAINER_NAME /usr/bin/mysql -u root --password=root_password DATABASE_NAME` - Restore a database from a mysqldump file

`for f in *.gz ; do zcat "$f" "${f%}" | mysql -u root --password=root_password database_name` - Restore multiple gz backup files into mysql database

# DOCKER-COMPOSE

`docker-compose up --build` - Runs the compose and builds at the same time

`docker-compose up -d` - load container(s) from compose file (docker-compose.yml)

