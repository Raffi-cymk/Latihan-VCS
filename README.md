# Latihan-VCS

Langkah-langkah Membuat Latihan VCS dengan Git

1. Instalasi Git

Untuk memulai menggunakan Git, pertama-tama, kita perlu menginstal Git di komputer kita.

Untuk pengguna Windows, bisa diunduh di Git for Windows.

Untuk pengguna macOS atau Linux, dapat diinstal menggunakan package manager (Homebrew untuk macOS, apt untuk Linux).


2. Konfigurasi Git

Setelah Git terinstal, perlu dilakukan konfigurasi awal seperti nama pengguna dan email yang akan disimpan dalam commit history.

git config --global user.name "Nama Anda"
git config --global user.email "email@example.com"

3. Membuat Repositori Git Baru

Repositori adalah tempat semua berkas proyek dan riwayat perubahan disimpan. Anda bisa membuat repositori Git baru di folder proyek lokal dengan menjalankan perintah:

git init

Ini akan menginisialisasi repositori Git di folder tersebut.

4. Menambahkan Berkas ke Repositori

Buat beberapa berkas di dalam folder proyek Anda, misalnya file .txt, .html, atau kode program. Setelah berkas dibuat, tambahkan berkas tersebut ke staging area dengan perintah:

git add nama_berkas

Untuk menambahkan semua berkas sekaligus, gunakan:

git add .

5. Commit Perubahan

Setelah berkas ditambahkan ke staging area, commit perubahan ke repositori dengan memberikan pesan deskriptif mengenai apa yang diubah.

git commit -m "Pesan commit"

Commit merupakan titik checkpoint yang menyimpan status proyek pada waktu tertentu.

6. Membuat Repositori di GitHub (Opsional)

Untuk menyimpan repositori secara remote (misalnya di GitHub), lakukan langkah berikut:

Buat akun GitHub di GitHub.

Buat repositori baru di GitHub.

Setelah repositori GitHub dibuat, sambungkan repositori lokal dengan remote repository menggunakan perintah:


git remote add origin https://github.com/username/nama-repo.git

Kirim (push) commit yang ada di lokal ke repositori GitHub:


git push -u origin master

7. Menarik Perubahan dari Remote Repository (Pull)

Jika Anda atau rekan tim melakukan perubahan di repositori remote, Anda dapat memperbarui repositori lokal dengan perintah:

git pull origin master

Ini akan menarik perubahan terbaru dari repositori GitHub.

8. Membuat Branch dan Merge

Git memungkinkan Anda bekerja di cabang (branch) yang berbeda untuk mengembangkan fitur baru tanpa mengganggu branch utama.

Buat branch baru:


git checkout -b nama-branch

Setelah selesai, lakukan commit seperti biasa di branch tersebut.

Untuk menggabungkan branch ke dalam branch utama (master/main), pindah ke branch utama dan lakukan merge:


git checkout master
git merge nama-branch

9. Menyelesaikan Konflik Merge (Jika Ada)

Kadang-kadang, merge akan menghasilkan konflik jika perubahan yang dibuat di branch lain berbenturan dengan perubahan yang ada. Git akan memberi tahu konflik mana yang harus diselesaikan, dan Anda harus memperbaiki berkas tersebut secara manual sebelum melakukan commit lagi.

10. Melihat Riwayat Perubahan

Untuk melihat riwayat commit yang pernah dibuat, gunakan perintah:

git log

11. Mengabaikan Berkas dengan .gitignore

Anda bisa membuat berkas .gitignore untuk memberitahu Git agar mengabaikan berkas-berkas tertentu yang tidak perlu dilacak, misalnya berkas konfigurasi lokal atau cache. Contoh isi berkas .gitignore:

node_modules/
*.log
