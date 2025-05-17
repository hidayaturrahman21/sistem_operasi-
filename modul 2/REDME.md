# Command Line: Manajemen Proses Dan Manajemen Memory

Dokumentasi ini menjelaskan cara menggunakan command line (terminal) di Linux (Ubuntu) untuk memantau penggunaan CPU dan memori, menjalankan skrip, serta melakukan perintah manajemen sistem seperti restart dan shutdown.

### Cek Spesifikasi Sistem di Windows
1. Tekan `Windows + E`.
2. Klik kanan pada “This PC”.
3. Pilih **Properties**.
   - Komputer: Dell OptiPlex 7470 AIO
   - OS: Windows 11 Pro versi 22H2
   - CPU: Intel Core i7-9700
   - RAM: 8 GB
   - Arsitektur: 64-bit

### Cek Memory, Core, dan Thread di Windows
1. Tekan `Ctrl + Shift + Esc` untuk membuka Task Manager.
2. Klik ikon tiga garis (menu) di kiri atas.
3. Pilih **Performance**:
   - **Memory**: Penggunaan RAM 82%, tersedia 3.0 GB, kecepatan 2667 MHz.
   - **CPU**: Penggunaan rendah (3%), kecepatan naik hingga 4.58 GHz, 8 core, 8 thread, virtualisasi aktif.

### Monitoring Sistem di Linux

- **Perintah `free -h`**:
  - RAM total: 3.8 GiB, digunakan: 1.0 GiB, bebas: 2.2 GiB.
  - Swap: 3.8 GiB (tidak digunakan).

- **Perintah `htop`**:
  - CPU dan memori rendah, swap tidak digunakan.
  - Proses utama: `gnome-shell`, `systemd`.

- **Perintah `top` dan lainnya**:
  - RAM 4GB, swap tidak digunakan.
  - Prosesor: Intel Core i5-8365U, 4 core, 8 thread.
  - Fitur: Virtualisasi VT-x, instruksi SIMD (SSE, AVX, AVX2).
  - Cache: L1 128KB, L2 1MB, L3 24MB.

- **Perintah `vmstat` dan `ps`**:
  - RAM masih cukup, aktivitas swap tidak terjadi.
  - Proses ringan, penggunaan memori dan CPU rendah.

### Eksekusi Script di Terminal Ubuntu
- Membuat direktori dan file Python/shell.
- Mengatur izin dengan `chmod +x`.
- Menjalankan dengan `./nama_file.sh`.

### Perintah Restart dan Shutdown di Ubuntu

- **Restart langsung**:
  ```bash
  sudo reboot
  ```

- **Shutdown langsung**:
  ```bash
  sudo shutdown now
  ```

- **Restart pada waktu tertentu**:
  ```bash
  sudo shutdown -r 07:07
  ```

- **Shutdown pada waktu tertentu**:
  ```bash
  sudo shutdown -h 04:10
  ```
- Gunakan `shutdown -c` untuk membatalkan jadwal restart/shutdown.

---

