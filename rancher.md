# rancher
Rancher Administrando kubernetes HA - fodão

## Alguns comandos

# docker commands

docker run --name -nginx -d -p 80:80 mau-nginx
docker run --name some-nginx -d -p 8080:80 some-content-nginx
docker run -d --name mau-nginx -p 80:80 nginx
docker rm -f $(docker ps -a -q)
docker volume rm $(docker volume ls)



# Setting up Unbreakable Enterprise Kernel
sudo yum-config-manager --disable ol7_UEKR3 ol7_UEKR4
sudo yum-config-manager --enable ol7_UEKR5

sudo yum update
sudo systemctl reboot

yum-config-manager --enable ol7_addons

# 2.3 Removing the docker Package
sudo rpm -qi docker
sudo systemctl stop docker
sudo yum remove docker


sudo yum install docker-engine docker-cli
sudo systemctl enable --now docker
sudo systemctl status docker
sudo docker info

systemctl daemon-reload
systemctl restart docker

# 7. Add User to Docker group
# rodando o docker sem sudo
sudo groupadd docker
sudo usermod -aG docker opc
newgrp docker

#Versão do linux
sudo yum install redhat-lsb-core 
lsb_release -d 
cat /etc/os-release

# OCI Teste DNS com NGINX



