# Simulasi-Kasus-SOC-Analyst-L1-Berdasarkan-Kejadian-Nyata-dan beberapa istilah istilah paling familiar 

Kasus Brute Force SSH
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
2️⃣ Bisa membaca log 
3️⃣ Tidak panik saat incident

# Dasar Jaringan 

1️⃣ Konsep Dasar Networking

Network adalah sistem yang menghubungkan beberapa perangkat untuk saling bertukar data.

Contoh perangkat dalam network:

Laptop
Server
Router
Firewall
Switch

Contoh sederhana:

Laptop → Router → Internet → Server

Ketika user membuka website:

Laptop → DNS → dapat IP → koneksi ke server

SOC Analyst biasanya memonitor aktivitas ini melalui log jaringan.

2️⃣ IP Address

IP Address adalah alamat unik perangkat di jaringan.

Contoh:

192.168.1.10
8.8.8.8
172.217.22.14

IP Address digunakan agar perangkat bisa saling menemukan satu sama lain.

Contoh komunikasi:

192.168.1.10 → 142.250.190.14

Artinya:

Laptop → Server Google
Jenis IP Address
Private IP

Digunakan di jaringan lokal.

Contoh:

192.168.x.x
10.x.x.x
172.16.x.x
Public IP

Digunakan di internet.

Contoh:

8.8.8.8
1.1.1.1
Dalam SOC

IP Address digunakan untuk:

melacak attacker

melihat sumber serangan

melihat tujuan koneksi

Contoh log:

Source IP: 185.220.101.45
Destination IP: 192.168.1.10
3️⃣ Port

Port adalah pintu komunikasi dalam jaringan.

Contoh:

IP = rumah
Port = pintu rumah

Satu server bisa memiliki banyak layanan.

Contoh:

IP: 192.168.1.10

Port:

22  → SSH
80  → HTTP
443 → HTTPS
21  → FTP

Contoh koneksi:

192.168.1.5 → 192.168.1.10:22

Artinya:

client mencoba SSH ke server
Dalam SOC

Port digunakan untuk:

mendeteksi scanning

melihat layanan yang diserang

Contoh log:

Connection attempt to port 22
Connection attempt to port 80
Connection attempt to port 443

Kemungkinan:

port scanning
4️⃣ Protocol Penting

Protocol adalah aturan komunikasi jaringan.

SOC sering melihat protocol ini.

DNS

DNS mengubah domain menjadi IP address.

Contoh:

google.com → 142.250.190.14

Prosesnya:

User buka google.com
↓
DNS request
↓
DNS server memberi IP
↓
Browser koneksi ke server
SOC sering melihat log seperti ini
DNS query: suspicious-domain.ru

Jika domain berbahaya:

⚠️ kemungkinan malware.

HTTP

HTTP digunakan untuk komunikasi web.

Port:

80

Contoh request:

GET /login HTTP/1.1
Host: example.com

SOC bisa mendeteksi:

SQL injection
web attack
suspicious request
HTTPS

HTTPS adalah HTTP yang dienkripsi.

Port:

443

Menggunakan:

TLS encryption

SOC tidak bisa melihat isi data, tetapi bisa melihat:

IP
domain
certificate
traffic pattern
5️⃣ TCP vs UDP

Ini pertanyaan interview SOC yang sangat sering muncul.

TCP

TCP adalah protocol connection oriented.

Artinya koneksi dibuat terlebih dahulu.

Contoh protocol:

HTTP
HTTPS
SSH
FTP
TCP Handshake
Client → SYN
Server → SYN-ACK
Client → ACK

Tujuannya memastikan koneksi stabil.

UDP

UDP adalah protocol connectionless.

Tidak ada handshake.

Contoh:

DNS
VoIP
Streaming

Keunggulan:

lebih cepat
6️⃣ OSI Layer Model

OSI Model menjelaskan bagaimana data bergerak dalam jaringan.

Ada 7 layer.

Namun SOC biasanya fokus pada 3 layer ini.

