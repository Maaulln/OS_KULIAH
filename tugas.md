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
     - HDD: 25GB ( '/' 20 GB, '/' storage 5GB, '/' swap 1,5GB )
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

