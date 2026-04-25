# TUGAS-PERTEMUAN-4-JAYA-ROSE-BOMBA-O.G
##🚀 Tugas Pertemuan 4 – Pemrograman Basis Data








##👤 Identitas
Keterangan	Detail
*👨‍🎓 Nama*	Jaya Rose Bomba O.G
*🆔 NIM*	IK2411007
*📚 Mata* Kuliah	Pemrograman Basis Data
##📌 Deskripsi Proyek

Proyek ini bertujuan untuk memahami penggunaan:

🔹 IF-THEN-ELSE
🔹 CASE Statement
🔹 Stored Procedure di MySQL

Digunakan untuk menyelesaikan beberapa studi kasus:

📦 Status stok barang
💰 Perhitungan diskon
🎓 Predikat & kelulusan mahasiswa
🗂️ Struktur Database
🧱 Membuat Database
CREATE DATABASE db_pertemuan4;
USE db_pertemuan4;
📦 Tabel Produk
CREATE TABLE produk (
    id_produk INT AUTO_INCREMENT PRIMARY KEY,
    nama_produk VARCHAR(100),
    stok INT
);
##📥 Data Produk
INSERT INTO produk (nama_produk, stok) VALUES
('Laptop', 25),
('Mouse', 4),
('Keyboard', 10),
('Flashdisk', 0),
('Monitor', 7);
##⚙️ Fitur Utama
🔹 1. Cek Status Stok (Stored Procedure)

Menentukan status stok berdasarkan jumlah barang.

##📊 Kategori:
Stok	Status
0	❌ Habis
1–5	⚠️ Hampir Habis
6–20	✅ Tersedia
>20	🔒 Stok Aman
▶️ Cara Menjalankan
CALL cek_status_stok(3);
🔹 2. CASE Statement (Query)

Menampilkan status stok langsung dari tabel.

SELECT 
id_produk,
nama_produk,
stok,
CASE 
    WHEN stok = 0 THEN 'Habis'
    WHEN stok BETWEEN 1 AND 5 THEN 'Hampir Habis'
    WHEN stok BETWEEN 6 AND 20 THEN 'Tersedia'
    ELSE 'Stok Aman'
END AS status_stok
FROM produk;
🔹 3. Hitung Diskon

Menghitung diskon berdasarkan total belanja.

##💸 Ketentuan Diskon:
Total Belanja	Diskon
≥ 1.000.000	15%
≥ 500.000	10%
≥ 250.000	5%
< 250.000	0%
▶️ Cara Menjalankan
CALL hitung_diskon(1200000);
🔹 4. Cek Predikat Mahasiswa

Menentukan nilai dan status kelulusan.

##🎓 Predikat:
Nilai	Predikat
≥ 90	🌟 Sangat Memuaskan
≥ 80	👍 Memuaskan
≥ 70	🙂 Baik
≥ 60	😐 Cukup
< 60	❌ Kurang
##✅ Kelulusan:
≥ 70 → Lulus
< 70 → Tidak Lulus
##▶️ Cara Menjalankan
CALL cek_predikat_mahasiswa(85);
🧪 Pengujian

✔ Menggunakan CALL untuk Stored Procedure
✔ Menggunakan SELECT untuk query CASE
✔ Semua output telah sesuai dengan logika percabangan

##📊 Insight / Pembelajaran
🧠 IF-THEN-ELSE cocok untuk logika kompleks dalam procedure
⚡ CASE lebih efisien untuk query langsung
🔄 Stored Procedure membuat kode lebih modular & reusable
📎 Contoh Output
Status: Hampir Habis

Total Belanja : Rp 1200000
Diskon : 15%
Jumlah Diskon : Rp 180000
Total Bayar : Rp 1020000

Nilai : 85
Predikat : Memuaskan
Status : Lulus
🏁 Status Project

✅ Selesai & Berjalan dengan Baik

##📌 Catatan

Project ini dibuat untuk keperluan pembelajaran dan latihan Pemrograman Basis Data.
