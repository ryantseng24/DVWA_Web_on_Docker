# DVWA_Web_on_Docker

install ubuntu Server

follow the below steps
----------------------------------------------------------------------------------------------------------
sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates curl gnupg-agent software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo apt-key fingerprint 0EBFCD88

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io

sudo systemctl restart docker && sudo systemctl enable docker


sudo docker run -dit --restart=always  --name dvwa   --publish 80:80   docker.io/vulnerables/web-dvwa
-----------------------------------------------------------------------------------------------------------
you can access http://server_ip


