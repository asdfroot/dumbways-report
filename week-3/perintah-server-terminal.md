# Manage Server with Terminal

## Texs Editor

  Nano merupakan sebuah aplikasi editor berbasis teks untuk Unix dan sistem Unix-like. :

-   nano

    `nano nanotes.txt` membuka file nanotes.txt dengan teks editor nano

    ![gambar 1](assets/nanotxt.png)

    `nano /directory/directory1/nanotes.txt` membuka file nanotes.txt yang lokasinya berada dalam folder

    ![gambar 2](assets/nano2.png)

-   Shortcut pada text editor nano

    `CTRL + X` untuk keluar dari editor. setelah keluar akan dimintai perubahan, perubahan akan disimpan atau tidak. jika `Y` untuk **Yes** dan `N` untuk **No**.

    `CTRL + O` untuk menyimpan tanpa menutup nanu. lalu **Enter**

    `CTRL + W` untuk mencari teks, kemudian masukan pada kolom pencarian lalu **Enter**

    `ALT + A` untuk melihat teks. arahkan cursor pada teks yang diinginkan.

    `ALT + 6` digunakan untuk _copy_ teks yang sudah di _select_

    `CTRL + K` digunakan untuk _cut_ teks yang sudah di _select_

    `CTRL + U` digunakan untuk _paste_ teks yang sudah di _copy_

    `CTRL + A` untuk pindah cursor ke baris paling awal

    `CTRL + E` untuk pindah cursor ke baris paling akhir

    ![gambar 3](assets/nano1.png)

## Text Manipulation

    Text Manipulation menggunakan terminal tanpa nano, berikut perintah yang dapat digunakan :

-   cat

    `cat file.md` digunakan untuk melihat isi file

    `cat > file1.md` untuk membuat file baru dan memasukan teks

    `cat file1.md file2.md > file3.md` untuk menggabungkan dua file dan menyimpannya pada file3.md

    ![gambar 4](assets/cat.png)

-   sed

    `sed -i 's/dalam/jero/g' file3.md`

    > keterangan : akan mengganti semua kata "dalam" menjadi "jero" pada file3.md

    ![gambar 5](assets/sed.png)

-   grep

    `grep file file3.md` akan mencari kata "file" pada file3.md

    ![gambar 6](assets/grepfile.png)

    `grep -c jero file3.md` akan menghitung jumlah kata "jero" pada file3.md

    ![gambar 7](assets/grep-c.png)

    `grep isi *` akan mencari semua kata yang berisi kata "isi"

    ![gambar 8](assets/grepisi.png)

-   sort

    `sort file3.md` mengurutkan berdasarkan ascending

    ![gambar 9](assets/sort.png)

    `sort -r file3.md` mengurutkan berdasarkan descending

    ![gambar 10](assets/sort-r.png)

-   echo

    `echo "Hello Google"` mencetak kata **hey kamu**

    ![gambar 11](assets/echohello.png)

    `echo "ini data di file3" >> file3.md` menambahkan **ini data di file3** pada file3.md

    ![gambar 12](assets/echoisi.png)

    `echo "isi file terganti semua" > file3.md` mengganti semua isi file3 menjadi **isi file terganti semua**

    ![gambar 13](assets/echoganti.png)

-   less

    `less /proc/cpuinfo` menampilkan isi file atau output "cpuinfo" dalam satu halaman sekaligus

    ![gambar 14](assets/less.png)

-   head

    `head /proc/cpuinfo` akan menampilkan 10 baris pertama

    ![gambar 15](assets/head.png)

-   tail

    `tail /proc/cpuinfo` menampilkan 10 baris terakhir dari cpuinfo

    `tail -n 5 /proc/cpuinfo` menampilkan 5 baris terakhir dari cpuinfo

    ![gambar 16](assets/tail.png)

## Monitoring

    melihat kinerja aktivitas sistem secara realtime. berikut perintah untuk memonitoring sebuah server :

-   htop

     `htop` melihat penggunaan memory, cpu, dan swap

    ![gambar 17](assets/htop.png)

-   nmon

    `nmon`

    > **C** untuk menampilkan cpu
    >
    > **D** untuk menampilkan disk

    ![gambar 18](assets/nmon1.png)

-   lsof

    `lsof` menampilkan seluruh proses

    ![gambar 19](assets/lsof.png)

    `lsof -u asdf` menampilkan proses yang dilakukan oleh user "asdf"

    ![gambar 20](assets/lsof-Uname.png)

    `lsof -i :80` menampilkan proses yang menggunakan port 80

    ![gambar 21](assets/lsof80.png)

-   ps

    `ps -f -u asdf` menampilkan proses pada user "asdf"

    ![gambar 22](assets/ps-f-u.png)

    `ps -aux` menampilkan proses secara lengkap

    ![gambar 23](assets/ps-aux.png)

## Network Firewall

   Network Firewall digunakan untuk mengamankan sebuah serveer. tools yang digunakan :

   `sudo ufw default deny incoming` memblokir semua akses yang masuk

   ![gambar 24](assets/ufw-deny.png)

   `sudo ufw default allow outgoing` membuka semua akses yang keluar

   ![gambar 25](assets/ufw-allow.png)

   `sudo ufw app list` menampilkan aplikasi yang didukung oleh ufw pada Server

   ![gambar 26](assets/ufw-app-list.png)

   `sudo ufw allow "Nginx full"` mengijinkan akses dari luar ke dalam untuk aplikasi nginx

   ![gambar 27](assets/ufw-allow-full.png)

   `sudo ufw allow 22` membuka akses untuk port  22

   ![gambar 28](assets/ufw-allow-22.png)

   `sudo ufw allow 22/tcp` membuka akses untuk port 22 dengan koneksi tcp

   ![gambar 29](assets/ufw-allow-tcp.png)

   `sudo ufw allow 22/udp` membuka akses untuk port 22 dengan koneksi udp

   ![gambar 30](assets/ufw-allow-udp.png)

   `sudo ufw deny 80` memblokir semua akses ke port 80

   ![gambar 31](assets/ufw-deny-80.png)

   `sudo ufw delete deny 80` menghapus konfigurasi, perintah harus sama dengan yang ingin dihapus

   ![gambar 32](assets/ufw-delete-deny.png)
