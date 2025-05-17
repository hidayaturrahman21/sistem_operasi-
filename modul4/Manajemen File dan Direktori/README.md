# 📁 Command Line : Manajemen File dan Direktori

Dokumentasi ini menjelaskan cara menggunakan command line (terminal) di Linux (Ubuntu) untuk membuat, mengelola, memindahkan, dan menghapus file serta direktori (folder), termasuk pengaturan izin dan kepemilikan.

## 1. Membuat dan Mengelola File
### a. Membuat Directory
```bash
mkdir Modul4
```

### b. Membuat File Kosong
```bash
touch file1.txt
```

### c. Membuat Folder Baru
```bash
mkdir folderbaru
```

### d. Menyalin File ke Folder
```bash
cp file1.txt folderbaru
cd folderbaru
```

### e. Menghapus File dan Folder
```bash
rm filesampah.txt       # Menghapus file
rmdir foldersampah      # Menghapus folder kosong
```

### f. Mengubah Nama File
```bash
mv file1.txt file2.txt
```

### g. Memindahkan File ke Folder yang Sama
```bash
mv file2.txt folderbaru
```

### h. Memindahkan File ke Direktori Lain
```bash
mv file2.txt /home/valskie/Modul4
```
<br>

## 2. Mengatur Izin (Permissions)

### a. Mengubah dengan Simbol
```bash
chmod u+x file2.txt      # Tambah izin eksekusi untuk user
chmod g+x file2.txt      # Tambah izin eksekusi untuk grup
chmod o+w file2.txt      # Tambah izin tulis untuk others
chmod ug-x file2.txt     # Hapus izin eksekusi dari user dan group
```

### b. Mengubah dengan Oktal
```bash
chmod 755 file2.txt      # rwxr-xr-x
chmod 000 file2.txt      # Tidak ada izin sama sekali
```

---
<br>

## 3. Mengubah Kepemilikan File/Folder

### a. Membuat User Baru
```bash
sudo adduser twothree
```

### b. Mengubah Kepemilikan File/Folder
```bash
ls -l                           # Lihat pemilik file
sudo chown twothre file2.txt      # Ubah pemilik file
sudo chown twothree folderbaru     # Ubah pemilik folder
```

### c. Mengubah Kepemilikan Seluruh Isi Folder
```bash
sudo chown -R twothree:twothree Modul4
```

---
<br>

## 📌 Catatan:
- Gunakan `ls` untuk melihat isi direktori.
- Gunakan `pwd` untuk mengetahui lokasi direktori saat ini.
- Gunakan `man [perintah]` untuk membaca manual dari perintah tertentu, misalnya: `man mv`.

---

## 🧑‍💻 Kontributor:
- Dokumentasi oleh: dayat 
- Bagian dari Modul 4: Sistem Operasi – Manajemen File dan Direktori
