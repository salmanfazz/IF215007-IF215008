# Template Proposal

## Permasalahan
- Terdapat kesulitan ketika ingin membuat sebuah strategi pada sebuah game 

## Rancangan Solusi
- Membuat sebuah aplikasi yang dapat mempermudah untuk pengaturan pembuatan strategi map untuk sebuah game
- Hanya guild leader yang dapat mengatur atau mengubah strategi map
- Setiap guild member dapat melihat strategi map yang telah dibuat oleh guild leader

## Use Case
- Guild leader dan guild member melakukan registrasi terlebih dahulu sebelum dapat menggunakan aplikasi
- Guild member hanya dapat bisa mengakses strategi map ketika telah terdaftar
- Guild leader dapat melihat jumlah guild member yang melihat strategi map

## Struktur Data

### Guild
Atribut|Tipe Data|Contoh
---|---|---
id_guild | integer | 1
guild_name | string | EVERGLADE

### User
Atribut|Tipe Data|Contoh
---|---|---
id_users | integer | 1
id_guild | integer | 1
nickname | string | SWTCOOL2.0
roles | enum('Leader','Member') | Leader
