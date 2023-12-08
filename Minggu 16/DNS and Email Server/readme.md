`Tugas ini merupakan tugas mata kuliah Konsep Jaringan yang dibimbing oleh Bpk. Dr. Ferry Astika Saputra, ST, M.Sc`

# DNS dan Email Server

#### Apa Itu DNS dan DNS Server

DNS memiliki kaitan yang erat dengan IP address dari setiap website yang ada di internet. Setiap website membutuhkan layanan DNS untuk mengidentifikasi IP address. Pengertian DNS secara ringkas bisa diibaratkan sebagai buku telepon dari internet. Ketika pengguna mengetikkan nama domain seperti google.com pada URL bar di browser, DNS bertanggung jawab untuk mencari IP address yang sesuai dengan website tersebut. Browser kemudian menggunakan IP address tersebut untuk berkomunikasi dengan server untuk mengakses informasi dari sebuah website.<br>

Semua ini dapat berjalan berkat DNS Server, yaitu mesin yang bertugas untuk menjawab permintaan informasi tentang alamat IP sebuah website atau DNS Query. Jadi, DNS akan digabung di dalam DNS Server dan keduanya bekerja sama untuk menerjemahkan nama domain menjadi nomor IP address yang dipahami oleh browser/server.<br>

#### Fungsi DNS
Dari pengertian di atas, salah satu fungsi DNS adalah sebagai penerjemah antara pengguna dan server. Namun selain fungsi tersebut, DNS masih memiliki beberapa fungsi lainnya, yaitu:
- Memetakan hostname dan IP Address yang ada secara global.
- Meminta informasi IP Address sebuah website berdasarkan nama domain.
- Menerjemahkan suatu hostname ke IP address ataupun sebaliknya
- Mencari alamat host untuk memenuhi permintaan client.
- Pada sistem DNS cache berperan melakukan pencarian domain dengan lebih cepat.
- DNS Server mampu mengidentifikasi komputer yang ada di suatu jaringan .
- Memfasilitasi pengiriman email dengan mencarikan server yang tepat.
- Mengamankan aktivitas transfer data yang terjadi selama pengguna mengakses suatu website.

#### Cara Kerja DNS
Terdapat lima rangkaian proses utama pada cara kerja DNS Server dalam mengelola suatu website, berikut ini penjelasan lengkapnya,
1. Request DNS Query
Tahapan pertama dimulai ketika pengguna mulai mengetikkan nama domain ke URL Bar. DNS Server akan mencari berbagai informasi dalam file hosts, yaitu berkas file teks yang berada di dalam sistem operasi dan berfungsi untuk mengarahkan hostname ke alamat IP. Jika informasi yang dicari tidak ditemukan, maka server akan melakukan pencarian di cache, yaitu komponen hardware atau software yang menyimpan data untuk sementara.

Pada tahap ini ada 3 jenis DNS Query, yaitu:
- Recursive Query
Ketika pengguna memasukkan hostname, DNS Resolver memberikan semua informasi yang relevan dengan permintaan pengguna melalui pencarian root server dan authoritative name server.
- Iterative Query
Ketika pengguna memasukkan hostname, maka DNS Resolver akan mencari semua cache yang relevan pada memori. Apabila tidak ditemukan, maka DNS Resolver akan mencari beberapa informasi pada root server serta authoritative name server yang relevan sesuai DNS zone.
- Non-recursive Query
Tipe ini merupakan tipe pencarian informasi yang paling cepat, karena ketika pengguna memasukkan nama hostname, server telah berhasil menemukan informasi tentang IP Address yang tersimpan dalam sistem cache.  Misalnya, jika pengguna mengetikkan biznetgio.com pada URL Bar maka jenis DNS Query yang berjalan adalah Recursive Query.
2. DNS Recursive Resolver atau DNS Recursor
Tahap kedua adalah proses pencarian informasi yang telah diberikan oleh pengguna, yaitu nama domain pada URL Bar. Jika informasi yang diminta tidak ditemukan dalam cache, maka sistem akan meminta server lain untuk memenuhi permintaan tersebut atas nama klien (browser) dengan mencari informasi di cache ISP (Internet Service Provider). Inilah yang disebut recursor. Server ini layaknya agen yang berperan untuk menyediakan setiap informasi yang diminta. Misalnya seperti recursor 8.8.8.8 atau 1.1.1.1
3. Root Name Server
Jika informasi yang diminta tidak ditemukan pada cache ISP, maka recursor akan meminta bantuan pada Root Name server, yaitu database yang bisa memberi jawaban atas pertanyaan yang berkaitan dengan nama domain dan IP Address. Kemudian, server ini akan merespons permintaan tersebut dengan memberitahu agen untuk mengakses area yang lebih spesifik, yaitu top-level-domain name server (TLD name server).
4. TLD Name Server
Server untuk tipe top-level domain (.org, .com, ,au, .edu, .id, dan sebagainya) disebut TLD Name Server, yang berperan untuk mengelola semua informasi terkait ekstensi domain umum.
TLD Name Server kemudian akan merespons permintaan dari  DNS Recursive Resolver dan meneruskannya ke Authoritative DNS Server, atau Authoritative Name Server. Server inilah yang memiliki data asli dari domain tersebut.
5. Authoritative Name Server
Ketika DNS Recursive Resolver bertemu dengan Authoritative Name Server, saat itulah jawaban akan diberikan. Authoritative Name Server memiliki semua informasi yang berkaitan dengan website. Saat informasi telah sesuai, browser menampilkan berbagai situs web pada halaman awal yang diminta, namun pencarian tersebut punya masa waktu sendiri. Sehingga, pencarian ini harus diulang untuk memastikan berbagai informasi yang akan ditampilkan tetap up-to-date. Setelah tahap ini selesai, web browser akan menampilkan halaman website yang tadi kita minta.

