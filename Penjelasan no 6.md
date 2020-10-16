#### Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).
------

***Mencari file zip***

```
frame contains "Answer.zip"
```

![6](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/6.png)

```
Klik kanan -> Follow -> TCP Stream -> Save data as Raw -> Ubah stream menjadi 12
```

![6a](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/6a.png)

*File akan tersimpan sebagai **zip***

![6b](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/6b.png)

*Saat file dibuka terdapat **Open This.pdf** yang jika dibuka kembali meminta masukan **password***
![6c](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/6c.png)

------

***Mencari password***

```
frame contains "zipkey.txt"
```

![6d](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/6d.png)

```
Klik kanan -> Follow -> TCP Stream -> Save data as **ASCII** -> Ubah stream menjadi **23**
```

![6e](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/6e.png)

*File txt akan tersimpan dan berisi **password** yang dibutuhkan*

![6f](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/6f.png)

*Masukkan password, dan **Open This.pdf** akan menampilkan seperti dibawah ini*
![6g](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/6g.png)
