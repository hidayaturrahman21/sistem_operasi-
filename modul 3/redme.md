# 📁 Command Line: Manajemen File dan Direktori

Dokumentasi ini menjelaskan cara menggunakan command line (terminal) di Linux (Ubuntu) untuk membuat, mengelola, memindahkan, dan menghapus file serta direktori (folder), termasuk pengaturan izin dan kepemilikan.

### A. Shell Scripting dan Automasi

#### 1. Menggunakan Variabel
```bash
nama="dayat"
umur=19
echo "Halo, nama saya $nama dan umur saya $umur."
```

#### 2. Input dari Pengguna
```bash
echo "Masukkan nama anda:"
read nama
echo "Selamat datang $nama."
```

#### 3. Operasi Matematika
```bash
x=10
y=5
hasil=$((x + y))
echo "Hasil penjumlahan: $hasil"
```

### B. Percabangan (Kondisi)

#### If-Else
```bash
angka=10
if [ $angka -gt 5 ]; then
  echo "Angka lebih besar dari 5"
else
  echo "Angka kurang dari atau sama dengan 5"
fi
```

#### If-Elif-Else
```bash
nilai=80
if [ $nilai -ge 90 ]; then
  echo "grade: A"
elif [ $nilai -ge 75 ]; then
  echo "grade: B"
else
  echo "grade: C"
fi
```

### C. Perulangan

#### For Loop
```bash
for angka in {1..5}; do
  echo "Angka saat ini: $angka"
done
```

#### While Loop
```bash
angka=1
while [ $angka -le 5 ]; do
  echo "Angka saat ini: $angka"
  angka=$((angka + 1))
done
```

### D. Automasi dengan Cron Job
1. Buat skrip:
```bash
nano ~/log_time.sh
```
2. Isi skrip dan beri izin:
```bash
chmod +x ~/log_time.sh
```
3. Jadwalkan:
```bash
crontab -e
# Tambahkan baris berikut:
* * * * * ~/log_time.sh
```
4. Cek:
```bash
crontab -l
cat ~/log_time.txt
```

### E. Automasi dengan systemd Timers
- Buat file `.service` dan `.timer` untuk menjalankan skrip otomatis menggunakan systemd.
- Aktifkan timer dan periksa statusnya dengan:
```bash
systemctl start nama.timer
systemctl status nama.timer
```

### F. Debugging dan Logging

#### journalctl
```bash
journalctl               # Semua log
journalctl -u cron       # Log cron
journalctl -f            # Real-time log
```

#### dmesg
```bash
sudo dmesg               # Log kernel
```

---
