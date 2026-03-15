# Simulasi-Kasus-SOC-Analyst-L1-Berdasarkan-Kejadian-Nyata-

asus Brute Force SSH
Interviewer

Kami melihat banyak login gagal di server Linux. Log seperti ini muncul:

Failed password for root from 185.234.217.12 port 45821 ssh2
Failed password for root from 185.234.217.12 port 45822 ssh2
Failed password for root from 185.234.217.12 port 45823 ssh2

Apa yang kamu lakukan?

Cara Menjawab

Dari log tersebut terlihat adanya percobaan login SSH yang gagal berulang kali menggunakan user root dari IP address yang sama.

Hal ini kemungkinan besar merupakan indikasi brute force attack.

Langkah yang saya lakukan adalah:

Memeriksa jumlah login gagal dari IP tersebut.

Mengecek apakah ada login yang berhasil setelah percobaan tersebut.

Memeriksa reputasi IP address menggunakan threat intelligence tools.

Jika aktivitas tersebut mencurigakan, saya akan merekomendasikan untuk memblokir IP tersebut dan melakukan eskalasi kepada tim yang lebih senior.

2️⃣ Kasus Phishing Email


Seorang user melaporkan email mencurigakan yang meminta reset password. Apa yang kamu lakukan?

Jawaban

Langkah pertama adalah melakukan analisis terhadap email tersebut dengan memeriksa header email untuk melihat sumber pengirim sebenarnya.

Kemudian saya akan memeriksa domain pengirim apakah termasuk domain yang mencurigakan atau tidak.

Saya juga akan memeriksa apakah email tersebut mengandung link atau attachment berbahaya.

Jika email tersebut terkonfirmasi sebagai phishing, saya akan melaporkannya kepada tim keamanan dan melakukan blokir domain tersebut di email gateway.

3️⃣ Kasus Malware di Endpoint


Antivirus mendeteksi file malware pada laptop user. Apa langkah kamu?

Jawaban

Jika antivirus mendeteksi malware pada endpoint, langkah pertama adalah melakukan containment dengan mengisolasi endpoint tersebut dari jaringan untuk mencegah penyebaran malware.

Setelah itu saya akan melakukan analisis terhadap file tersebut seperti memeriksa hash file dan memverifikasinya di threat intelligence database.

Selanjutnya saya akan melakukan scanning ulang sistem dan memastikan malware tersebut telah dihapus sepenuhnya.

4️⃣ Kasus Login dari Negara Tidak Biasa


Ada login ke akun admin dari negara yang tidak pernah digunakan sebelumnya. Apa yang kamu lakukan?

Jawaban

Saya akan memverifikasi apakah login tersebut dilakukan oleh user yang sah atau tidak.

Jika login tersebut tidak biasa, saya akan memeriksa aktivitas yang dilakukan setelah login seperti akses file atau perubahan konfigurasi sistem.

Jika ditemukan aktivitas mencurigakan, saya akan merekomendasikan untuk melakukan reset password dan memonitor aktivitas akun tersebut lebih lanjut.

5️⃣ Kasus Port Scanning

Firewall menunjukkan banyak koneksi dari satu IP ke banyak port berbeda. Apa indikasinya?

Jawaban

Aktivitas tersebut kemungkinan merupakan port scanning yang dilakukan untuk mencari port terbuka pada sistem target.

Port scanning biasanya merupakan tahap reconnaissance sebelum attacker melakukan eksploitasi.

Saya akan memeriksa IP address tersebut dan jika aktivitasnya mencurigakan, IP tersebut dapat diblokir di firewall.

6️⃣ Kasus Traffic ke Domain Berbahaya


SIEM menunjukkan ada koneksi dari endpoint ke domain yang dikenal sebagai malware domain. Apa yang kamu lakukan?

Jawaban

Hal ini dapat menjadi indikasi bahwa endpoint tersebut telah terinfeksi malware yang mencoba berkomunikasi dengan command and control server.

Langkah yang saya lakukan adalah:

Memeriksa endpoint yang melakukan koneksi tersebut.

Memeriksa proses yang berjalan di endpoint tersebut.

Mengisolasi endpoint jika diperlukan.

Melakukan analisis lebih lanjut terhadap aktivitas tersebut.

7️⃣ Kasus Banyak Alert dari SIEM


Jika SIEM menghasilkan ratusan alert dalam satu hari, bagaimana kamu menanganinya?

Jawaban

Saya akan memprioritaskan alert berdasarkan severity level yang diberikan oleh SIEM.

Alert dengan tingkat critical atau high akan dianalisis terlebih dahulu karena memiliki potensi dampak yang lebih besar terhadap sistem organisasi.

Setelah itu saya akan melakukan triage untuk menentukan apakah alert tersebut merupakan true positive atau false positive.

8️⃣ Kasus Suspicious Process di Windows


Kamu melihat proses aneh berjalan di Windows server. Apa yang kamu lakukan?

Jawaban

Saya akan memeriksa detail proses tersebut seperti nama file, lokasi file, dan parent process.

Kemudian saya akan memeriksa hash file tersebut menggunakan threat intelligence tools untuk mengetahui apakah file tersebut berbahaya atau tidak.

Jika file tersebut mencurigakan, saya akan melakukan isolasi sistem dan melakukan investigasi lebih lanjut.

9️⃣ Kasus User Mengunduh File Mencurigakan


User mengunduh file dari website yang tidak dikenal. Apa yang kamu lakukan?

Jawaban

Saya akan memeriksa file tersebut menggunakan antivirus atau sandbox untuk mengetahui apakah file tersebut mengandung malware.

Saya juga akan memeriksa aktivitas sistem setelah file tersebut dijalankan untuk memastikan tidak ada perubahan mencurigakan pada sistem.

🔟 Kasus Credential Leak


Kami menemukan username dan password karyawan di dark web. Apa langkah kamu?

Jawaban

Jika ditemukan credential leak, langkah pertama adalah melakukan reset password pada akun yang terdampak.

Kemudian melakukan monitoring terhadap aktivitas login untuk memastikan tidak ada penyalahgunaan akun tersebut.

Selain itu, saya akan merekomendasikan penggunaan multi-factor authentication untuk meningkatkan keamanan akun.

Pola Jawaban yang Disukai SOC Interviewer

Saat menjawab studi kasus, gunakan pola ini:

1️⃣ Identifikasi masalah

contoh:

Dari log tersebut terlihat adanya percobaan login gagal berulang.

2️⃣ Analisis kemungkinan serangan

contoh:

Hal ini kemungkinan merupakan brute force attack.

3️⃣ Langkah investigasi

contoh:

Saya akan memeriksa log, IP address, dan aktivitas login lainnya.

4️⃣ Tindakan

contoh:

Jika mencurigakan, saya akan melakukan eskalasi atau memblokir IP tersebut.

Rahasia Interview SOC yang Jarang Diberitahu

User sebenarnya melihat 3 hal ini:

1️⃣ Cara berpikir seperti analis

bukan hanya hafalan

2️⃣ Bisa membaca log
3️⃣ Tidak panik saat incident
