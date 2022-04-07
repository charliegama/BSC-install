# BSC-install
Como instalar un NODO BSC
Requerimientos minimos servidor BNB 

- 32Cores 
- 64Gb RAM
- 240GB SSD primary disk
- 4TB SSD or NVME Disk




Install Geth Binance - 

sudo mkdir /data/bsc
sudo chown ubuntu:ubuntu /data/bsc
cd /data/bsc
wget https://github.com/binance-chain/bsc/releases/download/v1.1.2/geth_linux
wget https://github.com/binance-chain/bsc/releases/download/v1.1.2/mainnet.zip
unzip mainnet.zip
mv geth_linux geth
chmod +x geth
./geth --datadir node init genesis.json



Install Botstrap BNB 
screen -S bnb wget -O - "https://tf-dex-prod-public-snapshot-site3.s3-accelerate.amazonaws.com/geth-20220403.tar.lz4?AWSAccessKeyId=AKIAYINE6SBQPUZDDRRO&Signature=U2y2CtRjbkdX4b9%2BmTYRFNd0U3I%3D&Expires=1651655213"  | lz4 -d - | tar -xv


Creando seguridad para evitar ataques no necesarios. 


sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow 30303
sudo ufw allow 262
sudo ufw allow from 204.12.216.18 to any port 8545
sudo ufw allow from 107.150.58.50 to any port 8545
sudo ufw enable


Si requieres ayuda escribenos, administrador@vps593.com 
