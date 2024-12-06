# Vana üzerinde çalışan Valora için node kuracağız.

## Ön gereksinimler

Cüzdanınızı Fonlayın

Vana Faucet [Bağlantısı](https://faucet.vana.org/moksha)

Sunucuya bir çok node kuracağımdan dolayı 16gb olarak seçtim. ![image](https://github.com/user-attachments/assets/ac8a226a-4d29-4189-a669-c58da7a208ab)


# Adımlar / kodlar sırasıyla tek tek girin.


sudo apt update && sudo apt upgrade -y

sudo apt install -y apt-transport-https ca-certificates curl software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io

[ -f "volara.sh" ] && rm volara.sh; curl -s -o volara.sh https://raw.githubusercontent.com/volaradlp/minercli/refs/heads/main/run_docker.sh && chmod +x volara.sh && ./volara.sh

` 
export VANA_PRIVATE_KEY=0xxxxx

docker pull volara/miner

docker run -it -e VANA_PRIVATE_KEY=${VANA_PRIVATE_KEY} volara/miner


`

