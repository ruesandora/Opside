<h1 align="center"> V2 içindir </h1>

### Mevcut sunucumuzda ki node'u durduralım
```console
cd
cd testnet-auto-install-v2
opside-chain/stop-all.sh
```

### Daha sonra yeni sunucumuza opside'ı yüklüyoruz:
```console
# Güncellemeler
sudo apt-get update -y && sudo apt-get upgrade -y

sudo apt install -y build-essential libssl-dev cmake screen git htop

# Opside'ı yükleyelim
wget -c https://pre-alpha-download.opside.network/testnet-auto-install-v2.tar.gz 
tar -C ./ -xzf testnet-auto-install-v2.tar.gz
chmod +x -R ./testnet-auto-install-v2
cd ./testnet-auto-install-v2
```

### Node'u başlatalım

```
./install-ubuntu-en-1.0.sh
# Bu komutu girdikten sonra sırasıyla:
```

> HALİ HAZIRDA ÇALIŞAN NODE'UNUZUN AYNI BİLGİLERİNİ GİRİYORUZ

> SONDAKİ 24 KELİME AŞAMASI FARKLIDIR O AŞAMAYI GEÇİN, MEVCUT KEYİMİZ İLE DEĞİŞTİRECEĞİZ.

> Cüzdan adresi

> Şifre

> Tekrar Cüzdan adresi

> Tekrar şifre

### Yukarıda ki kurulum tamamlandıysa yeni sunucumuzda ki node'u durduralım

```console
cd
cd testnet-auto-install-v2
opside-chain/stop-all.sh
```


### Mevcut Sunucumuzdan `validator_keys` klasörünü yedekleyelim.

```console
/root/testnet-auto-install-v2/
```

### Şimdi yeni sunucuzda aynı dizinde `validator_keys` kısmını silip, az önce yedeklediğimiz Mevcut Sunucunuda ki klasörü taşıyalım.

### Aynı işlemi aşağıda ki dizin içinde `keystore-m` içinde yapalım:

> Mevcutta yedekle, yenisinde sil, mevcutta ki dosyayı yenisine taşı.

```console
/root/testnet-auto-install-v2/opside-chain/prysm/validator/config/wallet/
```

> Anlamayanlar için, yeni bir cüzdan satın aldınız diyelim;

> Eski cüzdanında ki eşyaları masaya koy, yeni cüzdanında ki gösterge kartlarını kaldır, eski cüzdanında ki eşyaları yeni cüzdanına koy, şeffaf kısımda ruesin resmi olsun.

### `validator_keys` ve `keystore-m` yeni sunucumuza eskisinden taşıyıp yedeklediysek yeni sunuucmuzda ki node'u çalıştıralım:

```console
cd
testnet-auto-install-v2/opside-chain/start-geth.sh
testnet-auto-install-v2/opside-chain/start-beaconChain.sh
testnet-auto-install-v2/opside-chain/start-validator.sh
```

### Explorer'dan çalıştığına, yani `effectiveness`'in yüksek olduğunu teyit etmeden eski sunucunuzu kapatmanızı tavsiye etmem. Emin olun!
