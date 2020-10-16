# Jarkom_Modul1_Lapres_E03

## Display Filter

#### 2. Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!

```
File -> Export Object -> HTTP
```

*Masukkan nama file yang dicari, lalu **Save***
![2](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/2.png)
![2a](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/2a.png)

----

#### 4. Temukan paket dari web-web yang menggunakan basic authentication method!

```
http.authbasic
```

![4](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/4.png)

----

#### 6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).

Penjelasan no 6 [klik disini](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Penjelasan%20no%206.md)

----

#### 10. Cari file .pdf di wireshark lalu download dan buka file tersebut!

Penjelasan no 10 [klik disini](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Penjelasan%20no%2010.md)

----

## Capture Filter

#### 12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!

```
tcp.srcport==80
```

![12](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/12.png)

----

#### 13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

```
tcp.dstport==443
```

![13](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/13.png)

----

#### 14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

*Mencari **ip** pc dahulu melalui terminal*

![14](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/14.png)

*Capture di Wireshark*

```
ip.scr==192.168.43.254
```


![14a](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/14a.png)
