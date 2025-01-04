# Tarim-Otomasyonu
•Can ÇIKRIKÇI-220260003

•Uğur ÇETİNKAYA-220260013

•Taha M. GÖBEK-220260035

Tarım Otomasyon Sistemi, tarımsal faaliyetlerin ve kaynakların etkin bir şekilde yönetilmesi için geliştirilmiştir. Bu sistem, çiftlik bilgileri, silo kapasiteleri, tarım alanları, tarım araçları, ekim ve hasat süreçleri, bakım işlemleri ve kullanıcı verileri gibi ana varlıklardan oluşur.

## Varlık-Özellik Tablosu

| Varlık            | Özellikler                                                        |
|--------------------|-------------------------------------------------------------------|
| Çiftlik           | ÇiftlikID, Ad, Konum                                             |
| Silo              | SiloID, ÇiftlikID, Kapasite, DolulukOranı                        |
| TarımsalArazi     | AraziID, ÇiftlikID, EkimDurumu, HasatDurumu                      |
| TarımAracı        | AracID, ÇiftlikID, AracTürü, BakımDurumu                         |
| EkimHasat         | İşlemID, AraziID, İşlemTürü, Tarih                               |
| Bakım             | BakımID, AracID, BakımTürü, Tarih                                |
| ÇiftlikÇalışanı   | ÇalışanID, ÇiftlikID, Ad, Soyad, Pozisyon                        |
| ÇalışanArazi      | ÇalışanID, AraziID, GörevTarihi                                  |
| ÇiftlikHesap      | HesapID, ÇiftlikID, İşlemTürü, Miktar, Bakiye, Tarih             |


## Varlık-İlişki Tablosu

| Kaynak Varlık      | İlişki   | Hedef Varlık      | Açıklama                                                                      |
|---------------------|----------|-------------------|-------------------------------------------------------------------------------|
| Çiftlik            | 1-1      | ÇiftlikHesap      | Yönetir.                                   |
| Çiftlik            | 1-n      | TarımsalArazi     | Bulundurur.                     |
| Çiftlik            | 1-n      | Silo              | Sahip olur.                              |
| Çiftlik            | 1-n      | TarımAracı        | Kullanır.                      |
| TarımsalArazi      | 1-n      | EkimHasat         | İşlemi Geçirir.                |
| TarımAracı         | 1-n      | Bakım             | Gerektirir.                         |
| Çiftlik            | 1-n      | ÇiftlikÇalışanı   | Bulundurur.                          |
| ÇiftlikÇalışanı    | n-m      | ÇalışanArazi      | Görev Alır. |


Projenin E-R Diyagramı Aşağıda Verilmiştir.

![veritabaniDiyagrami](https://github.com/user-attachments/assets/ff6b6bae-0a47-48c2-82fb-ddcdc00d14e0)
