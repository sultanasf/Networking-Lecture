# OSI Layer

## Definisi OSI

OSI sendiri adalah singkatan dari Open System Interconnections. Model OSI adalah sebuah kerangka kerja yang digunakan untuk memahami dan menggambarkan bagaimana protokol jaringan komunikasi berinteraksi satu sama lain. Model ini terdiri dari tujuh lapisan (Layer) yang mewakili fungsi-fungsi yang berbeda dalam komunikasi jaringan. Setiap lapisan bertanggung jawab atas tugas-tugas tertentu yang membantu dalam pengiriman data antara perangkat di jaringan.

## Layer/lapisan dalam OSI

![osi layer](./assets/osi%20layer.jpeg)

Gambar diatas adalah ilustrasi mengenai lapisan/layer pada OSI. Berikut adalah penjelasan dari tiap layer:

1. **Application Layer**
Fungsi: Lapisan aplikasi adalah lapisan paling atas yang berinteraksi langsung dengan pengguna dan aplikasi.
Proses: Menyediakan layanan komunikasi dan interaksi antara pengguna dan jaringan. Contoh protokol di lapisan ini termasuk HTTP, FTP, SMTP, dan banyak lagi.

2. **Presentation Layer**
Fungsi: Lapisan presentasi menyediakan konversi format data, enkripsi, dan kompresi data.
Proses: Mengubah format data dari representasi internal ke format yang dapat dimengerti oleh penerima. Juga, mengenkripsi dan mendekompressi data jika diperlukan.

3. **Session Layer**
Fungsi: Lapisan ini mengelola dan mengontrol dialog antara aplikasi yang berjalan di perangkat yang berbeda.
Proses: Membuka, menjalankan, dan menutup sesi komunikasi antara aplikasi. Ini melibatkan sinkronisasi dan pengelolaan aliran data serta pengaturan sesi.

4. **Transport Layer**
Fungsi: Lapisan transport menyediakan pengiriman data yang andal antara perangkat akhir, mengelola aliran data, dan mengatur pengendalian kesalahan.
Proses: Memecah data menjadi segmen, menambahkan nomor urut untuk memastikan pengiriman yang benar, dan menyediakan mekanisme untuk mengatur aliran data dan pemulihan kesalahan.

5. **Network Layer**
Fungsi: Lapisan ini mengelola pengiriman paket data melalui jaringan yang berbeda dan mengontrol routing data.
Proses: Pengalamatan logis (IP address) dan routing data melalui jaringan menggunakan algoritma dan tabel routing. Ini memungkinkan pengiriman data melalui beberapa jaringan yang berbeda.

6. **Data Link Layer**
Fungsi: Lapisan ini mengelola akses ke media fisik, mengatur aliran data dalam bentuk frame, dan mengelola deteksi serta koreksi kesalahan.
Proses: Pembuatan dan pemecahan frame data, mengirimkan frame ke tujuan yang tepat, dan menangani pengenalan alamat fisik (MAC address) pada jaringan lokal.

7. **Physical Layer**
Fungsi: Lapisan fisik bertanggung jawab atas transmisi sinyal fisik melalui media transmisi seperti kabel, serat optik, atau gelombang radio.
Proses: Mengubah bit menjadi sinyal fisik dan mengirimkannya melalui media transmisi. Ini melibatkan pemilihan tipe kabel, pengaturan voltase, frekuensi, dan pengkodean sinyal.

Ketika data dikirim melalui jaringan, setiap lapisan menambahkan informasi dan kontrol yang diperlukan untuk mengatur komunikasi yang efektif antara perangkat di berbagai lapisan. Data melewati lapisan demi lapisan saat dikirim, dan di sisi penerima, data didekapsulasi lapisan demi lapisan hingga sampai ke aplikasi penerima.

Berikut adalah ilustrasi perubahan data hingga menjadi bits(101010) pada tiap layer:

![data layer](./assets/layer%20data.jpg)