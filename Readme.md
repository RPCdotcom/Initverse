![image](https://github.com/user-attachments/assets/35e841fa-a227-432a-bb05-0005e63d796a)

# Initchain Node Kurulum : 

## Gereksinimler : 

Minimum : 

- ∞ CPU+ / ∞ GB RAM /  ∞ MBit/sec İndirme Hızı

Tavsiye Edilen : 

- ∞+ CPU ( Hızlı ) / ∞+ GB RAM / ∞+ MBit/sec İndirme Hızı 

### Sonsuz yazmamızın sebebi sunucunuz / bilgisayarınız ile alakalı - Liste : https://github.com/RPCdotcom/Initverse/blob/main/Threadlistesi.md

## Kuruluma Başlayalım ; 

Sistem paketlerini güncellemek ve yükseltmek için aşağıdaki komutu çalıştırın:

```bash
sudo apt update -y && sudo apt upgrade -y
```
## 2. Gerekli paketleri kurun:

```bash
sudo apt install htop ca-certificates zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev tmux iptables curl nvme-cli git wget make jq libleveldb-dev build-essential pkg-config ncdu tar clang bsdmainutils lsb-release libssl-dev libreadline-dev libffi-dev jq gcc screen unzip lz4 -y
```
## 3. Gerekli Dosyayı indirelim kurun:

```bash
curl -L -O https://github.com/Project-InitVerse/miner/releases/download/v1.0.0/iniminer-linux-x64
```

#### Yetki Verelim : 

```bash
chmod +x iniminer-linux-x64
```

## 4. Screen Açalım : 

```bash
screen -S init
```

## 5. Ayarlama Yapalım - UYARI Çekirdekleri ayarlananı yapmanızı tavsiye ederiz. 
#### Durdurmak istediğinizde CTRL C yapmanız yeterli durdurur. 

- 0x0304f5193FCe6A27e3789c27EE2B9D95177e21A5 bu random cüzdan bunun yerine siz kendi cüzdan adresinizi yazın
- Worker001 sunucuya verdiğiniz isim isterseniz farklı yapabilirsiniz Sunucum1 misal olarak.

##### Tüm Çekirdeklere Yüklenen Model : 

```bash
./iniminer-linux-x64 --pool stratum+tcp://0x0304f5193FCe6A27e3789c27EE2B9D95177e21A5.Worker001@pool-a.yatespool.com:31588 
```
![image](https://github.com/user-attachments/assets/c1dd2098-a6a5-49a7-90cb-9ce42b7b8307)


##### Dilerseniz Çekirdeklere Yüklenmesini Ayarlayabilirsiniz Misal Alttaki komut 1 Thread Kullanmak için  --cpu-devices :

```bash
./iniminer-linux-x64 --pool stratum+tcp://0x0304f5193FCe6A27e3789c27EE2B9D95177e21A5.Worker001@pool-a.yatespool.com:31588 --cpu-devices 1
```

#### Multi CPU Ayarlamak İçin --cpu-devices ekleyebilirsiniz misal  4 Thread için - kısaca her çekirdek için yazıp sayıyı arttırıyoruz : 

```bash
./iniminer-linux-x64 --pool stratum+tcp://0x0304f5193FCe6A27e3789c27EE2B9D95177e21A5.Worker001@pool-a.yatespool.com:31588 --cpu-devices 1 --cpu-devices 2 --cpu-devices 3 --cpu-devices 4 
```

![image](https://github.com/user-attachments/assets/c5b535eb-47c8-4cc7-9167-9851438b18f4)

Misal 9'luda Böyle Kullanıyor : 

![image](https://github.com/user-attachments/assets/6ace2e49-9970-4f5d-b620-8d610ac13637)


#### Çalıştığında misal böyle gözükecek: 

![image](https://github.com/user-attachments/assets/bbbcd5ca-7660-4704-92e1-633d2c90b65f)

#### CTRL A + D ile screenden çalışmayı durdurmadna rahatlıkla çıkabilirsiniz.

## Ne Kadar Kastık Durumlar Ne Dasboard'ı : 

- Link : https://genesis-testnet.yatespool.com/ 

- Cüzdan adresinizi yazıp search butonuna basın - biraz geç yükleniyor.
