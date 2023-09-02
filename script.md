### Ara ara durduğu ve zırt pırt kontrol etmekten sıkıldığım için opside hakkında bir script
### Script 3 satte bir node'u fixliyor tekrar çalışması için.

### Tahminimce 4-5 saatte bir durduğu için 3 saat yaptım, sleep ile kendiniz karar verebilirsiniz:

```console
# screen açalım
apt install screen
screen -S script
```

> İçine girelim dosyanın: `nano rues_script.sh`

```console
# Altta ki kodu içine yapıştırıp ctrl x y ile çıkalım.


#!/bin/bash

# Run the script
cd testnet-auto-install-v2/opside-chain/
./stop-all.sh

# Run the necessary commands
cd
cd testnet-auto-install-v2/opside-chain/
./start-geth.sh &
./start-beaconChain.sh &
./start-validator.sh &

# View running processes and stop them if you want
echo "Çalışan işlemleri görüntülemek ve durdurmak için 'q' tuşuna basın."
top
```

### başlatalım:
```console
chmod +x rues_script.sh
./rues_script.sh
```

> Yinede script çalışıyor mu ara ara kontrol edersiniz bazen durabilir. Ama eskisi kadar uğraşmazsınız artık.