Layer	Nama	Contoh
7	Application	HTTP DNS
4	Transport	TCP UDP
3	Network	IP
Cara mudah mengingat
Application → HTTP DNS
Transport → TCP UDP
Network → IP
7️⃣ Bagaimana SOC Menggunakan Network Knowledge

SOC menggunakan network untuk menganalisis:

IP
Port
Protocol
Domain
Traffic

Contoh log:

Source IP: 192.168.1.5
Destination IP: 185.199.110.153
Port: 443
Protocol: HTTPS

SOC akan menganalisis:

siapa sumbernya

kemana koneksi

menggunakan protocol apa

apakah mencurigakan

8️⃣ Contoh Investigasi SOC Berdasarkan Network
Kasus 1: Port Scanning

Log:

203.0.113.5 → port 21
203.0.113.5 → port 22
203.0.113.5 → port 80
203.0.113.5 → port 443

Analisis:

Satu IP mencoba banyak port.

Kemungkinan:

port scanning
Kasus 2: DNS Malware

Log:

DNS query: malware-domain.ru

Analisis:

Endpoint mencoba mengakses domain berbahaya.

Kemungkinan:

malware communication
Kasus 3: Brute Force SSH

Log:

Failed password for root from 185.220.101.45

Analisis:

Login gagal berulang.

Kemungkinan:

brute force
Cara Menjawab Saat Interview SOC

Gunakan pola ini:

1️⃣ Identifikasi

Dari log tersebut terlihat adanya aktivitas mencurigakan.

2️⃣ Dugaan serangan

Hal ini kemungkinan merupakan brute force attack.

3️⃣ Investigasi

Saya akan memeriksa log lebih lanjut seperti IP address dan timestamp.

4️⃣ Tindakan

Jika aktivitas tersebut mencurigakan, saya akan melakukan eskalasi kepada tim SOC Level 2.

Ringkasan Cepat (Untuk Hafalan Interview)
Network
IP = alamat perangkat
Port = pintu layanan
Protocol = aturan komunikasi
Protocol penting
DNS → domain ke IP
HTTP → web
HTTPS → web encrypted
Transport
TCP → reliable
UDP → cepat
OSI Layer penting
Application
Transport
Network


# Istilah istilah di jaringan / network

Kita akan bahas:

1️⃣ IP Address
2️⃣ Port
3️⃣ DNS
4️⃣ HTTP / HTTPS
5️⃣ TCP / UDP
6️⃣ OSI Layer Model

1️⃣ IP Address
Apa itu IP Address

IP Address (Internet Protocol Address) adalah alamat unik yang digunakan untuk mengidentifikasi perangkat dalam jaringan.

Contoh:

192.168.1.10
8.8.8.8
142.250.190.14

Bayangkan seperti alamat rumah.

IP = alamat rumah
internet = jalan raya
data = kendaraan

Tanpa IP address, perangkat tidak tahu ke mana harus mengirim data.

Contoh Komunikasi IP

Misalnya laptop membuka Google.

Laptop IP: 192.168.1.10
Google IP: 142.250.190.14

Komunikasi:

192.168.1.10 → 142.250.190.14

Artinya:

Laptop mengirim request ke server Google
Jenis IP Address
Private IP

Digunakan di jaringan internal.

Contoh:

192.168.x.x
10.x.x.x
172.16.x.x

Biasanya digunakan di:

rumah

kantor

LAN

Public IP

Digunakan di internet.

Contoh:

8.8.8.8
1.1.1.1
142.250.190.14
Dalam SOC Investigation

SOC menggunakan IP untuk:

mencari sumber serangan

mencari lokasi attacker

memeriksa reputasi IP

Contoh log:

Source IP: 185.220.101.45
Destination IP: 192.168.1.10

Analisis:

IP external mencoba akses server internal

Kemungkinan:

brute force
port scanning
2️⃣ Port
Apa itu Port

Port adalah jalur komunikasi untuk layanan tertentu di suatu IP.

Jika IP adalah rumah, maka:

Port = pintu rumah

Contoh:

IP: 192.168.1.10

Port:

