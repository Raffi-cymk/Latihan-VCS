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

---

1. Direktori Kerja (Working directory)
Bagian ini menyimpan berkas aktual dari repositori lokal. Semua perubahan yang dilakukan pada berkas di lokal setelah inisiasi awal atau commit terakhir akan tersimpan pada bagian ini. Bisa dijalankan perintah berikut untuk melihat file apa saja yang terdapat pada bagian ini:

git status
Selanjutnya setelah dijalankan, bisa dilihat keluarannya adalah seperti ini,

![17293200312553123736227895075493](https://github.com/user-attachments/assets/a1b63432-e8de-4c0b-b1b9-d084f6158e54)

Bisa dilihat pada potongan gambar di atas, perubahan pada files di repositori lokal tersimpan dan bisa dilihat files yang mengalami perubahan direpresentasikan dengan warna merah. Semua files tersebut masih berada pada fase working directory. Setelah menyelesaikan perubahan pada working directory, untuk menambahkan atau memindahkan files dari working directory ke fase index (stage) adalah dengan menjalankan perintah berikut:

git add <nama_file_yang_ingin_ditambahkan>

Jika ingin memindahkan semua files, maka cukup jalankan perintah berikut:

git add .
Jika ingin membatalkan penambahan atau pemindahan file, maka dapat dijalankan perintah berikut:

git rm <nama_file_yang_batal_ditambahkan>

---

2. Index (Stage)

File yang sebelumnya sudah di-add, kini sudah tersimpan pada fase ini dan siap untuk disimpan pada suatu commit. Jika dilakukan kembali perubahan isi (kode) dari file yang sudah berada di tahap ini, maka ia akan kembali lagi ke fase working directory dan untuk memindahkan file tersebut ke fase ini tentunya perlu dijalankan git add lagi untuk file tersebut. Jika sudah yakin, sekarang adalah saatnya memindahkan file dari fase ini ke fase HEAD dengan menjalankan perintah:

git commit -m "Isi dengan pesan komit"

Saat komit, tambahkan dengan nama atau pesan komit yang nantinya akan menandakan perubahan dari file-file yang dilakukan. Sebagai contoh, misal perubahan yang saya lakukan adalah mengganti warna navigation bar, maka dapat dijalankan perintah:

git commit -m "[REFACTOR] changed navbar color, from red to blue"
Pemberian pesan komit yang jelas akan memudahkan tim dalam bekerja kolaboratif untuk memahami perubahan apa yang dilakukan pada kode dan juga akan memudahkan saat nantinya dihadapkan dengan keadaan ingin mengembalikan berkas kode ke suatu versi kode tertentu.

Bila perintah ini telah dijalankan, file akan dikomit ke HEAD, namun belum terkitim ke remote repository.

---

3. HEAD

Saat ini, perubahan sudah tersimpan di HEAD. Jika sudah yakin untuk mengirim perubahan ke repositori asli atau remote repository (repository yang ada di Gitlab/Github), jalankan perintah:

git push origin master
Master merupakan nama default untuk branch utama (akan ada penjelasan mengenai branching juga di bawah), ubah master sesuai dengan nama branch yang kalian tuju di mana perubahan tersebut ingin anda simpan di branch tersebut. Sebagai contoh misal terdapat branch bernama fitur-login, dan perubahan yang dilakukan terkait fitur tersebut dan saya ingin menyimpan perubahan ke branch tersebut, maka dapat dijalankan perintah:

git push origin fitur-login

Jika repositori yang ada saat ini belum di-clone dan ingin dihubungkan dengan remote server, maka jalankan perintah:

git remote add origin <alamat-server>
Setelah menjalankan git push, maka saat ini perubahan sudah masuk ke remote repository.

Branching
Dalam suatu repositori, dapat dibuat banyak branch sesuai dengan kebutuhan, setelah selesai, dapat dilakukan pula menggabungkan branch-branch dengan cabang utama.

![17293204292924849634652955443495](https://github.com/user-attachments/assets/84fafc07-b7ca-4692-867a-87060d8940e2)

Cara membuat branch sendiri adalah, jika ingin membuat branch baru dan tetap berada di branch saat ini, maka dapat dijalankan perintah:

git branch <nama_branch_baru>
Selain itu, jika ingin membuat branch baru dan sekaligus pindah ke branch baru tersebut, dapat dijalankan perintah:

git checkout -b <nama_branch_baru>

Untuk melihat daftar branch yang terdapat di repository, jalankan perintah:

git branch
Untuk pindah dari satu branch ke branch lainnya, jalankan perintah:

git checkout <nama_branch_dituju>
Perlu dipastikan saat berpindah dari satu branch ke branch lainnya tidak terdapat perubahan yang belum disimpan.

Jika ingin menghapus suatu branch, jalankan perintah:

git branch -d <nama_branch_yang_ingin_dihapus>
Untuk membuat branch dapat digunakan oleh orang lain, jangan lupa untuk mengirimkan hasil kerjaan dan branch tersebut ke remote repository dengan menggunakan perintah:

git push origin <nama_branch_yang_dibuat>

---

Update & Merge
Selanjutnya, jika ingin melakukan update direktori lokal dengan versi paling baru yang terdapat di remote repository (misal ingin mengambil commit pekerjaan teman yang tentunya belum ada di repositori lokal kita), jalankan perintah:

git pull <nama_remote> <nama_branch>
Jika ingin menggabungkan suatu branch dengan branch yang saat ini sudah aktif (letak branch anda sekarang), jalankan perintah:

git merge <nama_branch_yang_ingin_dimerge>

Setelah melakukan pull atau merge, git akan selalu mencoba menangani konflik sendiri, namun seringkali penanganan otomatis ini gagal. Jika terjadi kegagalan pull atau merge karena konflik, maka harus dilakukan resolve conflict secara manual yaitu dengan menghapus conflict.

Selain menggunakan git merge untuk menggabungkan satu branch dengan yang lainnya, terdapat pula git rebash. Git merge akan menghasilkan kombinasi komit-komit, sedangkan git rebash akan menggabungkan perubahan dari suatu branch secara satu per satu secara berurutan ke commit terakhir dari branch yang dituju. Berikut ilustrasinya (dalam kasus ini misal branch saat ini adalah feature dan branch yang dituju adalah master),

![17293207899562912805046126866987](https://github.com/user-attachments/assets/a1629c3b-c8a2-4e44-8f00-ee7ee4aed0a3)

Untuk menjalankan rebase, jalankan perintah:

git rebase <nama_branch_yang_dituju>
