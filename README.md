# notes

## Docker Commands

Cleanup Docker Images 
> docker ps -a -q | xargs -n 1 -I {} docker rm {}

> docker images --filter dangling=true -q | sort -u | xargs docker rmi 

> docker system prune

Stop all docker instances
> docker stop $(docker ps -a -q)

> docker rm $(docker ps -a -q)

docker-compose commands
> docker-compose build

> docker-compose up

> docker-compose start

> docker-compose stop

> docker-compose logs

> docker-compose ps




## npm Commands
Add dependency to package.json
##### dev
> npm install <package_name> --save-dev

##### prod
> npm install <package_name> --save

##### check dependencies that are out of date
> npm outdated

##### upgrade dependencies in package.json
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

> brew cask reinstall minikube

##### start minikube using hyperkit (need to brew install it)
> minikube --vm-driver=hyperkit



##### kubectl

##### get all resource types - pods, services, deamonsets, replicasets, etc.
> kubectl get all --all-namespaces -o wide

> watch kubectl get all --all-namespaces -o wide

##### get more data of resource types
> kubectl describe all --all-namespaces

> kubectl get nodes

> kubectl cluster-info

> kubectl describe node minikube

> kubectl get deployment

> kubectl delete pods <podname>

> kubectl delete deployments <deployment name>

> kubectl get pods --all-namespaces


##### Install busybox and run network utilities
> kubectl exec busybox nslookup kubernetes.default

## Raspberry Pi

##### Setup WiFi 
> sudo raspi-config

##### Check SSID currently connected to
> iwgetid

##### Scan SSIDs
> sudo iwlist wlan0 scan

##### Manually edit SSIDs
> sudo vi /etc/wpa_supplicant/wpa_supplicant.conf

## Vim Commands

### format html using external program (tidy).
> :!tidy -mi -xml -wrap 0 %

### ctrlp
##### start ctrlp in the working_directory
> :CtrlP working_directory

##### clear ctrlp caches
> :CtrlPClearAllCaches

## Misc Commands
##### decode base64 on commandline
> echo <base64_string> | base64 --decode

##### generate random password on commandline
> openssl rand -base64 13

##### process json in bash
> curl -s  url_that_returns_json | jq  '.field_in_json'

## Octave Commands
##### Fix GNU Plot QT errors on Mac
> setenv("GNUTERM","qt")

## ssh
##### generate ssh keys
> ssh-keygen -t rsa -b 4096 -C "<email_id>@gmail.com"

##### start ssh-agent
> eval "$(ssh-agent -s)"
> ssh-add -K path_to_id_pub_file


## git
##### revert local changes to a file
> git checkout -- <file>
  
##### create tag
> git tag -a <tagname>
 


