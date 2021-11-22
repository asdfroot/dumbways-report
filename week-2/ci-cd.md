# Github action

## Step 1 - Create Workflows

- push App project pada revository baru

![gambar a1](assets/a1.PNG)

- setelah project dipush masuk ke menu Github action

![gambar a2](assets/a2.PNG)

**Action** >> **Set up this workflow** pada **Node.js**

![gambar a3](assets/a3.PNG)

**Start commit** >> **Commit new file**

![gambar a4](assets/a4.PNG)

## Step 2 – Check Running CI

- masuk Github Actions disitu akan terlihat workflow yang kita buat

- jika workflow yang kita buat berhasil maka akan ada tanda checklist warna hijau dengan begitu tandanya kita berhasil melakukan Continouse integrations menggunakan GitHub.

![gambar a5](assets/a5.PNG)

## Step 3 – Menguji Workflows

- buka code di handlersnya dan coba menyalahkan codinganya agar mendapat error

![gambar a6](assets/a6.PNG)

- misal merubah salah satu symbol **+** menjadi **-**

- save

- lalu commit dan push pada revository

 ![gambar a7](assets/a7.PNG)

 - check Github actionsya running jobs otomatis setelah dipush repository

![gambar a8](assets/a8.PNG)

 - Hasilnya pasti akan error

![gambar a9](assets/a9.PNG)

 - error tersebut adalah tanda bahwa code yang kita buat harus di check lagi sebelum di push , selain itu notif error akan terkirim ke email account github kita sebagai penanda bahwa kita harus melakukan fixing bug.

 - Fixing Bug

 ![gambar a10](assets/a10.PNG)
