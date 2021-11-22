# Perintah Git Versioning
Perintah-perintah untuk git versioning :

## Git Config

 >git config --global user.name "nama_user"

 >git config --global user.email "email_anda"

 >git config --list

![gambar g1](assets/g1.PNG)

## Membuat SSH

 >ssh-keygen

 >cat id_rsa.pub

 >ssh -T git@github.com

![gambar g2](assets/g2.PNG)

## Repository Management

 >git init .

 >.gitignore

 >git status

![gambar g3](assets/g3.PNG)

## Git Add & Commit

**Git Add**

- menambahkan file

 > git add nama_file

 - Menambahkan File yang berakhiran *.html

  > git add .html

  - Melakukan add ke semua file

   > git add .

![gambar g4](assets/g4.PNG)

**Git Commit**

- Git commit maka file suda di upload ke databas

 > git commit -m "pesan commit"

![gambar g5](assets/g5.PNG)

## Git Remote
Pengembangan aplikasi, perlu adanya server untuk menyimpan semua perubahan agar semua orang dapat berkontribusi. beberapa layanan repository :

- github
- GitLab
- BitBucket

>git branch -M main

>git remote add origin git@github.com:marni/contoh.git

>git push -u origin main

![gambar g6](assets/g6.PNG)

## Git Branch
git branch digunakan untuk membuat versi dari repository :

- Membuat branch baru

>git branch nama_branch

- Merename branch

>git branch -M nama_branch

- Membuat list branch

>git branch -a

![gambar g7](assets/g7.PNG)

## Git Checkout
Git checkout digunakan untuk berpindah dari satu branch ke branch yang lain :

- Pindah dari branch staging ke banch production

>git checkout production

![gambar g8](assets/g8.PNG)

## Git Push
Git push di gunakan untuk upload file dari file local ke database server github, berikut cara penggunaan nya :


 >git push origin nama_branch

![gambar g9](assets/g9.PNG)

## Git Pull
Git pull merupakan perintah untuk menyamakan perubahan yang terjadi pada server git, berikut cara penggunaan nya : :

>git pull origin nama branch

![gambar g10](assets/g10.PNG)
