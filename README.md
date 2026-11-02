# Superstore Sales Analysis — Excel Portfolio Project

## 📌 Ringkasan Proyek
Analisis data penjualan ritel Superstore (2014–2017) untuk mengidentifikasi
wilayah dan kategori produk yang menghasilkan penjualan tinggi namun margin
keuntungan rendah, serta memberikan rekomendasi strategi diskon.

## 🎯 Tujuan Analisis
1. Menghitung total penjualan & profit per region dan category.
2. Mengidentifikasi produk dengan profit negatif.
3. Menganalisis dampak diskon terhadap margin keuntungan.
4. Membuat dashboard interaktif untuk manajemen.

## 📂 Sumber Data
- **Dataset**: Superstore Sales Dataset
- **Sumber**: Kaggle (https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)
- **Jumlah baris**: ±9.994 transaksi
- **Kolom utama**: Order ID, Order Date, Region, Category, Sub-Category,
  Sales, Quantity, Discount, Profit

## 🗂️ Struktur File
| Sheet | Isi |
|-------|-----|
| `Raw_Data` | Data mentah tanpa perubahan |
| `Clean_Data` | Data setelah pembersihan |
| `Analysis` | Pivot Table & perhitungan |
| `Dashboard` | Visualisasi interaktif |
| `README` | Dokumentasi ini |

## 🧹 Proses Pembersihan Data
- Menghapus 17 baris duplikat berdasarkan Order ID + Product ID.
- Mengubah format tanggal dari `MM/DD/YYYY` ke `DD-MMM-YYYY`.
- Mengisi 4 nilai Postal Code kosong dengan "Unknown".
- Menambahkan kolom `Profit Margin` = Profit / Sales (format persentase).
- Menstandarkan nama region (menghapus spasi berlebih).

## 🔧 Fungsi Excel yang Digunakan
| Fungsi | Kegunaan |
|--------|----------|
| `XLOOKUP` | Menggabungkan tabel Region dengan tabel target penjualan |
| `SUMIFS` | Total sales per region & category |
| `COUNTIFS` | Jumlah order dengan profit negatif per sub-category |
| `IFS` | Kategorisasi margin: "Rendah" (<10%), "Sedang" (10–25%), "Tinggi" (>25%) |
| `Pivot Table` | Agregasi penjualan per region & tahun |
| `Slicer` | Filter interaktif dashboard |
| `Conditional Formatting` | Highlight baris dengan profit negatif |

## 📊 Insight Utama
1. **Region West** menyumbang 31% total penjualan tetapi margin hanya 14,9%.
2. **Sub-Category Tables** memiliki total profit negatif (-$17.725) akibat
   diskon rata-rata 26%.
3. Diskon >30% menurunkan margin hingga **-8%** (rata-rata).
4. **Technology** adalah kategori dengan margin tertinggi (17,4%).

## 💡 Rekomendasi Bisnis
- Batasi diskon maksimal 20% untuk sub-category Tables.
- Fokuskan promosi pada kategori Technology di region East.
- Evaluasi ulang strategi harga pada produk dengan profit negatif.

## 🛠️ Tools
Microsoft Excel 365 (Pivot Table, XLOOKUP, Slicer, Pivot Chart)
