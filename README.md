# Tugas Pertemuan 12 - Sistem Reservasi Tiket Pesawat

# Soal
Buatlah sistem reservasi tiket pesawat yang mendukung tiga jenis kelas penerbangan:
1. Ekonomi
2. Bisnis
3. First Class

Setiap kelas penerbangan memiliki perhitungan tarif yang berbeda-beda. Selain itu, setiap kelas juga memiliki kebijakan khusus, seperti fasilitas tambahan, batas bagasi, atau layanan yang disediakan.

Struktur Kelas:
1. Kelas Ticket adalah kelas dasar atau superclass yang berfungsi sebagai kelas umum untuk semua jenis reservasi tiket pesawat.
2. Kelas EconomyTicket, BusinessTicket, dan FirstClassTicket adalah subclass yang mewarisi dari Ticket. Setiap subclass mengoverride metode calculateFare() untuk menentukan tarif sesuai kelas penerbangan.
3. Ketentuan Diskon ticket :
- EconomyTicket memberikan diskon 10%.
- BusinessTicket menambahkan biaya 25%.
- FirstClassTicket menambahkan biaya 50%.

# Penjelasan
Polymorphism pada program ini diterapkan ketika metode calculateFare() dan ```displayInfo()``` dipanggil pada objek dengan tipe referensi Ticket tetapi mengacu pada objek subclass (EconomyTicket, BusinessTicket, atau FirstClassTicket).<br>
Fungsi polymorphism di sini adalah untuk mempermudah pengelolaan berbagai jenis tiket penerbangan dengan tarif yang berbeda tanpa menggunakan struktur kontrol kompleks, memungkinkan ekspansi program dengan mudah, dan mengurangi duplikasi kode.
<br>
<br>
1. Superclass Ticket :
   - Berfungsi sebagai kelas dasar yang menyimpan informasi umum tiket seperti nama penumpang dan harga dasar.
   - Metode calculateFare() dihitung berdasarkan harga dasar, akan dioverride oleh subclass untuk perhitungan tarif yang lebih spesifik.
2. Subclass EconomyTicket :
   - Mengoverride metode calculateFare() untuk menerapkan diskon 10%.
   - Menambahkan informasi diskon dalam metode displayInfo().
3. Subclass BusinessTicket :
   - Mengoverride metode calculateFare() untuk menambahkan biaya 25%.
   - Menampilkan informasi tambahan biaya dalam metode displayInfo().
4. Subclass FirstClassTicket :
   - Mengoverride metode calculateFare() untuk menambahkan biaya 50%.
   - Menampilkan informasi tambahan biaya dalam metode displayInfo().
5. Kelas Main :
   - Membuat objek tiket untuk setiap kelas penerbangan (Ekonomi, Bisnis, First Class).
   - Menampilkan informasi setiap tiket menggunakan metode polymorphism displayInfo().