22   SSH
80   HTTP
443  HTTPS
21   FTP
25   SMTP
53   DNS
Contoh Komunikasi
192.168.1.5 → 192.168.1.10:22

Artinya:

Client mencoba koneksi SSH ke server
Dalam SOC

SOC sering menganalisis:

IP
Port
Protocol

Contoh log:

Connection from 203.0.113.10
to port 22

Jika berulang:

Kemungkinan:

SSH brute force
3️⃣ DNS
Apa itu DNS

DNS (Domain Name System) adalah sistem yang mengubah nama domain menjadi IP address.

Contoh:

google.com → 142.250.190.14

Karena manusia lebih mudah mengingat domain daripada IP.

Cara Kerja DNS

Misalnya user membuka:

google.com

Prosesnya:

1. Browser mengirim DNS request
2. DNS server mencari IP
3. DNS server mengirim IP
4. Browser koneksi ke server

Diagram sederhana:

User
 ↓
DNS request
 ↓
DNS server
 ↓
IP address
 ↓
Website
DNS dalam SOC

SOC sering melihat log seperti ini:

DNS query: suspicious-domain.ru

Jika domain tersebut adalah domain malware:

⚠️ kemungkinan:

malware communication

Biasanya malware akan:

DNS query → connect C2 server
4️⃣ HTTP

HTTP adalah protocol komunikasi web.

Port:

80

Digunakan untuk:

website
API
web application
Cara Kerja HTTP

Client mengirim request.

Contoh:

GET /login HTTP/1.1
Host: example.com

Server mengirim response.

Contoh:

HTTP/1.1 200 OK
Serangan yang sering muncul di HTTP

SOC sering melihat:

SQL Injection
Directory Traversal
Web scanning

Contoh request mencurigakan:

GET /login.php?id=1' OR '1'='1

Ini indikasi:

SQL injection
5️⃣ HTTPS

HTTPS adalah HTTP yang dienkripsi menggunakan TLS.

Port:

443

Keuntungan:

data terenkripsi
lebih aman
Apa yang bisa dilihat SOC

Walaupun terenkripsi, SOC masih bisa melihat:

IP
domain
port
traffic size
certificate

Contoh log:

192.168.1.10 → malicious-domain.ru:443

Jika domain berbahaya:

⚠️ kemungkinan:

malware communication
6️⃣ TCP

TCP adalah protocol yang reliable dan connection oriented.

Artinya koneksi harus dibuat terlebih dahulu.

Contoh protocol TCP:

HTTP
HTTPS
SSH
FTP
TCP 3-way handshake

Sebelum komunikasi terjadi:

Client → SYN
Server → SYN-ACK
Client → ACK

Diagram:

Client     Server
  SYN  →
       ← SYN-ACK
  ACK  →

Setelah itu komunikasi dimulai.

7️⃣ UDP

UDP adalah protocol connectionless.

Tidak ada handshake.

Contoh protocol UDP:

DNS
VoIP
Streaming

Keuntungan:

lebih cepat

Kerugian:

tidak reliable
8️⃣ OSI Layer Model

OSI Model menjelaskan bagaimana data bergerak dalam jaringan.

Ada 7 layer.

Layer	Nama
7	Application
6	Presentation
5	Session
4	Transport
3	Network
2	Data Link
1	Physical
Layer yang sering digunakan di SOC

SOC biasanya fokus pada 3 layer ini.

Layer 7 — Application

Contoh:

HTTP
HTTPS
DNS
SMTP
Layer 4 — Transport

Protocol:

TCP
UDP
Layer 3 — Network

Protocol:

IP
Contoh Analisis SOC Berdasarkan Network
Kasus 1 — Port Scanning

Log:

203.0.113.5 → port 21
203.0.113.5 → port 22
203.0.113.5 → port 80
203.0.113.5 → port 443

Analisis:

Satu IP mencoba banyak port.

Kemungkinan:

port scanning
Kasus 2 — DNS Malware

Log:

DNS query: bad-domain.ru

Analisis:

Endpoint mengakses domain berbahaya.

Kemungkinan:

