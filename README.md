# Tarim-Otomasyonu

| Varlık        | Özellikler                                                                                       |
|---------------|--------------------------------------------------------------------------------------------------|
| Çiftlik       | Çiftlik_ID (INT, PK), Ad (NVARCHAR(50)), Konum (NVARCHAR(100))                                   |
| Silo          | Silo_ID (INT, PK), Kapasite (INT), Doluluk_Oranı (FLOAT), Çiftlik_ID (INT, FK)                   |
| Tarım Alanı   | Alan_ID (INT, PK), Ürün_Türü (NVARCHAR(50)), Ekim_Tarihi (DATE), Hasat_Tarihi (DATE), Çiftlik_ID (INT, FK) |
| Tarım Aracı   | Araç_ID (INT, PK), Tür (NVARCHAR(50)), Marka (NVARCHAR(50)), Model (NVARCHAR(50)), Bakım_Tarihi (DATE), Çiftlik_ID (INT, FK) |
| Ekim/Hasat    | İşlem_ID (INT, PK), Alan_ID (INT, FK), Tarih (DATE), İşlem_Türü (NVARCHAR(20))                   |
| Bakım         | Bakım_ID (INT, PK), Araç_ID (INT, FK), Tarih (DATE), Bakım_Türü (NVARCHAR(50))                   |
| Kullanıcı     | Kullanıcı_ID (INT, PK), İsim (NVARCHAR(50)), Soyisim (NVARCHAR(50)), Email (NVARCHAR(100)), Şifre (NVARCHAR(50)) |



| Varlık 1      | Varlık 2      | İlişki       |
|---------------|---------------|--------------|
| Çiftlik       | Silo          | Sahibi (1-N) |
| Çiftlik       | Tarım Alanı   | Sahibi (1-N) |
| Çiftlik       | Tarım Aracı   | Sahibi (1-N) |
| Tarım Alanı   | Ekim/Hasat    | İçerir (1-N) |
| Tarım Aracı   | Bakım         | Sahip (1-1) |
| Kullanıcı     | Çiftlik       | Sahibi (N-1) |
