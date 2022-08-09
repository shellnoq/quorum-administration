### Setup Requirements for Ubuntu 20.04 LTS

1. install essentials
````bash
sudo apt update -y &&
sudo apt install -y build-essential manpages-dev &&
sudo apt-get install -y unzip libdb-dev libleveldb-dev libsodium-dev zlib1g-dev libtinfo-dev solc sysvbanner software-properties-common default-jdk maven -y &&
sudo apt install -y git &&
sudo apt update -y 

````

2. Install go

````bash
#!/bin/bash

wget https://go.dev/dl/go1.18.5.linux-amd64.tar.gz &&
tar -xzvf go1.18.5.linux-amd64.tar.gz &&
echo "GOPATH=$HOME/go/bin" >> .bashrc &&
echo "PATH=$PATH:$HOME/go/bin">> .bashrc &&
source ~/.bashrc

````
3. install docker

````bash
sudo apt install -y apt-transport-https ca-certificates curl software-properties-common &&
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add &&
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" &&
apt-cache policy docker-ce &&
sudo apt update -y &&
sudo apt install -y docker-ce &&
sudo gpasswd -a $USER docker 


````
4. Install Geth
> https://geth.ethereum.org/docs/install-and-build/installing-geth 
> https://github.com/ethereum/go-ethereum  
> https://www.quicknode.com/guides/infrastructure/how-to-install-and-run-a-geth-node  

````bash

````

5. install QuorumMaker
````bash
git clone https://github.com/synechron-finlabs/quorum-maker 
./setup.sh
````

 
