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

| Kaynak Varlik      | Iliski   | Hedef Varlik      | Aciklama             |
|---------------------|----------|-------------------|----------------------|
| Ciftlik            | 1-1      | CiftlikHesap      | Yonetir.            |
| Ciftlik            | 1-n      | TarimsalArazi     | Bulundurur.         |
| Ciftlik            | 1-n      | Silo              | Sahiptir.         |
| Ciftlik            | 1-n      | TarimAraci        | Kullanir.            |
| TarimsalArazi      | 1-n      | EkimHasat         | Islemi Gecirir.     |
| TarimAraci         | 1-n      | Bakim             | Gerektirir.         |
| Ciftlik            | 1-n      | CiftlikCalisani   | Bulundurur.         |
| CiftlikCalisani    | n-m      | CalisanArazi      | Gorev Alir.         |


Projenin E-R Diyagramları Aşağıda Verilmiştir.

![WhatsApp Görsel 2025-01-05 saat 13 01 37_7665df15](https://github.com/user-attachments/assets/82780838-f817-484b-a010-d879b80f4d8e)



![E-R Diyagramı](https://github.com/user-attachments/assets/c9b662f0-b66c-45fe-a826-02237e5f1564)


Proje Raporu
-------------
[rapor.pdf](https://github.com/user-attachments/files/18311292/rapor.pdf)





