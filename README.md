# Aplikasi Pemesanan — UTS Mobile Programming

Repositori ini berisi proyek aplikasi pemesanan sederhana yang dikembangkan sebagai bagian dari Ujian Tengah Semester. Aplikasi menampilkan daftar produk, keranjang belanja, hingga halaman ringkasan pesanan (Order Summary).  

---

## 🧩 Fitur Utama Aplikasi
- Menampilkan daftar item yang dapat dibeli
- Menambah & mengurangi jumlah pesanan
- Perhitungan total harga berdasarkan isi keranjang
- Halaman Ringkasan Pesanan (Order Summary)
- **Bonus UTS: Diskon otomatis 10% untuk pembelian di atas Rp100.000**

---

## 🏷️ **Fitur Bonus: Diskon 10%**
Fitur tambahan ini memberikan potongan **10%** apabila nilai subtotal belanja melebihi **Rp100.000**.  

Diskon dihitung secara otomatis dan ditampilkan pada halaman `order_summary_page.dart`.

### 📘 **Logika Perhitungan**
```dart
double hitungDiskon(double subtotal) {
  return subtotal > 100000 ? subtotal * 0.10 : 0;
}

double totalAkhir(double subtotal) {
  final diskon = hitungDiskon(subtotal);
  return subtotal - diskon;
}
