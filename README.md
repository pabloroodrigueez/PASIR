# PASIR
En este repositorio podras encontrar dos carpetas que en las cuales hay un servidor web Apache con una pagina diferente en cada uno para hacer una demostracion con un balanceador de cargas.

sudo passwd root
su -
apt update

https://voidnull.es/instalacion-de-docker-en-debian-12/

apt install software-properties-common apt-transport-https ca-certificates curl gnupg lsb-release

mkdir -p /etc/apt/keyrings

curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

apt update

apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin

systemctl status docker
systemctl enable docker

git clone https://github.com/pabloroodrigueez/PASIR

docker-compose build
docker-compose up

