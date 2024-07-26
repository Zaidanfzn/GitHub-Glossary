### **1. Membuat Repositori Menggunakan GitHub CLI**

#### *Langkah 1: Instal GitHub CLI*

1. **Unduh GitHub CLI**
   - Buka [situs GitHub CLI](https://cli.github.com/) dan unduh installer sesuai dengan sistem operasi Anda.

2. **Instal GitHub CLI**
   - Jalankan installer yang sudah diunduh dan ikuti petunjuk instalasi.

#### *Langkah 2: Verifikasi Instalasi*

1. **Buka Terminal**
   - Buka terminal atau command prompt.

2. **Cek Versi GitHub CLI**
   - Jalankan perintah berikut untuk memastikan GitHub CLI terinstal dengan benar:
     ```bash
     gh --version
     ```
   - Jika GitHub CLI terinstal dengan benar, Anda akan melihat informasi versi.
   - Jika keluar perintah berikut :
     ```bash
     bash: gh: command not found
     ```
     Maka Anda harus menambahkan GitHub CLI ke PATH di Git Bash. Tutorial terdapat pada file `002-add-github-cli.md`.

#### *Langkah 3: Login ke GitHub*

1. **Login ke GitHub Menggunakan GitHub CLI**
   - Jalankan perintah berikut untuk login ke akun GitHub Anda:
     ```bash
     gh auth login
     ```
   - Ikuti petunjuk yang muncul di terminal untuk menyelesaikan proses login.

#### *Langkah 4: Membuat Repositori Privat atau Public dan Push*

1. **Inisialisasi Git di Folder Lokal**
   - Buka terminal atau command prompt.
   - Arahkan ke folder lokal yang ingin Anda dorong ke GitHub.
   - Jalankan perintah berikut untuk menginisialisasi Git:
     ```bash
     git init
     git add .
     git commit -m "Initial commit"
     ```

2. **Buat Repositori Baru di GitHub (Privat) Menggunakan GitHub CLI**
   - Jalankan perintah berikut untuk membuat repositori baru di GitHub dan menjadikannya privat:
     ```bash
     gh repo create REPOSITORY_NAME --private --source=. --remote=origin
     ```
   - Gantilah `private` dengan `public` jika ingin membuat repositori public.
   - Gantilah `REPOSITORY_NAME` dengan nama repositori yang Anda inginkan.

3. **Push Perubahan ke GitHub**
   - Jalankan perintah berikut untuk mendorong perubahan ke repositori baru:
     ```bash
     git push -u origin master
     ```