malware C2 communication
Kasus 3 — Brute Force SSH

Log:

Failed password for root from 185.220.101.45

Analisis:

Login gagal berulang.

Kemungkinan:

brute force attack
Cara Menjawab Saat Interview SOC

Gunakan framework ini.

1️⃣ Identifikasi

Dari log tersebut terlihat adanya aktivitas mencurigakan.

2️⃣ Dugaan serangan

Hal ini kemungkinan merupakan brute force attack.

3️⃣ Investigasi

Saya akan memeriksa IP address, port, dan aktivitas log lainnya.

4️⃣ Tindakan

Jika aktivitas tersebut mencurigakan, saya akan melakukan eskalasi.

# Ringkasan Super Cepat (Untuk Interview)

IP
alamat perangkat

Port
jalur layanan

DNS
domain → IP

HTTP
web communication
port 80

HTTPS
web encrypted
port 443

TCP
reliable
handshake

UDP
lebih cepat
tanpa handshake

# OSI Layer penting

Application
Transport
Network





# beberapa istilah di soc 

1. Ceritakan bagaimana cara kerja SOC Analyst Level 1

Jawaban

SOC Analyst Level 1 bertugas melakukan monitoring alert keamanan dari SIEM atau security tools lainnya.
Tugas utamanya adalah melakukan triage alert, melakukan analisis awal terhadap log, menentukan apakah alert tersebut true positive atau false positive, dan melakukan eskalasi ke tim SOC Level 2 jika diperlukan.

2. Apa itu SIEM dan kenapa penting?

Jawaban

SIEM adalah sistem yang digunakan untuk mengumpulkan, mengkorelasikan, dan menganalisis log dari berbagai sumber seperti server, firewall, endpoint, dan aplikasi untuk mendeteksi aktivitas mencurigakan atau ancaman keamanan.

3. Apa perbedaan antara alert dan incident?

Jawaban

Alert adalah notifikasi dari sistem keamanan yang menunjukkan aktivitas mencurigakan.
Sedangkan incident adalah kejadian keamanan yang telah dikonfirmasi sebagai ancaman atau pelanggaran keamanan.

4. Jika kamu menerima alert brute force, apa yang kamu lakukan?

Jawaban

Saya akan memeriksa log authentication untuk melihat jumlah login gagal, IP address yang melakukan percobaan login, serta waktu terjadinya aktivitas tersebut.
Jika terlihat banyak login gagal dari satu IP dalam waktu singkat, maka kemungkinan besar terjadi brute force attack dan saya akan melakukan eskalasi atau memblokir IP tersebut sesuai prosedur.

5. Apa itu false positive?

Jawaban

False positive adalah alert yang dihasilkan oleh sistem keamanan tetapi sebenarnya bukan aktivitas berbahaya.

6. Apa itu log analysis?

Jawaban

Log analysis adalah proses menganalisis log dari sistem atau perangkat jaringan untuk mendeteksi aktivitas mencurigakan, kesalahan sistem, atau indikasi serangan.

7. Apa itu MITRE ATT&CK framework?

Jawaban

MITRE ATT&CK adalah framework yang mendokumentasikan taktik dan teknik yang digunakan oleh attacker berdasarkan data serangan dunia nyata.

8. Apa perbedaan IDS dan IPS?

Jawaban

IDS hanya mendeteksi serangan dan menghasilkan alert, sedangkan IPS dapat mendeteksi sekaligus memblokir serangan secara otomatis.

9. Bagaimana cara mendeteksi malware di jaringan?

Jawaban

Malware dapat dideteksi melalui aktivitas jaringan mencurigakan, signature antivirus, perilaku file yang tidak normal, atau komunikasi dengan domain command and control.

10. Apa itu IOC?

Jawaban

IOC adalah indikator yang menunjukkan kemungkinan adanya kompromi pada sistem seperti IP berbahaya, hash malware, domain malicious, atau file mencurigakan.

11. Jika ada login berhasil setelah banyak login gagal, apa indikasinya?

Jawaban

Ini bisa menjadi indikasi brute force attack yang berhasil menebak password.

