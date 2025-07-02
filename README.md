# 🍽️ Tugas Aplikasi Pemesanan Makanan / Minuman

## 📚 Tujuan

Membuat aplikasi sederhana berbasis **terminal/console** menggunakan **PHP**, yang digunakan untuk menghitung total pembayaran dari pemesanan makanan/minuman.

---

## 🔰 Part 1: Basic

### ✅ Fitur Wajib

1. Aplikasi berjalan di **console/terminal** (bukan web).
2. Saat aplikasi dijalankan, tampilkan daftar **menu makanan/minuman dan harganya**.
3. Input dilakukan secara **berurutan**:
   - **Nama item yang ingin dibeli** (misal: Nasi Goreng)
   - **Jumlah porsi** (misal: 2)
   - **Jumlah uang yang dibayar**
4. Setelah input, aplikasi akan menampilkan hasil pemesanan:
   - Nama makanan/minuman
   - Harga satuan
   - Jumlah porsi
   - Total harga
   - Uang dibayar
   - Kembalian (jika ada)

---

### 🍱 Daftar Menu

| Menu              | Harga/Porsi (Rp) |
| ----------------- | ---------------- |
| Nasi Goreng       | 15.000           |
| Mie Ayam          | 12.000           |
| Es Teh            | 5.000            |
| Kopi Hitam        | 8.000            |
| Jus Mangga        | 10.000           |

---

### 🧮 Contoh Kasus

Andi ingin membeli **2 porsi Nasi Goreng** dan membayar dengan **Rp 50.000**.

**Perhitungan:**
- Harga per porsi Nasi Goreng = Rp 15.000  
- Total = 2 × 15.000 = Rp 30.000  
- Kembalian = 50.000 - 30.000 = **Rp 20.000**

---

### 🧩 Contoh Output Console

```bash
=== Daftar Menu ===
1. Nasi Goreng - Rp 15.000
2. Mie Ayam    - Rp 12.000
3. Es Teh      - Rp 5.000
4. Kopi Hitam  - Rp 8.000
5. Jus Mangga  - Rp 10.000

Masukkan nama menu yang dibeli: Nasi Goreng
Masukkan jumlah porsi: 2
Masukkan jumlah uang yang dibayar: 50000

=== Rincian Pemesanan ===
Menu         : Nasi Goreng
Harga/porsi  : Rp 15.000
Jumlah porsi : 2
Total harga  : Rp 30.000
Uang dibayar : Rp 50.000
Kembalian    : Rp 20.000
```



⚠️ Validasi Wajib

  - Input jumlah porsi dan uang yang dibayar harus angka (gunakan is_numeric()).
  - Uang yang dibayar tidak boleh kurang dari total harga.
  - Gunakan format angka: Rp dan pemisah ribuan (number_format).
  - Tampilkan output dengan rapi dan mudah dibaca.

---
<!--
## 🚀 Part 2: Advance

Tambahkan fitur lanjutan ke dalam aplikasi:

### 1️⃣ Fitur Diskon (Opsional)

  - Tambahkan input diskon dalam bentuk persen (%)
  - Diskon maksimum 100%, tidak boleh negatif
  - Jika diskon diisi, total harga dikurangi diskon sebelum dihitung pajak

Contoh:
```
Total harga: Rp 30.000
Diskon: 10%
Setelah diskon: Rp 27.000
```

### 2️⃣ Tambahkan Pajak (PPN)

    Tambahkan PPN sebesar 11%
    PPN dihitung setelah diskon (jika ada)
    PPN wajib ditambahkan ke total bayar akhir

Contoh:
```
Setelah diskon: Rp 27.000
PPN 11% = Rp 2.970
Total yang harus dibayar = Rp 29.970
```

### 🧩 Contoh Output Advance
```
=== Rincian Pemesanan ===
Menu           : Nasi Goreng
Harga/porsi    : Rp 15.000
Jumlah porsi   : 2
Diskon         : 10%
Total diskon   : Rp 3.000
Harga setelah diskon : Rp 27.000
PPN (11%)      : Rp 2.970
Total bayar    : Rp 29.970
Uang dibayar   : Rp 50.000
Kembalian      : Rp 20.030
```
### 💡 Tips Tambahan
  - Gunakan strtolower() agar input menu tidak case-sensitive.
  - Buat array untuk menyimpan menu dan harga.
  - Gunakan fungsi round() untuk pembulatan desimal jika diperlukan.
  - Buat fungsi sendiri untuk format Rp agar bisa dipakai ulang.
  - Gunakan number_format() untuk pemisah ribuan.
