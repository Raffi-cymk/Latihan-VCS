# Latihan-VCS
Langkah-langkah Membuat Latihan VCS dengan Git

Langkah 1 — Membuat Akun Git
Yang harus dilakukan pertama adalah membuat akun Git. Saat ini, layanan git yang paling populer digunakan adalah gitlab.com atau github.com.

Langkah 2— Instalasi Git
Yang harus dilakukan selanjutnya adalah melakukan instalasi Git pada device. Bisa dimulai dengan googling “install git [device’s os]” contohnya, “install git windows” atau bisa langsung menuju website https://git-scm.com/download/ dan download installer. Setelah selesai di-download, buka file untuk melakukan instalasi. Ikuti hingga seluruh proses instalasi selesai (klik next > next > finish). Perlu diperhatikan bahwa selama proses tersebut terdapat beberapa pilihan yang harus dipilih agar Git dapat dijalankan pada terminal.

Selanjutnya, jika proses instalasi sudah selesai, buka terminal dan jalankan perintah:

git --version
Jika proses instalasi berhasil, maka akan ditampilkan versi dari Git yang sudah diinstal. Berikut contohnya,

![17293192729114270585256060567297](https://github.com/user-attachments/assets/ac5502b8-114f-4515-804e-dcab5ca0d5a1)

Langkah 3— Konfigurasi Awal
Sebelum memulai menggunakan Git, yang perlu dilakukan adalah konfigurasi dengan email dan nama sesuai dengan yang sebelumnya sudah didaftarkan saat membuat akun Git dengan menjalankan perintah berikut:

git config --global user.name "Nama Anda"
git config --global user.email "username@email.com"
Setelah itu jalankan perintah berikut untuk memeriksa apakah konfigurasi berhasil:

git config --list

Langkah 4— Menggunakan Git!
Akhirnya, tiba juga pada tahap di mana sekarang saatnya menggunakan Git! Pada bagian ini, saya akan menjelaskan perintah-perintah yang sering digunakan pada Git.

Inisiasi
Untuk mengintegrasikan suatu folder atau repositori lokal dengan Git caranya adalah dengan membuat folder baru atau buka folder (direktori) lokal yang ingin diintegrasikan lalu jalankan perintah ini pada terminal:

git init
Jika sudah memiliki repositori sebelumnya dan ingin mengambilnya atau membuat salinan dari repositori tersebut, caranya adalah dengan menjalankan perintah berikut:

git clone <link_repository>
Untuk link sendiri bisa didapatkan dengan buka repositori yang ingin disalin pada Gitlab/Github, dan salin link-nya.

![17293195176215509082309936317955](https://github.com/user-attachments/assets/96af1204-e115-4406-b1f3-6230fc030991)

Alur Kerja (Workflow) Git
Pada Git, terdapat alur kerja atau workflow yang efektif dan efisien. Repositori tersebut dibagi menjadi tiga bagian pokok yang disebut dengan “trees”.

![17293196849405366814385390578577](https://github.com/user-attachments/assets/3494a39e-6d16-4143-961e-61f17329d160)


