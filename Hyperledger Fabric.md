# Blockchain
*This is my repository regarding the Blockchain which contain Hyperledger Fabric deploy.*




# Hyperledger-Fabric

To initiate the first Hyperledger Fabric network, we will utilize the Fabric-samples repository. This repository consists of CLI tool binaries and Fabric Docker Images, which are essential for comprehending and utilizing the fundamentals of Fabric. Before commencing the project, it is necessary to install the following dependencies:

## 1.Install Docker
For this Some of the codes from **Shubham Tatvamasi** are used to install the docker.


### Quick Install
```bash
curl -sL https://github.com/ShubhamTatvamasi/docker-install/raw/master/docker-install.sh | bash
```
---

Install packages:
```bash
sudo apt update
sudo apt install -y \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release \
    jq
```

Add Docker’s official GPG key:
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

Setup repository:
```bash
echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

Install Docker Engine:
```bash
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io
```

Add your user to the docker group:
```bash
sudo usermod -aG docker $USER
```

### Docker Compose

Download the current stable release of Docker Compose:
```bash
COMPOSE_VERSION=$(curl -s "https://api.github.com/repos/docker/compose/tags" | jq -r '.[0].name')
sudo curl -L "https://github.com/docker/compose/releases/download/${COMPOSE_VERSION}/docker-compose-$(uname -s)-$(uname -m)" \
  -o /usr/local/bin/docker-compose
```

Apply executable permissions to the binary:
```bash
sudo chmod +x /usr/local/bin/docker-compose
```


    sudo apt-get -y install docker-compose

## 2. Install Golang-go

    sudo apt install golang-go

## 3. Install jq
(jq is like sed for JSON data )

    sudo apt install jq

## 4. Install Node/java

    sudo apt install npm
    npm install node

## 5. Installing Fabric-samples Repository

    curl -sSLO https://raw.githubusercontent.com/hyperledger/fabric/main/scripts/install-fabric.sh && chmod +x install-fabric.sh

Then you can pull docker containers by running one of these commands:
   
    ./install-fabric.sh docker samples
    ./install-fabric.sh d s


To install binaries for Fabric samples you can use the command below:
   
    ./install-fabric.sh binary

## Building First Network
1. Navigate through the Fabric-samples folder and then through the Test network folder where you can find script files using these we can run our network.
 
       cd fabric-samples/test-network
 


2. we can bring up a network using the following command. This command creates a fabric network that consists of two peer nodes and one ordering node

        ./network.sh up

***Now our first Hyperledger Fabric Network is successfully running.***

**HYPERLEDGER DONE!!**

