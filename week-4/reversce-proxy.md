# Reverse Proxy

  Reverse proxy digunakan untuk mengamankan server dari serangan malware, dengan menggunakan reverse proxy, user tidak bisa langsung mengakses aplikasi secara langsung, sehingga harus melewati web server (nginx) sebagai jembatan. Untuk menggunakan reverse proxy pada nginx, berikut langkah yang akan kita lakukan :

## Reverse Proxy App node.js

    `cd /etc/nginx`

    `sudo mkdir js`

    ![gambar 1](assets/buatfolder.png)

    `sudo nano /etc/nginx/nginx.conf`

    ![gambar 2](assets/nanoconf.png)

    `sudo nano js.reverse-proxy.conf`

    ![gambar 3](assets/nanojsreverce.png)

    ![gambar 4](assets/nano-js-reverse-conf.png)

    `sudo nano /etc/hosts`

    ![gambar 5](assets/edit-etc-host.png)

    `sudo nginx -t`

    ![gambar 6](assets/tes.png)

    `sudo systemctl reload nginx`

    ![gambar 7](assets/reload.png)

    Masukan `nodejs.syarif.xyz` pada _url_ _**Web Browser**_

    ![gambar 8](assets/out.png)

## Reverse Proxy App Python

    `cd /etc/nginx`

    `sudo mkdir py`

    ![gambar 9](assets/mkdir.png)

    `sudo nano /etc/nginx/nginx.conf`

    ![gambar 10](assets/nanoconf.png)

    ![gambar 11](assets/nginx-conf.png)    

    `sudo nano py.reverse-proxy.conf`

    ![gambar 12](assets/proxy-conf.png)

    ![gambar 13](assets/nona-proxy.png)

    `sudo nano /etc/hosts`

    ![gambar 14](assets/edit-etc-host.png)

    `sudo nginx -t`

    ![gambar 15](assets/tes.png)

    `sudo systemctl reload nginx`

    ![gambar 16](assets/reload.png)

    Masukan `python.syarif.xyz` pada _url_ _**Web Browser**_

    ![gambar 17](assets/output.png)

## Reverse Proxy App Golang

    `cd /etc/nginx`

    `sudo mkdir go`

    ![gambar 1](assets/cdgo.png)

    `sudo nano /etc/nginx/nginx.conf`

    ![gambar 2](assets/nanoconf.png)

    `cd go.reverse-proxy.conf`

    `sudo nano go.reverse-proxy.conf`

    ![gambar 14](assets/cdgo.png)

    ![gambar 14](assets/nano-go.png)

    `sudo nano /etc/hosts`

    ![gambar 14](assets/edit-etc-host.png)

    `sudo nginx -t`

    ![gambar 15](assets/tes.png)

    `sudo systemctl reload nginx`

    ![gambar 16](assets/reload.png)

    Masukan `nodejs.syarif.xyz` pada _url_ _**Web Browser**_

    ![gambar 17](assets/outgolang.png)
