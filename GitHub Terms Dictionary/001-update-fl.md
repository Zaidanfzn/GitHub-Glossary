### 1. *Mengupdate Repositori Fork Lokal Anda dengan Perubahan dari Repositori Utama*

Ketika ada perubahan di repositori utama yang Anda butuhkan di repositori fork lokal Anda, berikut adalah langkah-langkahnya:

#### A. *Menambahkan Repositori Utama sebagai Remote di Repositori Fork Lokal*

1. *Tambahkan Remote upstream:*
   - Buka Git Bash atau terminal di direktori repositori fork lokal Anda.
   - Tambahkan repositori utama sebagai remote upstream:
     sh
     git remote add upstream <URL-repositori-utama>
     
   - Misalnya, jika URL repositori utama adalah https://github.com/owner/repo.git, perintahnya akan menjadi:
     sh
     git remote add upstream https://github.com/owner/repo.git
     

#### B. *Update Repositori Fork Lokal dengan Perubahan dari Repositori Utama*

2. *Ambil Perubahan dari Remote upstream:*
   - Ambil perubahan terbaru dari repositori utama:
     sh
     git fetch upstream
     

3. *Periksa Perubahan yang Ditemukan:*
   - Lihat perbedaan antara branch lokal Anda dan branch di repositori utama:
     sh
     git diff main upstream/main
     

4. *Gabungkan Perubahan dari upstream ke Branch Lokal Anda:*
   - Gabungkan perubahan dari branch utama repositori utama ke branch lokal Anda:
     sh
     git merge upstream/main
     
   - Jika Anda berada di branch lain, pastikan untuk pindah ke branch yang sesuai sebelum melakukan merge.

5. *Tanggulangi Konflik (Jika Ada):*
   - Jika ada konflik, Anda perlu menyelesaikannya secara manual di editor Anda, kemudian lakukan commit:
     sh
     git add <file-yang-diperbaiki>
     git commit -m "Resolve merge conflicts"
     

6. *Push Perubahan ke Repositori Fork di GitHub (Opsional):*
   - Setelah menggabungkan perubahan, jika Anda ingin memperbarui repositori fork di GitHub, lakukan push:
     sh
     git push origin main