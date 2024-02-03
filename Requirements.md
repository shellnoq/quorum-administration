### Setup Requirements for Ubuntu 20.04 LTS

____
1. install tools, 
2. setup nodes
3. setup monitoring tools
4.
____
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

wget https://dl.google.com/go/go1.17.4.linux-amd64.tar.gz
sudo tar -xvf go1.17.4.linux-amd64.tar.gz
sudo mv go /usr/local
export PATH=$PATH:/usr/local/go/bin
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc
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
sudo add-apt-repository -y ppa:ethereum/ethereum
sudo apt-get update
sudo apt-get install ethereum
sudo apt-get upgrade geth

````

5. Install QuorumMaker
````bash
git clone https://github.com/jpmorganchase/quorum.git
cd quorum
make all
````

6. Install Tessera
````bash
git clone https://github.com/jpmorganchase/tessera.git
cd tessera
./gradlew build
````


6. Install Nethermind
what is Nethermind?
> Nethermind is a client for the Ethereum network. It is written in C# and is compatible with the Ethereum mainnet, Ropsten, Goerli, and Rinkeby testnets. It is also compatible with the Ethereum 2.0 Beacon Chain. Nethermind is a full node, meaning it stores the entire Ethereum blockchain and processes transactions. It is also a mining node, meaning it can mine new blocks and validate transactions. Nethermind is a popular choice for developers who want to run their own Ethereum node, as it is easy to install and use.
````bash
sudo apt-get install -y software-properties-common
sudo add-apt-repository ppa:ethereum/ethereum
sudo apt-get update
sudo apt-get install -y nethermind
````


6. Monitoring Tools

> Install Grafana  
````bash
sudo apt-get install -y apt-transport-https gnupg2 
sudo apt-get install -y software-properties-common wget
wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -
echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
sudo apt-get update
sudo apt-get install grafana
````
 > Install Prometheus  

````bash 
sudo apt-get install -y prometheus


````
