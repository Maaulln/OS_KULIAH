# Laporan Instalasi Debian 12 (Rosetta) di UTM pada Mac

**Tujuan:**  
Laporan ini bertujuan untuk mendokumentasikan proses instalasi Debian 12 menggunakan UTM (Unified Toolbox for Mac) pada perangkat Mac.

---

## A. Langkah-langkah Instalasi

1. **Unduh UTM**  
   - Akses situs resmi UTM di [https://mac.getutm.app/](https://mac.getutm.app/).  
   - Unduh aplikasi UTM.

2. **Instal UTM**  
   - Setelah proses pengunduhan selesai, buka file **UTM**.  
   - Pada menu installasi, seret logo **UTM** ke logo folder **Applications**.

3. **Buka Aplikasi UTM**  
   - Buka aplikasi UTM.  
   - Setelah UTM terbuka, pilih menu **UTM Gallery** untuk mendownload OS yang akan digunakan.  

4. **Pilih OS Debian 12 Rosetta**  
   - Di dalam UTM Gallery, cari dan pilih OS **Debian 12 Rosetta**.  
   - Klik opsi **Open in UTM** untuk memulai proses pengunduhan image OS Debian 12.  

5. **Tunggu Proses Pengunduhan**  
   - Tunggu hingga proses pengunduhan image Debian 12 selesai.  

6. **Mulai Instalasi Debian 12 Rosetta**  
   - Setelah pengunduhan selesai, klik tombol **Play** untuk memulai virtual machine Debian 12 Rosetta.  
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
   - Setelah instalasi selesai, Debian 12 Rosetta akan berjalan di UTM pada perangkat Mac.

8. **Selesai**  
   - Setelah proses konfigurasi selesai, Debian 12 siap digunakan di UTM pada perangkat Mac.  

---

# Perbedaan Debian 11 (bullseye) dan Debian 12 (bookworm)
| Aspek                | Debian 11 (Bullseye)                          | Debian 12 (Bookworm)                          |
|----------------------|-----------------------------------------------|-----------------------------------------------|
| **Versi Kernel**     | Kernel Linux 5.10                             | Kernel Linux 6.1                             |
| **Kebutuhan Sistem** | - RAM minimal: 512 MB                        | - RAM minimal: 1 GB                          |
|                      | - Ruang disk: 10 GB (minimal), 20 GB (disarankan) | - Ruang disk: 10 GB (minimal), 20 GB (disarankan) |
| **Penerapan systemd**| systemd 247                                   | systemd 252                                   |
| **Perbedaan Package**| - GNOME 3.38                                 | - GNOME 43                                   |
|                      | - LibreOffice 7.0                            | - LibreOffice 7.4                            |
|                      | - Python 3.9                                 | - Python 3.11                                |
|                      | - GCC 10.2                                   | - GCC 12.2                                   |

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

---

# Mencari Daftar Aplikasi Terinstal di Debian 12

Berikut adalah beberapa perintah shell yang dapat digunakan untuk mencari daftar aplikasi yang terinstal pada sistem Debian 12:

## 1. Menggunakan `lshw`
Perintah ini menampilkan informasi lengkap hardware.

```bash
`sudo lshw`
```

## 2. Menggunakan 'inxi -Fxz'
Perintah ini menampilkan informasi suhu dan driver.

```bash
`sudo inxi -Fxz`
```

## 3. Menggunakan 'dmidecode'
Perintah ini menampilkan informasi firmware dan komponen hardware dari sistem

```bash
`sudo dmidecode`
```

## 4. Menggunakan 'lsblk'
Perintah ini menampilkan daftar penyimpanan

```bash
`sudo lsblk`
```

## 5. Menggunakan 'lscpu'
Perintah ini menampilkan informasi CPU

```bash
`sudo lscpu`
```

