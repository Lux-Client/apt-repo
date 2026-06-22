sudo install -d -m 0755 /etc/apt/keyrings

curl -fsSL https://apt.lux.pluginhub.de/lux-archive-keyring.asc | sudo tee /etc/apt/keyrings/lux.asc > /dev/null

echo "deb [signed-by=/etc/apt/keyrings/lux.asc] https://apt.lux.pluginhub.de ./" | sudo tee /etc/apt/sources.list.d/lux.list

sudo apt update

sudo apt install lux
