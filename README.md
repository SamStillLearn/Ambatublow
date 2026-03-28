# 💣 Amba to Blow: ESP32 Bomb Defusal Simulation

Amba to Blow adalah sebuah permainan interaktif berbasis mikrokontroler ESP32 yang menguji ketepatan, pengambilan keputusan, dan manajemen tekanan pemain. Sistem ini mereplikasi ketegangan skenario penjinakan bom melalui antarmuka perangkat keras fisik, yang diperkuat dengan umpan balik visual dari layar OLED dan efek suara dari buzzer.

## 🎮 Mekanika Permainan & Pengalaman Pengguna

Permainan ini dirancang dengan alur logika yang lugas namun menantang, memaksa pemain untuk tetap tenang dengan menggunakan sistem toleransi kesalahan yang ketat:

* **🎯 Objektif Utama:** Pemain dihadapkan pada 5 tombol fisik dan harus menemukan **satu** tombol "Defuse" yang tepat untuk menonaktifkan sistem.
* **📺 Antarmuka Layar OLED:** Layar berfungsi sebagai dashboard utama yang menampilkan status permainan dan timer secara *real-time*.
* **⚠️ Sistem Kesalahan:** Pemain memiliki batas toleransi maksimal **2 (dua) kali kesalahan**. Setiap kali pemain menekan tombol yang salah:
  * Layar OLED akan memperbarui status kesalahan.
  * Buzzer akan mengeluarkan efek suara peringatan.
* **💥 Kondisi Gagal:** Jika batas toleransi habis (3 kali salah tekan), sistem memicu status **Gagal**. OLED akan menampilkan status meledak yang diiringi dengan nada panjang/khas dari buzzer.
* **✅ Kondisi Berhasil:** Menekan tombol yang tepat sebelum jatah kesalahan habis akan menonaktifkan sistem, memicu pesan kemenangan di layar dan nada keberhasilan dari buzzer.
* **🔀 Sistem Acak Dinamis:** Posisi tombol "Defuse" diacak secara otomatis oleh algoritma ESP32 pada setiap ronde baru, memastikan tingkat putar ulang (*replayability*) yang tinggi.

---

## 🛠️ Komponen yang Dibutuhkan

Untuk membangun proyek ini, Anda akan membutuhkan komponen-komponen berikut:

* 1x ESP32 Development Board
* 1x Layar OLED 0.96" (I2C)
* 5x Push Button (Tombol Taktil)
* 1x Buzzer Aktif
* Breadboard & Kabel Jumper secukupnya

## 🔌 Skema Rangkaian (Pinout)

*Sesuaikan pin di bawah ini dengan kode yang Anda gunakan.*

| Komponen | Pin ESP32 | Keterangan |
| :--- | :---: | :--- |
| **OLED SDA** | `GPIO 21` | I2C Data |
| **OLED SCL** | `GPIO 22` | I2C Clock |
| **Buzzer** | `GPIO 15` | Output Suara |
| **Button 1** | `GPIO 13` | Input Pull-up |
| **Button 2** | `GPIO 12` | Input Pull-up |
| **Button 3** | `GPIO 14` | Input Pull-up |
| **Button 4** | `GPIO 27` | Input Pull-up |
| **Button 5** | `GPIO 26` | Input Pull-up |
