### 2. *Mengupdate Repositori Utama dengan Perubahan dari Repositori Fork Lokal Anda*

Jika Anda telah membuat perubahan di repositori fork lokal Anda dan ingin mengupdate repositori utama:

#### A. *Push Perubahan ke Repositori Fork di GitHub*

1. *Cek Status Perubahan:*
   - Pastikan tidak ada perubahan yang belum di-commit:
     sh
     git status
     

2. *Tambahkan dan Commit Perubahan:*
   - Tambahkan file yang telah diubah atau ditambahkan:
     sh
     git add .
     
   - Commit perubahan dengan pesan yang jelas:
     sh
     git commit -m "Deskripsi perubahan"
     

3. *Push Perubahan ke Repositori Fork di GitHub:*
   - Kirim perubahan ke repositori fork Anda di GitHub:
     sh
     git push origin main
     

#### B. *Buat Pull Request dari Repositori Fork ke Repositori Utama*

4. *Buka GitHub dan Pergi ke Repositori Fork Anda:*
   - Kunjungi repositori fork Anda di GitHub.

5. *Buat Pull Request:*
   - Di halaman repositori fork Anda, klik tab *"Pull requests"*.
   - Klik *"New pull request"*.
   - Pilih *"compare across forks"* jika tidak otomatis terdeteksi.
   - Pilih repositori utama sebagai *base repository* dan branch dari fork Anda sebagai *head repository*.
   - Pilih branch yang berisi perubahan Anda di bagian *"compare"*.
   - Klik *"Create pull request"* dan isi deskripsi yang relevan mengenai perubahan Anda.

6. *Review dan Submit Pull Request:*
   - Tulis deskripsi yang jelas tentang perubahan Anda.
   - Klik *"Create pull request"* untuk mengirimkan pull request ke repositori utama.

7. *Tunggu Review dan Merge:*
   - Admin repositori utama akan meninjau pull request Anda.
   - Mereka mungkin meminta perubahan atau memberikan umpan balik.
   - Setelah disetujui, pull request akan digabungkan ke repositori utama.