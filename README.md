# Customer_segmentation_financing_companya

# 🚗 Customer Segmentation with KMeans, Studi kasus Perusahaan Pembiayaan Kendaraan
Analisis ini bertujuan untuk melakukan segmentasi customer perusahaan pembiayaan kendaraan berdasarkan faktor usia, pendapatan tahunan, jumlah pinjaman, lama bergabung, dan skor kredit. Tujuan akhir adalah memberikan rekomendasi program promosi yang lebih tepat sasaran untuk tiap segmen.

## Tahapan
- Standarisasi data sebelum clustering.
- Cari jumlah cluster terbaik (pakai Elbow Method).
- Jalankan KMeans dan interpretasi hasilnya.

## Elbow Method 
adalah cara yang populer untuk menentukan jumlah cluster optimal di KMeans. Cara kerjanya adalah:
1. WCSS (Within-Cluster Sum of Squares): Ini adalah ukuran seberapa padat data dalam setiap cluster. Semakin kecil nilai WCSS, semakin baik. WCSS dihitung untuk setiap jumlah cluster yang dicoba (misal 1 cluster, 2 cluster, 3 cluster, dll.).
2. Plot Elbow: Kamu akan menggambarkan grafik WCSS terhadap jumlah cluster. Biasanya, grafik akan menurun tajam pada awalnya, lalu melambat setelah mencapai titik tertentu, yang disebut "elbow".
3. Titik Elbow: Titik di mana penurunan WCSS mulai melambat adalah jumlah cluster yang paling optimal. Mengapa? Karena menambah cluster lebih banyak setelah titik ini tidak memberikan banyak perbaikan dalam pemisahan data, sehingga membuat model jadi lebih kompleks tanpa manfaat signifikan.

Cara Membaca Grafik Elbow:
- Pada grafik, cari titik di mana penurunan WCSS mulai melambat.
- Titik ini biasanya muncul seperti elbow (siku) pada grafik.
- Misalnya, jika penurunan WCSS mulai melambat setelah 4 cluster, maka jumlah cluster yang optimal adalah 4.

Hasil Grafik Elbow:
Kalau kita amati plot Elbow Method:
- Dari 1 ke 2 cluster, penurunan WCSS sangat besar.
- Dari 2 ke 3 dan 3 ke 4 cluster, penurunannya juga cukup tajam.
- Setelah 4 cluster, garis mulai mendatar — artinya, menambah lebih banyak cluster (5, 6, dst.) sudah tidak banyak mengurangi WCSS lagi.
👉 Jadi, 4 cluster memang terlihat sebagai titik "elbow" — tempat di mana manfaat menambah cluster mulai berkurang.
Kesimpulannya: Jumlah cluster yang baik untuk kasus ini adalah 4.
  
## Metodologi
Metode KMeans Clustering digunakan untuk mengelompokkan customer menjadi 4 segmentasi berdasarkan hasil Elbow Method.

## Hasil KMeans
Cluster | Usia (~tahun) | Pendapatan_Tahunan (~juta) | Jumlah_Pinjaman (~juta) | Lama_Bergabung (~tahun) | Skor_Kredit
0 | 53.2 | 176.6 | 558.8 | 9.6 | 494
1 | 31.9 | 322.4 | 642.1 | 6.0 | 577
2 | 39.8 | 316.8 | 230.2 | 7.5 | 423
3 | 47.9 | 275.0 | 259.8 | 6.4 | 740

## Profil Cluster:
Cluster 0:
- Usia: Tua (53 tahun),
- Pendapatan: Rendah-menengah (176 juta/tahun),
- Jumlah Pinjaman: Tinggi (558 juta),
- Lama Bergabung: Lama (9,6 tahun),
- Skor Kredit: Rendah (494).
👉 Segmentasi: Customer senior dengan pinjaman besar dan risiko kredit rendah — perlu perhatian untuk retensi dan monitoring.

Cluster 1:
- Usia: Muda (32 tahun),
- Pendapatan: Tinggi (322 juta/tahun),
- Jumlah Pinjaman: Sangat besar (642 juta),
- Lama Bergabung: Baru (~6 tahun),
- Skor Kredit: Sedang (577).
👉 Segmentasi: Customer muda berpenghasilan tinggi, pinjaman besar — cocok untuk program loyalitas dan cross-selling produk tambahan.

Cluster 2:
- Usia: Dewasa menengah (40 tahun),
- Pendapatan: Tinggi (316 juta/tahun),
- Jumlah Pinjaman: Kecil (230 juta),
- Lama Bergabung: Cukup lama (~7,5 tahun),
- Skor Kredit: Rendah (423).
👉 Segmentasi: Customer dewasa, pendapatan tinggi tapi skor kredit rendah — butuh edukasi finansial dan monitoring ketat.

Cluster 3:
- Usia: Paruh baya (48 tahun),
- Pendapatan: Menengah-atas (275 juta/tahun),
- Jumlah Pinjaman: Sedang (259 juta),
- Lama Bergabung: Sedang (~6,4 tahun),
- Skor Kredit: Sangat tinggi (740).
👉 Segmentasi: Customer loyal, stabil, dan aman — ideal untuk diberikan promo spesial atau program penghargaan.

## Strategi Promo
Cluster | Strategi Promo
0 | Program retensi senior + monitoring kredit
1 | Program loyalitas muda, kredit besar (cross-sell produk tambahan)
2 | Edukasi kredit & monitoring ketat
3 | Program VIP dan penghargaan loyalitas


---

🧑‍💻 Dibuat oleh: Andy Sarbini  
📬 Kontak: kangandy09@gmail.com
