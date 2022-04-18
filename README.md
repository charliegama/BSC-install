# BSC-install
Como instalar un NODO BSC
# Requerimientos minimos servidor BNB 

- 32Cores 
- 64Gb RAM
- 240GB SSD primary disk
- 4TB SSD or NVME Disk

<br>

# Install Geth Binance - 

sudo mkdir /data/bsc<br>
sudo chown ubuntu:ubuntu /data/bsc<br>
cd /data/bsc<br>
wget https://github.com/binance-chain/bsc/releases/download/v1.1.2/geth_linux<br>
wget https://github.com/binance-chain/bsc/releases/download/v1.1.2/mainnet.zip<br>
unzip mainnet.zip<br>
mv geth_linux geth<br>
chmod +x geth<br>
./geth --datadir node init genesis.json<br>

<br>

# Install Botstrap BNB <br>
screen -S bnb wget -O - "https://tf-dex-prod-public-snapshot-site3.s3-accelerate.amazonaws.com/geth-20220403.tar.lz4?AWSAccessKeyId=AKIAYINE6SBQPUZDDRRO&Signature=U2y2CtRjbkdX4b9%2BmTYRFNd0U3I%3D&Expires=1651655213"  | lz4 -d - | tar -xv<br>
<br>

# Creando seguridad para evitar ataques no necesarios. <br>

<br>
sudo ufw default deny incoming<br>
sudo ufw default allow outgoing<br>
sudo ufw allow 30303<br>
sudo ufw allow 22<br>
sudo ufw allow from "your ip server" to any port 8545<br>
sudo ufw allow from "your server read" to any port 8545<br>
sudo ufw enable<br>

<br><br>
Si requieres ayuda escribenos, 
<br> email administrador@vps593.com 
