# Pembuatan Aplikasi

## Instalasi Node.js

   Aplikasi yang dibuat oleh javascript (node.js) maka perlu instal node.js

   `curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.38.0/install.sh|bash`

   `nvm install 16.13.0`
   
   ![gambar 1](assets/instal2.png)

   `nvm use 16`

   ![gambar 2](assets/cekcek.png)

   Jika instalasi node.js sudah berhasil, untuk mengeceknya gunakan perintah :

   `node -v`
   
   `npm -v`

   ![gambar 3](assets/ver.png)

-   Membuat example app Node.js :

   `mkdir myapp-nodejs` Membuat folder baru dengan nama myapp-nodejs

   `cd myapp-nodejs` Pindah directory ke myapp-nodejs

   ![gambar 4](assets/buatfolder.png)

   `npm init -y` Membuat file package.json

   ![gambar 5](assets/buatjson.png)

   `npm install express` Menginstal express

   ![gambar 6](assets/expressinstal.png)

   `nano index.js` Membuat file dengan index.js

   ![gambar 7](assets/nanabuat.png)

      const express = require('express')
      const app = express()
      const port = 3000
      app.get('/', (req, res) {
        res.send('Hello World!')
      })
      app.listen(port, () => {
        console.log('Example app listening at http://localhost:${port}')
      })

   ![gambar 8](assets/nanocode.png)    

   `CTRL+X` untuk keluar dan `y` untuk menyimpan dan yang terakhir tekan `Enter`

   `node index.js` Untuk menjalankan aplikasi

   ![gambar 9](assets/jalan.png)

   Masukan `http://localhost:3000` pada _url_ _**Web Browser**_

   ![gambar 10](assets/berjalan.png)

## Instalasi Python

   Aplikasi yang dibuat dengan Python maka perlu instal Python

   `sudo apt update` Update sistem

   ![gambar 11](assets/instal1.png)

   `sudo apt upgrade -y` Upgrade sistem

   ![gambar 12](assets/instalkk.png)

   `python3 -V` Biasanya Python sudah ada secara default

   ![gambar 13](assets/python3-v.png)

   `sudo apt install python3-pip` Instalasi package manager

   ![gambar 14](assets/pip.png)

   `pip install flask` Instalsi flask

   ![gambar 15](assets/instal4.png)

-   Membuat example app Python :

   `mkdir python` Membuat sebuah folder

   ![gambar 16](assets/folder.png)

   `nano index.py` Membuat file index.py

   ![gambar 17](assets/nanoedit.png)

      from flask import Flask
      app = Flask(__name__)
      @app.route("/")
      def hello_world():
          return "<p>Hello, World!</p>"
      if __name__=="__main__":
          app.run()

   ![gambar 18](assets/buatnano.png)

   `python3 index.py` Menjalankan aplikasi

   ![gambar 19](assets/menjalankan.png)

   Masukan `http://localhost:5000` pada _url_ _**Web Browser**_

   ![gambar 20](assets/webview.png)

## Instalasi Golang

   Aplikasi yang dibuat dengan Golang maka perlu instal Golang

   `wget https://go.dev/dl/go1.17.3.linux-amd64.tar.gz` Download Golang

   ![gambar 21](assets/down.png)

   `sudo tar -C /usr/local -xzf go1.17.3.linux-amd64.tar.gz` Upgrade sistem

   ![gambar 22](assets/extra.png)

   `nano .bashrc` Memasukan path go pada bashrc

   ![gambar 23](assets/editbash.png)

   Dipaling bawah file **.bashrc** isi path go `export PATH=$PATH:/usr/local/go/bin`

   ![gambar 24](assets/export.png)

   `go version` Verifikasi instalasi

   ![gambar 25](assets/verif.png)

   `mkdir golang` Membuat directory golang

   `cd golang` Pindah directory

   ![gambar 26](assets/buatfol.png)

   `nano index.go` Membuat sebuah file index.go

   ![gambar 27](assets/buatnano-go.png)

      package main
      import (
    	        "fmt"
    	        "log"
    	        "net/http"
      )
      const port string = "2000"
      func welcome(w http.ResponseWriter, r *http.Request) {
    	      dataHTML := `<h1>Sebutkan Satu Mahluk Hidup yang Serakah</h1>
    		      <ul>
    			       <li>Manusia</li>
    		      </ul>
    		      Referensi : <a href="https://youtu.be/Q_WHGV5bejk">Video</a>`
    	      if r.Method == "GET" {
    		        fmt.Fprintf(w, dataHTML)
    	      }
      }
      func main() {
    	      fmt.Println("Berjalan di Port :", port)
    	      http.HandleFunc("/", welcome)
    	      if err := http.ListenAndServe(":"+port, nil); err != nil {
    		        log.Fatal(err)
    	      }
      }

   ![gambar 28](assets/nanogoindex.png)

   Masukan `http://localhost:2000` pada _url_ _**Web Browser**_

   ![gambar 29](assets/out.png)
