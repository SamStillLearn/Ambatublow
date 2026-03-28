# Ambatublow (Microcontroller Game)
Amba to Blow adalah sebuah permainan interaktif berbasis mikrokontroler ESP32 yang menguji ketepatan, pengambilan keputusan, dan manajemen tekanan pemain. Sistem ini mereplikasi ketegangan skenario penjinakan bom melalui antarmuka perangkat keras fisik, yang diperkuat dengan umpan balik visual dari layar OLED dan efek suara dari buzzer.

Mekanika Permainan & Pengalaman Pengguna: Permainan ini dirancang dengan alur logika yang lugas namun menantang, menggunakan sistem toleransi kesalahan:

Objektif Utama: Pemain dihadapkan pada 5 tombol fisik dan harus menemukan satu tombol "Defuse" yang tepat untuk menonaktifkan sistem.

Antarmuka Layar OLED: Layar berfungsi sebagai dashboard utama yang menampilkan status permainan dan timer secara real-time.

Sistem Kesalahan: Pemain memiliki batas toleransi maksimal 2 (dua) kali kesalahan. Setiap kali pemain menekan tombol yang salah, layar OLED akan memperbarui status dan buzzer akan mengeluarkan efek suara peringatan.

Kondisi Gagal: Jika batas toleransi habis (3 kali salah), sistem memicu status Gagal. OLED akan menampilkan status meledak yang diiringi dengan nada panjang/khas dari buzzer.

Kondisi Berhasil: Menekan tombol yang tepat sebelum jatah kesalahan habis akan menonaktifkan sistem, memicu pesan kemenangan di layar dan nada keberhasilan dari buzzer.

Sistem Acak Dinamis: Posisi tombol "Defuse" diacak secara otomatis oleh algoritma ESP32 pada setiap ronde baru, memastikan tingkat putar ulang (replayability) yang tinggi.
