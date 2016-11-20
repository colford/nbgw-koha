# nbgw-koha
Koha instance creation on AWS

* Start the Ubuntu instance on AWS
* Log in to the instance
* sudo apt-get install git
* git clone https://github.com/colford/nbgw-koha.git
* sudo apt-get install apt-transport-https ca-certificates
* sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
* sudo vi /etc/apt/sources.list.d/docker.list

  deb https://apt.dockerproject.org/repo ubuntu-trusty main 

* lsb_release -a
* sudo apt-get update
* sudo apt-get purge lxc-docker
* apt-cache policy docker-engine
* sudo apt-get update
* sudo apt-get install linux-image-extra-$(uname -r) linux-image-extra-virtual
* sudo apt-get update
* sudo apt-get install docker-engine
* sudo service docker start
* sudo groupadd docker
* sudo usermod -aG docker $USER
* sudo curl -L "https://github.com/docker/compose/releases/download/1.8.0/docker-compose-$(uname -s)-$(uname -m)" > docker-compose
* chmod +x docker-compose
* sudo cp docker-compose /usr/local/bin/.
* docker-compose up