#### Mengenal Jenis DNS
DNS Record merupakan informasi yang diminta oleh pengguna dalam sistem DNS. DNS Record akan mencatat keterhubungan suatu domain dengan IP. Pencatatan domainnya bervariasi, menyesuaikan kebutuhan pengguna. Ada beberapa jenis informasi yang bisa diminta dalam sistem DNS. Berikut adalah 10 DNS record yang paling sering dijumpai:
- A Record atau Address record; ─ menyimpan informasi soal hostname, time to live (TTL), dan IPv4 Address.
- AAA Record; sama seperti A Record hanya saja jenis DNS Record yang satu ini menyimpan informasi hostname dan hubungannya dengan IPv6 Address.
- MX Record; digunakan untuk merekam server SMTP yang berguna untuk memfasilitasi komunikasi email dalam suatu domain.
- CNAME Record; digunakan untuk me-redirect domain atau subdomain ke sebuah IP Address. Lewat fungsi satu ini, pengguna tak perlu memperbarui DNS record.
- NS Record; merujuk subdomain pada Authoritative Name Server yang diinginkan. Record ini berguna jika subdomain berada di web hosting yang berbeda dengan domain utama.
- PTR Record; memberikan izin pada DNS resolver untuk menyediakan informasi soal IP Address dan menampilkan hostname (reverse DNS lookup).
- TXT Record; membawa dan menyalurkan data yang hanya bisa dibaca oleh mesin.
- SOA Record; bagian yang muncul di awal dokumen DNS zone. Bagian yang sama juga merujuk pada Authoritative Name Server serta informasi lengkap sebuah domain.

#### Apa Itu Mail Server?
Mail server adalah server yang bertugas mengirim dan menerima email. Meskipun terlihat simpel, sebenarnya prosesnya pengiriman email cukup kompleks. Email yang Anda kirim akan  melewati serangkaian proses rumit di server email untuk dapat sampai ke penerima.  

Secara sederhana, fungsi mail server seperti kantor pos. Ia menyimpan surat masuk, lalu mengirimkannya ke penerima.

#### Komponen Mail Server
Secara umum, semua mail server terdiri dari tiga komponen yaitu MTA, MDA, dan MUA. Setiap komponen memiliki peran spesifik dalam proses memindahkan dan mengelola email.

1. MUA (Mail User Agent)
MUA adalah aplikasi yang digunakan untuk menyusun, mengirim, dan menerima email. Contoh MUA misalnya adalah Yahoo, Gmail, Outlook, dan layanan email yang lain. Beberapa MUA bisa tampak lebih grafis, seperti Evolution, Thunderbird, dan Outlook, atau memiliki interface yang berbasis teks sederhana seperti Mutt.

2. MTA (Mail Transport Agent) 
MTA merupakan salah satu komponen mail server yang bertugas menerima dan mengirim email dari komputer yang satu ke komputer yang lain. MTA memainkan peranan penting dalam sistem penanganan pesan internet. Beberapa tugas MTA antara lain:
- Menerima email.
- Meminta catatan mail exchange dan memilih server email untuk mentransfer email.
- Mengirim pesan respons otomatis jika pesan gagal sampai tujuan. 
3. MDA (Mail Delivery Agent)
MDA adalah sebuah software komputer yang bertanggung jawab mengantarkan email dari MTA sever. MDA juga dikenal sebagai LDA atau Local Delivery Agent. Beberapa MTA dapat mengisi peran MDA ketika mereka menambahkan pesan email baru ke file pesan pengguna lokal.

