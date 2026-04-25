# 📘 Tugas Pertemuan 4 - Pemrograman Basis Data

## 👤 Identitas Mahasiswa

* **Nama** : Jaya Rose Bomba O.G
* **NIM** : IK2411007
* **Mata Kuliah** : Pemrograman Basis Data

---

## 📌 Deskripsi Tugas

Repository ini berisi hasil pengerjaan tugas pertemuan ke-4 yang membahas tentang **struktur kontrol percabangan** dalam MySQL, yaitu penggunaan **IF-THEN-ELSE** dan **CASE**.

Percabangan digunakan untuk mengambil keputusan berdasarkan kondisi tertentu, seperti:

* Menentukan status stok barang
* Menghitung diskon berdasarkan total belanja
* Menentukan predikat dan kelulusan mahasiswa

Seluruh implementasi dibuat menggunakan **Stored Procedure** dan **Query SQL**.

---

## 🗂️ Daftar File dalam Repository

* `program.sql` → Berisi seluruh kode SQL (database, tabel, data, procedure, dan pengujian)
* `laporan.pdf` → Berisi laporan analisis tugas
* `README.md` → Penjelasan repository

---

## ⚙️ Cara Menjalankan Program (Menggunakan Laragon)

### 1. Jalankan Laragon

* Buka aplikasi Laragon
* Klik **Start All** untuk menjalankan Apache & MySQL

---

### 2. Buka Database

* Klik menu **Database** di Laragon
* Pilih **phpMyAdmin** atau **HeidiSQL**

---

### 3. Import / Jalankan Script SQL

* Buat database baru (opsional, karena sudah ada di script)
* Buka file `program.sql`
* Copy seluruh isi file
* Paste ke query editor
* Klik **Run / Execute**

---

### 4. Menjalankan Procedure (Pengujian)

Gunakan perintah berikut:

```sql
CALL cek_status_stok(3);
CALL hitung_diskon(750000);
CALL cek_predikat_mahasiswa(85);
```

---

### 5. Menjalankan Query CASE

```sql
SELECT * FROM produk;
```

---

## 📊 Hasil yang Diharapkan

* Status stok ditampilkan sesuai jumlah stok
* Diskon dihitung berdasarkan total belanja
* Predikat dan status mahasiswa ditentukan sesuai nilai

---

## 🎯 Kesimpulan

Tugas ini menunjukkan bahwa struktur percabangan **IF-THEN-ELSE** dan **CASE** sangat penting dalam pemrograman basis data karena memungkinkan sistem untuk mengambil keputusan secara otomatis berdasarkan kondisi tertentu.

---

## 🚀 Catatan

* Pastikan MySQL pada Laragon sudah berjalan
* Pastikan tidak ada error saat menjalankan script
* Gunakan database `db_pertemuan4` sesuai script

---
