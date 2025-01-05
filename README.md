# Tarim-Otomasyonu
•Can ÇIKRIKÇI-220260003

•Uğur ÇETİNKAYA-220260013

•Taha M. GÖBEK-220260035

Tarım Otomasyon Sistemi, tarımsal faaliyetlerin ve kaynakların etkin bir şekilde yönetilmesi için geliştirilmiştir. Bu sistem, çiftlik bilgileri, silo kapasiteleri, tarım alanları, tarım araçları, ekim ve hasat süreçleri, bakım işlemleri ve kullanıcı verileri gibi ana varlıklardan oluşur.

## Varlık-Özellik Tablosu

| VARLIK            | OZELLIKLER                                        |
|--------------------|--------------------------------------------------|
| Ciftlik           | CiftlikID, Ad, Konum                             |
| Silo              | SiloID, CiftlikID, Kapasite, DolulukOrani, MevcutDoluluk |
| TarimsalArazi     | AraziID, CiftlikID, EkimDurumu, HasatDurumu      |
| TarimAraci        | AracID, CiftlikID, AracTuru, BakimDurumu         |
| CiftlikCalisani   | CalisanID, CiftlikID, Ad, Soyad, Pozisyon        |
| CiftlikHesap      | HesapID, CiftlikID, IslemTuru, Miktar, Bakiye, Tarih |
| EkimHasat         | IslemID, AraziID, IslemTuru, Tarih               |
| CalisanArazi      | CalisanID, AraziID, GorevTarihi                  |
| Bakim             | BakimID, AracID, BakimTuru, Tarih                |


## Varlık-İlişki Tablosu

| Kaynak Varlık      | İlişki   | Hedef Varlık      | Açıklama                                                                      |
|---------------------|----------|-------------------|-------------------------------------------------------------------------------|
| Çiftlik            | 1-1      | ÇiftlikHesap      | Yönetir.                                   |
| Çiftlik            | 1-n      | TarımsalArazi     | Bulundurur.                     |
| Çiftlik            | 1-n      | Silo              | Sahip olur.                              |
| Çiftlik            | 1-n      | TarımAracı        | Kullanır.                      |
| TarımsalArazi      | 1-n      | EkimHasat         | İşlemi Geçirir.                |
| TarımAracı         | 1-n      | Bakım             | Gerektirir.                         |
| Çiftlik            | 1-n      | ÇiftlikÇalışani   | Bulundurur.                          |
| ÇiftlikÇalışani    | n-m      | ÇalışanArazi      | Görev Alır. |


Projenin E-R Diyagramı Aşağıda Verilmiştir.

![veritabaniDiyagrami](https://github.com/user-attachments/assets/ff6b6bae-0a47-48c2-82fb-ddcdc00d14e0)
