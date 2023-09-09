# Ping dan Tracert

#### :bulb: Apa Itu Ping?

Ping merupakan singkatan dari **Packet Internet Network Groper**. Secara sederhana, ping adalah perintah untuk mengecek status dan keberadaan host dalam sebuah jaringan internet. Sebagai contoh, client bisa menggunakan ping untuk mengecek apakah server dari website yang client akses berjalan baik. Ketika melakukan ping, client akan mendapatkan hasil sesuai dengan respon dari host tujuan.

> **:memo: Cara Kerja Ping**

Prinsip utama ping adalah seperti penggunaan sonar untuk mengukur kedalaman laut. Jadi, sebuah sinyal dikirimkan ke dasar, lalu lamanya waktu kembali ke atas menjadi dasar perhitungannya.

Prinsip utama ping adalah seperti penggunaan sonar untuk mengukur kedalaman laut. Jadi, sebuah sinyal dikirimkan ke dasar, lalu lamanya waktu kembali ke atas menjadi dasar perhitungannya.

Nah, cara kerja ping hampir mirip contoh di atas. Dengan perintah ping, client akan mengirim sebuah paket data berupa ICMP_ECHO ke host tujuan. Lalu, host akan membalas dengan paket data berupa ICMP_ECHOREPLAY. Kalau client tidak mendapat jawaban, itu artinya host mungkin sedang tidak aktif. Kalau jawaban yang client terima lama, bisa jadi ada kendala yang perlu dicari tahu lebih lanjut.

> **:memo: Fungsi Ping**

Sesuai dengan cara kerjanya, ada tiga fungsi ping yang bisa dimanfaatkan:

- Mengecek apakah host atau server dalam keadaan aktif.
- Mengukur berapa lama respon yang diberikan host sebagai petunjuk apakah ada kendala jaringan.
- Melihat kualitas koneksi internet Anda berdasarkan hasil respon ping yang Anda terima.

# Tracert

#### :bulb: Apa Itu Tracert?

Traceroute atau tracert adalah network diagnostic tool yang digunakan untuk melacak setiap rute jaringan yang dilalui oleh IP address secara real-time.

Sederhananya, jika sedang mengunjungi suatu website, data yang didapatkan dari website tersebut tentunya harus melintasi beberapa perangkat dan jaringan di sepanjang jalan, terutama router. Traceroute melacak bagaimana data di internet bergerak dari sumbernya ke tujuannya.

Selama melacak perjalanan jaringan, tracert juga mampu mengetahui kesalahan atau kegagalan yang terjadi selama proses pertukaran data berlangsung. Di situlah tracert berperan sebagai alat diagnosa jaringan. Sehingga dapat menunjukkan di mana lokasi yang menyebabkan koneksi internet kamu bermasalah.

> **:memo: Cara Kerja Tracert**

Sesuai namanya, tracert bekerja dengan cara melacak trace route suatu jaringan. Pelacakan tersebut dilakukan dengan mengirimkan paket Internet Control Message Protocol (ICMP). Paket ini, berfungsi untuk memberikan informasi apakah router yang digunakan dalam perjalanannya dapat mentransfer data secara efektif atau tidak.

> **:memo: Fungsi Tracert**

Fungsi atau kegunaan tracert adalah sebagai berikut:

- Membantu mencari di mana letak masalah pada jaringan, sehingga akan lebih mudah untuk memperbaikinya
- Membantu mengetahui jika server website bermasalah lewat pelacakan rute yang dilakukan
- Melihat nama ISP dan jaringan yang digunakan. Informasi ini biasanya akan muncul pada hop ke 4
- Memantau kualitas jaringan perangkat berdasarkan respon saat melakukan traceroute
