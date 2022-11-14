# __Writing Test Week 7__
## __Sequelize__

- Sequelize ORM (Object Relational Mapping) : Node JS yang berbasis promise.

- Install Sequielize-cli 
```
npm install -g sequelize-cli
```
- Install driver mysql 
```
npm install save mysql2
```
- Sequelize init 
```
npx sequelize-cli init
```
- Generate Model 
```
npx sequelize model:create --name User --attributes name:string,email:string,password:string
```
- Generate Model Database 
```
npx sequelize db:migrate
```
- Generate Model Database 
```
npx sequelize db:migrate:undo
```
- Generate Seed : Seed adalah data awal yang digunakan untuk mengisi database 
```
npx sequelize seed:create --name demo-user
```

<hr>


## __MongoDB__

- MongoDB : salah satu produk database noSQL Open Source yang menggunakan struktur data JSON untuk menyimpan datanya dan sering dipakai untuk aplikasi berbasis Cloud, Grid Computing, atau Big Data.

- NoSQL adalah Not Only SQL : mengolah database dengan fleksibel dan tidak membutuhkan Query

- Kelebihan sebagai salah satu NoSQL :
    - Sistem tidak membutuhkan Tabel
    - Tidak perlu menggunakan Tabel yang terstruktur
    - By Default sudah menggunakan JSON(JavaScript Object Notation), sehingga memudahkan integrasi dengan JavaScript
    - Performa lebih cepat dengan kemampuan menampung banyak data yang bervariasi

- Kekurangan sebagai salah satu NoSQL :
    - Tidak mendukung transaksi
    - Masalah konsistensi data
    - Menggunakan banyak memory
    - Hanya bisa menampung maksimal 16MB disetiap document

- Contoh data pada MongoDB
![x](/img/1.png)

- Command untuk menjalankan, menghentikan, dan memulai ulang mongodb
```
sudo service mongod start
sudo service mongod stop
sudo service mongod restart
```

<hr>

## __Mongoose__

- Mongoose : library yang bisa dibilang sebagai Object Modelling MongoDB untuk NodeJS dan digunakan untuk mengelola hubungan antara data, menyediakan validasi dan untuk menerjemahkan antara objek dalam kode dan representasi Objek tersebut di MongoDB.

- Instalasi
```
npm install mongoose
```

- Buat koneksi Mongoose npm install mongoose const mongoose 
```
require("mongoose"); const DB_URL = "mongodb://localhost:27017/sekolahku" const db = mongoose.connect(DB_URL); module.exports = db;
```
- Buat koneksi Mongoose const mongoose 
```
 require("mongoose"); const DB_URL = "mongodb://localhost:27017/sekolahku" const db = mongoose.connect(DB_URL); module.exports = db;
```

- Skema Mongoose const mongoose 
```
require("mongoose"); const DB_URL = "mongodb://localhost:27017/sekolahku" const db = mongoose.connect(DB_URL); module.exports = db; mongoose = require("mongoose"); const { Schema } = mongoose; const userSchema = new Schema({ // name: String, email: { type: String, require: true, }, password: String, address: { name: String, no: Number, kecamatan: String, }, }); const User = mongoose.model("User", userSchema);
```

<hr>

## __Docker__

- Docker : software yang menjalankan suatu aplikasi menggunakan container dan men-sharing kernel dari host OS, serta meng-container-kan suatu aplikasi agar dapat dijalankan dimana saja dan kapan saja dan berfungsi sebagai penyedia layanan virtual bagi aplikasi yg diinstall pada sebuah host. 

- Perbedaan VM dan container VM memakan banyak resource dan waktu utk booting karena melakukan virtualisasi pada host hardware-nya, sedangkan container kebalikannya dari vm, container melakukan virtualisasi pada host OS-nya

- Docker File : Blueprint untuk membuat image
    Caranya:

    - Buat file Dockerfile di dalam project yang kamu buat
    - Tulis beberapa perintah ke dalam dockerfile
    - Jalankan docker file menggunakan perintah 
    ```
    docker build -t NAMA_IMAGES:TAG . 
    docker build -t my-app:1.0 . 
    ```

-  Docker Compose : menjalankan lebih dari 1 container secara bersamaan dan saling terhubung

    Caranya:
    - Buat file NAMA_FILE.yaml di dalam project yang kamu buat
    - Tulis beberapa perintah ke dalam sana
    - Jalankan menggunakan perintah 
    ```
    docker-compose NAMA_FILE.yaml up
    ```





 