#### Protokol Mail Server
Sedangkan untuk protokol, terdapat dua kategori dalam server email: protokol surat keluar (SMTP) dan protokol surat masuk (IMAP dan POP3). Untuk mengetahui penjelasan lebih detail tentang dua kategori tadi, Anda dapat melihat poin-poin di bawah ini:

1. SMTP atau Simple Mail Transfer Protocol 
SMTP adalah protokol standar untuk transmisi atau pengiriman email. Protokol ini bertugas melakukan komunikasi dengan server untuk mengirimkan email dari lokal email ke server email.  Dalam proses kerjanya, SMTP dikontrol oleh MTA yang ada pada email server Anda.

2. POP3 atau Post Office Protocol 
POP 3 adalah versi ketiga dari metode penerimaan email. POP3 menerima dan menyimpan email untuk seseorang sampai mereka mengambilnya. POP3 adalah protokol server/client tempat di mana email dikirimkan dari server menuju email lokal. POP3 bekerja dengan mengontak server email Anda, lalu mengunduh semua pesan baru dari email lokal. Setelah Anda mengunduhnya, mereka akan hilang dari server. Jadi, jika Anda memutuskan untuk memeriksa email Anda dengan gadget yang berbeda, pesan yang sudah Anda unduh sebelumnya tidak akan ada lagi. Itulah mengapa, ada baiknya untuk melakukan back up. POP3 cocok digunakan untuk Anda yang biasanya membuka email dengan hanya satu gadget.

3. IMAP atau Internet Message Access. 
IMAP memungkinkan Anda dapat mengakses email Anda di mana pun Anda berada, biasanya diakses melalui internet. Ketika Anda membaca email menggunakan IMAP, Anda sebenarnya tidak mengunduh atau menyimpannya ke komputer, tetapi membacanya melalui server. Untuk Anda yang sering bepergian dan sering menggunakan berbagai gadget untuk mengakses email, kami sarankan untuk menggunakan servis email berbasis IMAP.

#### Cara Kerja Mail Server
Pada dasarnya, cara kerja utama mail server adalah sending email (mengirim email) dan receiving email (menerima email) yang akan melalui lima tahapan berikut:
1. Tahap 1: Mengirim Pesan
Setelah membuat pesan dan meng-klik tombol send, MUA akan mengirim email tersebut. Kemudian, email penerima/ klien akan terkoneksi dengan server SMTP domain Anda. Server ini bisa bernama apa saja, misalnya smtp.misalnya.com.

2. Tahap 2: Email Penerima Berkomunikasi dengan Server SMTP 
Email penerima/klien berkomunikasi dengan MTA server yang menggunakan SMTP. Kemudian memberikannya alamat email Anda, alamat email penerima, isi pesan dan lampiran.

3. Tahap 3: Server SMTP Memproses Alamat Email Penerima 
Setelah berkomunikasi dengan email penerima, komponen MDA melalui SMTP akan memproses alamat email penerima (khususnya domain-nya). Jika nama domain sama dengan pengirim pesan, maka pesan akan langsung dialihkan ke server domain POP3 atau IMAP.Namun, jika domain berbeda, server SMTP akan berkomunikasi dengan server domain terlebih dahulu. 

4. Tahap 4: Server SMTP Pengirim Berkomunikasi dengan DNS
Agar bisa menemukan server penerima, MTA melalui SMTP harus berkomunikasi dengan DNS. Atau, Server Nama Domain. Nanti DNS akan mengambil nama email domain penerima, lalu menerjemahkannya menjadi sebuah IP address.Kenapa harus dijadikan IP address? Karena server SMTP pengirim tidak bisa menyalurkan email dengan benar hanya dengan nama domain. Maka, dibutuhkan IP address, yang merupakan sebuah nomor identitas setiap komputer yang terkoneksi internet.Dengan mengetahui informasi IP address-nya, mail server dapat bekerja dengan lebih efisien.

5. Tahap 5: Email Terkoneksi dengan Server SMTP
Setelah server SMTP memiliki IP address penerima, maka email yang diteruskan MDA/MTA dapat terkoneksi dengan server SMTP. Proses ini tidak terjadi begitu saja. Karena, sebenarnya pesan yang dikirim tadi harus melewati serangkaian proses SMTP, sampai akhirnya tiba di tujuan.  

6. Tahap 6: Server SMTP Penerima Memindai Pesan Masuk
Di tahap ini MUA memindai pesan masuk. Jika ia mengenali domain dan username, pesan akan diteruskan ke server POP3 atau IMAP domain. Dari sana, pesan akan ditempatkan di antrean sendmail. Pesan akan berada di antrian sendmail sampai email penerima mengizinkannya untuk diunduh. 

