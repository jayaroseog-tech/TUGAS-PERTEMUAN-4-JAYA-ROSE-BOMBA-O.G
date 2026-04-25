# TUGAS-PERTEMUAN-4-JAYA-ROSE-BOMBA-O.G
📘 README – Tugas Pertemuan 4

Pemrograman Basis Data

👤 Identitas
Nama: Jaya Rose Bomba O.G
NIM: IK2411007
Mata Kuliah: Pemrograman Basis Data
📌 Deskripsi Proyek

Proyek ini berisi implementasi struktur kontrol percabangan dalam MySQL, yaitu:

IF-THEN-ELSE
CASE

Digunakan untuk menyelesaikan beberapa kasus:

Menentukan status stok barang
Menghitung diskon belanja
Menentukan predikat dan kelulusan mahasiswa
🗂️ Struktur Database
1. Database
CREATE DATABASE db_pertemuan4;
USE db_pertemuan4;
2. Tabel Produk
CREATE TABLE produk (
    id_produk INT AUTO_INCREMENT PRIMARY KEY,
    nama_produk VARCHAR(100),
    stok INT
);
3. Data Produk
INSERT INTO produk (nama_produk, stok) VALUES
('Laptop', 25),
('Mouse', 4),
('Keyboard', 10),
('Flashdisk', 0),
('Monitor', 7);
⚙️ Fitur & Stored Procedure
1. 🔹 Cek Status Stok

Menentukan kondisi stok berdasarkan jumlah.

Logika:
0 → Habis
1–5 → Hampir Habis
6–20 → Tersedia

20 → Stok Aman

Pemanggilan:
CALL cek_status_stok(3);
2. 🔹 Query CASE Status Stok

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
3. 🔹 Hitung Diskon Belanja

Menghitung diskon berdasarkan total belanja.

Ketentuan Diskon:
≥ 1.000.000 → 15%
≥ 500.000 → 10%
≥ 250.000 → 5%
< 250.000 → 0%
Pemanggilan:
CALL hitung_diskon(1200000);
Output:
Total Belanja
Diskon (%)
Jumlah Diskon
Total Bayar
4. 🔹 Cek Predikat Mahasiswa

Menentukan predikat nilai dan status kelulusan.

Predikat:
≥ 90 → Sangat Memuaskan
≥ 80 → Memuaskan
≥ 70 → Baik
≥ 60 → Cukup
< 60 → Kurang
Kelulusan:
≥ 70 → Lulus
< 70 → Tidak Lulus
Pemanggilan:
CALL cek_predikat_mahasiswa(85);
🧪 Pengujian

Semua program diuji menggunakan:

CALL untuk stored procedure
SELECT untuk query CASE

Hasil diuji untuk memastikan:

Logika percabangan berjalan benar
Output sesuai dengan kondisi yang ditentukan
🎯 Kesimpulan

Melalui tugas ini, dipelajari bahwa:

IF-THEN-ELSE cocok untuk logika dalam procedure
CASE efektif untuk query langsung
Stored Procedure membantu modularisasi program di database
