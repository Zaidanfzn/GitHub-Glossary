### **2. Menambahkan GitHub CLI ke PATH di Git Bash**

1. **Temukan Lokasi Instalasi GitHub CLI**
   - Buka **PowerShell** dan jalankan perintah berikut untuk menemukan lokasi instalasi `gh`:
     ```powershell
     Get-Command gh
     ```
   - Anda akan melihat output yang menunjukkan path ke executable `gh`. Catat path tersebut, misalnya:
     ```
     C:\Program Files\GitHub CLI\gh.exe
     ```

2. **Tambahkan Lokasi Instalasi ke PATH di Git Bash**
   - Buka **Git Bash**.
   - Buka file `.bashrc` atau `.bash_profile` di editor teks menggunakan perintah berikut:
     ```bash
     nano ~/.bashrc
     ```
     atau
     ```bash
     nano ~/.bash_profile
     ```
   - Tambahkan baris berikut di akhir file `.bashrc` atau `.bash_profile`, ganti `C:\Program Files\GitHub CLI\` dengan path yang Anda catat dari langkah sebelumnya. Penting untuk mengubah backslashes (`\`) menjadi slashes (`/`) dan menambahkan `/c/` di awal path:
     ```bash
     export PATH=$PATH:/c/Program\ Files/GitHub\ CLI/
     ```
   - Simpan file dan keluar dari editor (di nano, tekan `CTRL + X`, lalu `Y`, lalu `Enter`).

3. **Reload .bashrc atau .bash_profile**
   - Jalankan perintah berikut untuk memuat ulang `.bashrc` atau `.bash_profile`:
     ```bash
     source ~/.bashrc
     ```
     atau
     ```bash
     source ~/.bash_profile
     ```

4. **Verifikasi Instalasi**
   - Coba jalankan perintah berikut di Git Bash untuk memastikan `gh` sekarang dapat dikenali:
     ```bash
     gh --version
     ```
   - Jika berhasil, Anda akan melihat versi GitHub CLI yang terinstal.

### **Alternatif: Menambahkan PATH di Windows Environment Variables**

Jika langkah-langkah di atas tidak berhasil, Anda bisa menambahkan path GitHub CLI ke environment variables Windows:

1. **Buka System Properties**
   - Buka "Control Panel" > "System and Security" > "System" > "Advanced system settings".

2. **Buka Environment Variables**
   - Klik tombol "Environment Variables" di bagian bawah jendela.

3. **Edit System PATH**
   - Di bagian "System variables", temukan variabel `Path`, lalu klik "Edit".
   - Tambahkan path ke direktori GitHub CLI, misalnya:
     ```
     C:\Program Files\GitHub CLI\
     ```
   - Klik "OK" untuk menyimpan perubahan.

4. **Restart Git Bash**
   - Tutup Git Bash dan buka kembali, lalu coba jalankan perintah:
     ```bash
     gh --version
     ```