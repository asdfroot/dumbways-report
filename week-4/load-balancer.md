# Load Balancing

  Load Balancing adalah sebuah mekanisme untuk membagi atau mendistribusikan trafik ke beberapa server. Nginx selain berfungsi sebagai web server bisa juga berfungsi sebagai load balancer.

## Metode Load Balancing

-   Round Robin: mendistribusikan trafik ke setiap server secara bergantian.

-   Least Connections: mendistribusikan trafik ke server yang paling sedikit koneksi aktifnya.

-   IP Hash: mendistribusikan trafik ke server yang sama ketika visitor pertama kali melakukan request.

    ![gambar 0](assets/topologi.png)

## Load Balancing metode Round Robin dengan Nginx

-   Membuat file node.js

    `mkdir load-balancer-nginx` Membuat folder

    ![gambar 1](assets/mkdir.png)

    `cd load-balancer-nginx` Pindah directory yang telah dibuat

    `npm init -y` Membuat file package.json

    ![gambar 2](assets/npm-init-pack.png)

    `npm i express` Menginstal express

    ![gambar 3](assets/npm-express-i.png)

    `sudo nano index.js` Membuat aplikasi dengan format js

    ![gambar 4](assets/buatapp.png)

        const express = require("express");
        const app = express();
        const PORT = process.env.PORT;
        if (!PORT) {
              throw new Error("PORT variable not defined");
        }
        app.get("/", (req, res) => {
              const data = `App running at PORT ${PORT}`;
              return res.send(data);
        });
        app.listen(PORT, "0.0.0.0", () => console.log(`Server at ${PORT}`));

    ![gambar 5](assets/buat-app-nano.png)

    `export PORT=1212;` Mendefinisikan aplikasi 1 berjalan pada port 1212

    ![gambar 6](assets/jalanapp1212.png)

    `node index.js` Menjalankan aplikasi 1

    ![gambar 7](assets/berjalanport1212.png)

    `export PORT=1313;` Mendefinisikan aplikasi 2 berjalan pada port 1313

    ![gambar 8](assets/jalanapp1313.png)

    `node index.js` Menjalankan aplikasi 2

    ![gambar 9](assets/berjalanport1313.png)

    `cd /etc/nginx` Membuka directory nginx

    `sudo nano nginx.conf` Memasukan config

    ![gambar 10](assets/bukaconfig.png)

         http {
                upstream backend {
                        server 127.0.0.1:1212;
                        server 127.0.0.1:1313;
                }
                server {
                        listen 80;
                        root /home/asdf/load-balancer-nginx/;
                        location / {
                          proxy_pass <http://backend>;
      		              }
      	         }
          }
          events { }

    ![gambar 11](assets/config-conf.png)

    `nginx -s reload` Memuat ulang konfigurasi nginx

    ![gambar 12](assets/reload.png)

    Masukan `127.0.0.1` pada _url_ _**Web Browser**_ dan lakukan _Reload Current Page_ atau `CTRL+R` pada _**Web Browser**_, maka secara bergantian menampilkan halaman dari 1212 dan 1313

    ![gambar 13](assets/output1212.png)

    ![gambar 14](assets/output1313.png)
