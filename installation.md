
# Installation

For dockeriot use we need to install docker under an ARM based arquitecture, that is common for embedded systems. 
we are going to describe a basic installation for the raspberry pi3 platform using the raspbian operative system.

## Raspbian intallation
### Download raspbian
```
wget https://downloads.raspberrypi.org/raspbian_lite_latest
```
### Execute raspbian installation on an SD
You have to plug an SD into a Linux, MAC or Windows based computer
```
dd bs=4M if=2017-11-29-raspbian-stretch.img of=/dev/sdX conv=fsync
```
### Configure network interfaces


### Install docker
```
$ curl -s https://packagecloud.io/install/repositories/Hypriot/Schatzkiste/script.deb.sh | sudo bash
$ sudo apt-get install docker-hypriot=1.10.3-1
$ sudo sh -c 'usermod -aG docker $SUDO_USER'
$ sudo systemctl enable docker.service
$ systemctl unmask docker.service
$ systemctl unmask docker.socket
$ systemctl start docker.service
```
### Check that docker is running
```
$ sudo docker run hello-world   
$ sudo docker info 
$ docker rmi hello-world 
```
### Install docker-compose 

### Check that docker-compose is up and running

* All these steps can via automated script install.sh

## Dockeriot installation
* script install.sh
## Check that dockeriot is up and running
* check_dockeriot.sh
