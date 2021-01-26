# Installation

OS: Linux Mint 20.1 (Ulyssa)

First, run below commmands to install dependencies and add the docker repository

    sudo apt update
    sudo apt install apt-transport-https ca-certificates curl gnupg-agent software-properties-common
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"

Then run below commands to install docker engine and cli

    sudo apt update
    sudo apt install docker-ce docker-ce-cli containerd.io

To install docker-compose, run below commands

    sudo curl -L "https://github.com/docker/compose/releases/download/1.28.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
    sudo chmod +x /usr/local/bin/docker-compose

Finally, to test if both docker and docker-compose installations are ok, run below commands

    sudo docker -v
    sudo docker-compose -v
