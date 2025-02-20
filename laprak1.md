# Laporan Instalasi Debian 12 di UTM pada Mac

**Tujuan:**  
Laporan ini bertujuan untuk mendokumentasikan proses instalasi Debian 12 menggunakan UTM (Unified Toolbox for Mac) pada perangkat Mac.

---

## Langkah-langkah Instalasi

1. **Unduh UTM**  
   - Akses situs resmi UTM di [https://mac.getutm.app/](https://mac.getutm.app/).  
   - Unduh aplikasi UTM.

2. **Instal UTM**  
   - Setelah proses pengunduhan selesai, buka file **UTM**.  
   - Pada menu installasi, seret logo **UTM** ke logo folder **Applications**.

3. **Buka Aplikasi UTM**  
   - Buka aplikasi UTM.  
   - Setelah UTM terbuka, pilih menu **UTM Gallery** untuk mendownload OS yang akan digunakan.  

4. **Pilih OS Debian 12**  
   - Di dalam UTM Gallery, cari dan pilih OS **Debian 12**.  
   - Klik opsi **Open in UTM** untuk memulai proses pengunduhan image OS Debian 12.  

5. **Tunggu Proses Pengunduhan**  
   - Tunggu hingga proses pengunduhan image Debian 12 selesai.  

6. **Mulai Instalasi Debian 12**  
   - Setelah pengunduhan selesai, klik tombol **Play** untuk memulai virtual machine Debian 12 .  
   - Konfigurasi OS dengan konfigurasi sebagai berikut.
     - CPU: 2
     - RAM: 4
     - HDD: 25GB ( `/` 20 GB, `/` storage 5GB, `/` swap 1,5GB )
     - Hostname : PrakOS_NRP

7. **Konfigurasi OS**
   - Pada saat instalasi, pilih **Install Debian GNU/Linux** dan ikuti langkah-langkah instalasi.
   - Setelah masuk ke menu **Dekstop** buka **Terminal**.
   - Pada terminal ketikkan perintah `sudo apt update` dan `sudo apt upgrade`.
   - Setelah itu ketikkan perintah `sudo nano /etc/hostname`.
   - Setelah masuk ke editor, ubah hostname sesuai dengan **PrakOS_NRP**.
   - Setelah itu ketikkan perintah `sudo reboot`.
   - Setelah instalasi selesai, Debian 12  akan berjalan di UTM pada perangkat Mac.

8. **Selesai**  
   - Setelah proses konfigurasi selesai, Debian 12 siap digunakan di UTM pada perangkat Mac.  

## Kesimpulan
1. **Kemudahan Penggunaan UTM:** UTM menyediakan antarmuka yang user-friendly dan memudahkan pengguna Mac untuk menjalankan sistem operasi virtual seperti Debian 12. Proses pengunduhan dan instalasi UTM sangatlah mudah dan cepat.


2. **Konfigurasi Virtual Machine:** Proses konfigurasi virtual machine, seperti alokasi CPU, RAM, dan penyimpanan, dapat disesuaikan dengan kebutuhan pengguna. Dalam percobaan ini, konfigurasi yang digunakan adalah 2 CPU, 4 GB RAM, dan 25 GB penyimpanan.

3. **Kinerja yang Stabil:** Setelah instalasi selesai, Debian 12  berjalan dengan stabil di UTM pada perangkat Mac, menunjukkan bahwa kombinasi ini dapat menjadi solusi yang efektif untuk menjalankan sistem operasi Linux di lingkungan macOS.

Secara keseluruhan, percobaan ini menunjukkan bahwa UTM adalah alat yang efektif dan efisien untuk menjalankan Debian 12 pada perangkat Mac, memberikan fleksibilitas dan kemudahan bagi pengguna yang membutuhkan lingkungan Linux di sistem macOS.

---

# Perbedaan Debian 11 (`Bullseye`) dan Debian 12 (`Bookworm`)
| Aspek                | Debian 11 (Bullseye)                          | Debian 12 (Bookworm)                          |
|----------------------|-----------------------------------------------|-----------------------------------------------|
| **Versi Kernel**     | Kernel Linux 5.10                             | Kernel Linux 6.1                             |
| **Kebutuhan Sistem** | RAM minimal: 512 MB                        | RAM minimal: 1 GB                          |
|                      | Ruang disk: 10 GB (minimal), 20 GB (disarankan) | Ruang disk: 10 GB (minimal), 20 GB (disarankan) |
| **Penerapan systemd**| systemd 247                                   | systemd 252                                   |
| **Perbedaan Package**| GNOME 3.38                                 | GNOME 43                                   |
|                      | LibreOffice 7.0                            | LibreOffice 7.4                            |
|                      | Python 3.9                                 | Python 3.11                                |
|                      | GCC 10.2                                   | GCC 12.2                                   |

## Kesimpulan
Debian 12 (`Bookworm`) menawarkan beberapa peningkatan signifikan dibandingkan Debian 11 (`Bullseye`):

1. **Kernel Lebih Baru:** Debian 12 menggunakan Kernel Linux 6.1, lebih baru dari Kernel Linux 5.10 pada Debian 11, memberikan dukungan hardware dan keamanan yang lebih baik.

2. **Kebutuhan Sistem Lebih Tinggi:** Debian 12 membutuhkan RAM minimal 1 GB, lebih tinggi dari 512 MB pada Debian 11, menunjukkan kesesuaian untuk perangkat modern.

3. **Pembaruan Paket:** Debian 12 menawarkan versi terbaru dari berbagai paket seperti GNOME 43, LibreOffice 7.4, Python 3.11, dan GCC 12.2, memberikan fitur dan perbaikan terbaru.

4. **Peningkatan systemd:** Debian 12 menggunakan systemd 252, lebih baru dari systemd 247 pada Debian 11, dengan berbagai perbaikan dalam manajemen sistem.

Secara keseluruhan, Debian 12 lebih cocok untuk pengguna yang menginginkan fitur terbaru dan kinerja yang lebih baik, sementara Debian 11 tetap menjadi pilihan yang layak untuk perangkat dengan spesifikasi lebih rendah.

---

# Cek Environment Menggunakan CPU-X
1. Buka terminal dan ketikkan perintah `sudo apt install cpu-x`.
2. Setelah proses instalasi selesai, ketikkan perintah `cpu-x`.
3. Setelah proses selesai, akan muncul informasi seperti berikut.

| Komponen | Spesifikasi |
|----------|-------------|
| CPU      | Intel Core i5-10300H |
| CPU      | 2.50 GHz |
| CPU      | 2 Core |
| RAM      | 4GB |
| Motherboard | ASUS ROG Strix Z390-F Gaming |
| GPU      | NVIDIA GeForce GTX 1650 |

## Kesimpulan

Percobaan ini menunjukkan cara menggunakan aplikasi `CPU-X` untuk memeriksa spesifikasi perangkat keras komputer. Setelah menginstal dan menjalankan `CPU-X`, diperoleh informasi detail tentang komponen utama sistem, seperti prosesor `(Intel Core i5-10300H dengan kecepatan 2.50 GHz dan 2 core)`, RAM `(4GB)`, motherboard `(ASUS ROG Strix Z390-F Gaming)`, dan GPU `(NVIDIA GeForce GTX 1650)`. Hasil ini memudahkan pengguna untuk memahami konfigurasi perangkat keras yang digunakan.

---

# Mencari Daftar Aplikasi Terinstal di Debian 12

Berikut adalah beberapa perintah shell yang dapat digunakan untuk mencari daftar aplikasi yang terinstal pada sistem Debian 12:

## 1. Menggunakan lshw
Perintah ini menampilkan informasi lengkap hardware.

```bash
sudo lshw
```

## 2. Menggunakan inxi -Fxz
Perintah ini menampilkan informasi suhu dan driver.

```bash
sudo inxi -Fxz
```

## 3. Menggunakan dmidecode
Perintah ini menampilkan informasi firmware dan komponen hardware dari sistem

```bash
sudo dmidecode
```

## 4. Menggunakan lsblk
Perintah ini menampilkan daftar penyimpanan

```bash
sudo lsblk
```

## 5. Menggunakan lscpu
Perintah ini menampilkan informasi CPU

```bash
sudo lscpu
```

## Kesimpulan
Perintah-perintah ini sangat berguna untuk memantau dan menganalisis konfigurasi sistem, baik untuk keperluan *administrasi* maupun *troubleshooting*.
