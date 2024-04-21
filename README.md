> Ben uzun süre kapatmayacağım bir sunucuya kurdum çünkü yaklaşık 1-1.5 ay açık kalmalı tahminim.

> Ne kadar erken kurulursa katkıda bulunma sırasının gelmesi de o kadar iyidir. (daha erken yine ameliyatta oldgum ıcın paylasamadım)

> Ben katkıda bulunan herkesin github rewardsı alacağını düşünüyorum bir kesinlik yok.

> Donanım olarak herhangi bir sunucu yeterli - taşıma için aynı github ile başka sunucuda kursanız olur. 


```console
# sunucu güncelleme
sudo apt update
sudo apt upgrade -y


# nvmi yükleyelim
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.0/install.sh | bash
source ~/.bashrc

# geçici dizin oluşturup içine giriyoruz
mkdir ~/p0tion-tmp
cd ~/p0tion-tmp

#  nvm v16.20 kurmak
nvm install 16.20
nvm use 16.20


# phase2cli yüklüyoruz
npm i @p0tion/phase2cli
```

#

### GitHub ile kimlik doğrulaması yapmak bu kısım önemli

// aşağıdaki linki açın

https://github.com/login/device 

// Aşağıdaki kodu node içinde çalıştırın

`npx phase2cli auth

// ve 8 dijit şifreyi açılan linke giriniz - github'ınızı bağlayınız.


//"Congratulations, you're all set!" olarak şifreyi doğru girerseniz github sayfanızda mesaj göreceksiniz

#


### Katkıda bulunma kısmına geçelim:

// Bu kısımda önce enter tuşuna basın ardından randomly/otomatik seçip enter yapın. 

```
screen -S risczero
npx phase2cli contribute
```

// Screen içinde çalıştırın eğer komut durmuş ise aşağıdaki komudu tekrar çalıştırın.

//Herhangi bir hatayla karşılaşırsanız veya bağlantınız kesilirse, `npx phase2cli contribute` komutunu yeniden çalıştırarak katkılarınızı yeniden başlatmayı deneyebilirsiniz. 

// Katkınız en son kaldığı yerden devam etmelidir.

#

### Doğru çalışan node:

![image](https://github.com/ruesandora/risc-zero/assets/101149671/cb1671ad-72c5-4f82-97bf-87aa1d30b8a5)



### Kodları silme ve kaldırma

```
npx phase2cli clean
npx phase2cli logout
rm -rf ~/p0tion-tmp
```

