# notes

## Docker Commands

Cleanup Docker Images 
> docker ps -a -q | xargs -n 1 -I {} docker rm {}

> docker images --filter dangling=true -q | sort -u | xargs docker rmi 

Stop all docker instances
> docker stop $(docker ps -a -q)
> docker rm $(docker ps -a -q)
