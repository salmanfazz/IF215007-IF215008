
## Git Project Init
### Langkah 1
Buatlah sebuah repository baru pada github yang digunakan
![image](https://user-images.githubusercontent.com/49604034/210849158-45b53fea-f144-4a81-ba54-8940a6c39c91.png)
### Langkah 2
Setelah membuat repository baru maka akan tampilan seperti ini
![image](https://user-images.githubusercontent.com/49604034/210849257-82d63b64-c759-49f3-b743-55fb5e382313.png)
### Langkah 3
Terdapat beberapa cara untuk memasukan project kedalam git, disini saya akan mencontohkan salah satu caranya yaitu dengan membuka terminal / cmd pada folder project yang akan kita gunakan kemudian jalankan 
```
git init .
```
### Langkah 4
Lalu jalankan perintah dibawah untuk menambahkan seluruh file yang ada pada folder project tersebut
```
git add .
```
### Langkah 5
Lalu jalankan perintah dibawah untuk melakukan commit serta menambahkan message / comment
```
git commit -m "first commit"
```
### Langkah 6
Lalu jalankan perintah
```
git branch -M main
```
### Langkah 7
Lalu jalankan perintah dibawah untuk mendeklarasikan repository mana yang akan kita gunakan nanti, link yang digunakan adalah link repository yang kita buat sebelumnya dibuat
```
git remote add origin link
```
### Langkah 8
Kemudian jalankan perintah untuk melakukan push ke repository yang digunakan
```
git push -u origin main
```

Maka apabila telah berhasil melakukan push, kita hanya perlu melakukan refresh pada halaman repository sebelumnya dan file yang ada pada folder project yang kita tambahkan akan secara otomatis ditambahkan kedalam repository github
![image](https://user-images.githubusercontent.com/49604034/210851278-ed2eb333-8e81-4873-855b-c6e92085d4df.png)
