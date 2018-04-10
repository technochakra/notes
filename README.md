# notes

## Docker Commands

Cleanup Docker Images 
> docker ps -a -q | xargs -n 1 -I {} docker rm {}

> docker images --filter dangling=true -q | sort -u | xargs docker rmi 

Stop all docker instances
> docker stop $(docker ps -a -q)

> docker rm $(docker ps -a -q)

## npm Commands
Add dependency to package.json
##### dev
> npm install <package_name> --save-dev

##### prod
> npm install <package_name> --save

##### check depenencies that are out of date
> npm outdated

##### upgrade depenencies in package.json
> npm-check-updates or ncu
or 
> npm update

## brew Commands
##### update brew itself and the formulae
> brew update

##### update brew installed software
> brew upgrade

##### clean old versions of brew installed software (good for reclaiming diskspace).
> brew cleanup


## Kubernetes commands
##### minikube
> minikube start

> minikube stop

> minikube status

> minikube delete

> minikube dashboard


##### kubectl
> kubectl get nodes

> kubectl cluster-info

> kubectl describe node minikube

> kubectl get deployment

> kubectl delete pods <podname>

> kubectl delete deployments <deployment name>

> kubectl get pods --all-namespaces

## Vim Commands

### format html using external program (tidy).
:!tidy -mi -xml -wrap 0 %

### ctrlp
##### start ctrlp in the working_directory
> :CtrlP working_directory

##### clear ctrlp caches
> :CtrlPClearAllCaches

## Misc Commands
##### decode base64 on commandline
> echo <base64_string> | base64 --decode