12. Apa itu phishing?

Jawaban

Phishing adalah teknik social engineering yang digunakan attacker untuk menipu korban agar memberikan informasi sensitif melalui email atau website palsu.

13. Apa itu malware?

Jawaban

Malware adalah software berbahaya yang dirancang untuk merusak sistem atau mencuri data.

14. Apa yang dimaksud dengan CIA Triad?

Jawaban

CIA Triad terdiri dari Confidentiality, Integrity, dan Availability yang merupakan prinsip dasar keamanan informasi.

15. Jika kamu menemukan IP address mencurigakan, apa yang kamu lakukan?

Jawaban

Saya akan melakukan pengecekan reputasi IP menggunakan threat intelligence tools seperti VirusTotal atau AbuseIPDB untuk mengetahui apakah IP tersebut pernah terlibat dalam aktivitas berbahaya.

16. Apa itu port scanning?

Jawaban

Port scanning adalah teknik yang digunakan attacker untuk mencari port terbuka pada sistem target untuk menemukan layanan yang bisa diserang.

17. Apa itu firewall?

Jawaban

Firewall adalah sistem keamanan jaringan yang digunakan untuk mengontrol lalu lintas jaringan berdasarkan aturan keamanan.

18. Apa itu SIEM correlation rule?

Jawaban

Correlation rule digunakan dalam SIEM untuk menghubungkan berbagai event log sehingga dapat mendeteksi pola serangan yang kompleks.

19. Bagaimana cara mendeteksi brute force di Linux?

Jawaban

Dengan melihat log authentication seperti /var/log/auth.log untuk melihat banyak login gagal dari IP yang sama.

20. Apa itu command and control (C2)?

Jawaban

Command and Control adalah server yang digunakan attacker untuk berkomunikasi dengan malware yang telah menginfeksi sistem korban.

21. Apa itu ransomware?

Jawaban

Ransomware adalah malware yang mengenkripsi file korban dan meminta tebusan untuk mengembalikan akses.

22. Apa yang kamu lakukan jika endpoint terinfeksi malware?

Jawaban

Saya akan mengisolasi endpoint dari jaringan untuk mencegah penyebaran malware, kemudian melakukan analisis dan pembersihan sistem.

23. Apa itu threat intelligence?

Jawaban

Threat intelligence adalah informasi tentang ancaman keamanan yang digunakan untuk membantu organisasi mendeteksi dan mencegah serangan.

24. Apa itu privilege escalation?

Jawaban

Privilege escalation adalah teknik yang digunakan attacker untuk mendapatkan hak akses yang lebih tinggi pada sistem.

25. Apa itu lateral movement?

Jawaban

Lateral movement adalah teknik attacker untuk berpindah dari satu sistem ke sistem lain dalam jaringan setelah berhasil masuk.

26. Apa itu vulnerability?

Jawaban

Vulnerability adalah kelemahan pada sistem yang dapat dimanfaatkan oleh attacker untuk melakukan serangan.

27. Apa itu patch management?

Jawaban

Patch management adalah proses memperbarui software untuk memperbaiki vulnerability atau bug keamanan.

28. Apa itu SOC playbook?

Jawaban

Playbook adalah panduan langkah-langkah yang harus dilakukan oleh SOC analyst saat menangani jenis incident tertentu.

29. Apa yang kamu lakukan jika SIEM menghasilkan banyak alert?

Jawaban

Saya akan memprioritaskan alert berdasarkan tingkat severity dan potensi dampaknya terhadap sistem organisasi.

30. Kenapa kami harus memilih kamu sebagai SOC Analyst?

Jawaban yang bagus untuk kamu

Saya memiliki ketertarikan yang besar dalam bidang cybersecurity khususnya di SOC analyst. Saat ini saya sedang mempelajari SOC analyst path di TryHackMe dan juga telah belajar tentang log analysis, threat detection, dan dasar-dasar incident response. Saya juga memiliki semangat belajar yang tinggi dan siap berkembang dalam lingkungan SOC.
bukan hanya hafalan

