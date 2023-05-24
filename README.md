<h1 align="center"> Opside </h1>

> Hatılrasınız Opside [form](https://t.me/RuesAnnouncement/2073) doldurmuştuk ve dün seçilenler olarak ile validatör kurmaya başlayabiliriz. 

> Sorularınız için: [Chat](https://t.me/RuesChat) - Faucetten token aldığınıza emin olun.

<h1 align="center"> Donanım </h1>

> Ben buraa [Hetzner](https://github.com/ruesandora/Hetzner/blob/main/README.md) kullandım lakin disk oldukça düşük ve az kaldı, contabo en düşük paket 400 GB diske çıkarılmış versionu tercih edebilirsiniz.

```sh
# Ekibin önerisi:
4 CPU 16 RAM 500 GB SSD

# Benim önerim:

4 CPU 8 RAM 400 GB SSD
```

<h1 align="center"> Kurulum </h1>

```sh
# Güncellemeler
sudo apt-get update -y && sudo apt-get upgrade -y

sudo apt install -y build-essential libssl-dev cmake screen git htop

# Opside'ı yükleyelim
wget -c https://pre-alpha-download.opside.network/testnet-auto-install-v2.tar.gz 
tar -C ./ -xzf testnet-auto-install-v2.tar.gz
chmod +x -R ./testnet-auto-install-v2
cd ./testnet-auto-install-v2

# Genesisi yükleyelim:
wget -c https://pre-alpha-download.opside.network/testnet-auto-install.tar.gz 
tar -C ./ -xzf testnet-auto-install.tar.gz
chmod +x -R ./testnet-auto-install
cd ./testnet-auto-install
```

<h1 align="center"> Node'u başlatalım </h1>

```
./install-ubuntu-en-1.0.sh
# Bu komutu girdikten sonra sırasıyla:
```

> Cüzdan adresi

> Şifre

> Tekrar Cüzdan adresi

> Tekrar şifre

> Vereceği 12 kelimeyi alın, daha sonra sadece ilk 4 hafrlerini girin.

<h1 align="center"> Validatör oluşturma </h1>

> Node'umuz sync olduktan sonra [buraya](https://opside.network/validator/deposit) gidelim.

> Upload deposit data'ya kadar okey diyin.

> Daha sonra WinSCP ile `/root/testnet-auto-install-v2/validator_keys/deposit_data` klasörünü masa üstüne atın.

> Upload edin.

> Tüm tikleri işaretledikten sonra 25000 IDE'yı stake edin.

> Kontrol: [eplorer](https://pre-alpha-beacon.opside.info/)


<h1 align="center"> Yardımcı komutlar </h1>

```sh
# execution client logları
opside-chain/show-geth-log.sh

# consensus client logları
opside-chain/show-beaconChain-log.sh

# validatör logları
opside-chain/show-validator-log.sh
```
<h1 align="center"> Explorer </h1>

[Link](https://pre-alpha.opside.info/)
