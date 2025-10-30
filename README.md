# Analisis Data NYC TLC (New York City Taxi & Limousine Commission)

## Deskripsi Proyek
Proyek ini berfokus pada analisis data transportasi taksi di New York City dengan tujuan memahami pola penggunaan taksi dan karakteristik penggunanya. Analisis ini mengeksplorasi perjalanan taksi berdasarkan waktu, lokasi, dan karakteristik penumpang taksi, sehingga memberikan wawasan yang dapat digunakan untuk mendukung kebijakan transportasi, optimalisasi armada, dan meningkatkan layanan taksi di New York City.

## Tujuan Analisis
1. Mengidentifikasi waktu dan lokasi dengan tingkat penggunaan layanan taksi paling tinggi.
2. Mengidentifikasi kategori jarak dan durasi perjalanan yang sering dilakukan pengguna. 
3. Mengidentifikasi metode pembayaran yang paling banyak digunakan.
4. Mengidentifikasi hubungan antara tipe perjalanan dengan jarak perjalanan yang ditempuh.

## Dataset yang Digunakan
- Sumber: https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page
- Periode Data: 1 Januari 2023 – 31 Januari 2023
- Ukuran Data: ± 68 ribu baris
- Kolom Penting:
  <ol type="1">
    <li> <code>lpep_pickup_datetime</code> / <code>lpep_dropoff_datetime</code> – tanggal dan waktu penjemputan / penurunan</li>
    <li> <code>PULocationID</code> / <code>DOLocationID</code> – kode lokasi penjemputan / penurunan</li>
    <li> <code>trip_distance</code> – jarak perjalanan (mil)</li>
    <li> <code>total_amount</code> – total biaya perjalanan ($)</li>
    <li> <code>payment_type</code> – metode pembayaran</li>
    <li> <code>trip_type</code> – kode tipe perjalanan</li>
  </ol>

## Alur Analisis Data
1. **Persiapan dan Pembersihan Data**
    - Menghapus *missing value* dan anomali pada data
    -	Melakukan transformasi data
    -	Menambah beberapa kolom baru
2. **Analisis Pola Waktu Penggunaan**
    - Memvisualisasikan jumlah perjalanan berdasarkan jam, hari, dan hari kerja vs akhir pekan
    - Mengidentifikasi waktu puncak penggunaan taksi
3. **Analisis Pola Lokasi**
    - Mengidentifikasi lokasi dengan titik penjemputan dan penurunan paling banyak
    - Mengidentifikasi rute perjalanan yang sering dilalui
4. **Analisis Jarak dan Durasi Perjalanan**
    - Membandingkan jumlah perjalanan berdasarkan kategori jarak dan durasi perjalanan
    - Melakukan uji korelasi untuk menguji seberapa kuat hubungan antara jarak perjalanan dengan total biaya
5. **Analisis Metode Pembayaran**
    - Menghitung proporsi perjalanan berdasarkan metode pembayaran (kartu kredit vs tunai).
6. **Hubungan Tipe Perjalanan dan Jarak Perjalanan**
    - Membandingkan tipe perjalanan (*Street-hail* vs *Dispatch*) terhadap jarak perjalanan.
    - Melakukan uji chi-square untuk mengetahui apakah terdapat hubungan yang signifikan antara tipe perjalanan dengan jarak perjalanan

## Hasil Analisis
1. **Waktu Penggunaan Taksi**
    - Hari kerja: pengguna lebih banyak menggunakan taksi pada sore hari (17–18).
    - Akhir pekan: puncak penggunaan terjadi pada jam 15–16.
    - Menunjukkan bahwa taksi banyak digunakan untuk pulang kerja, sekolah, atau aktivitas harian.
2.	**Lokasi Perjalanan Populer**
    - East Harlem North dan East Harlem South menjadi lokasi dengan jumlah perjalanan tertinggi.
3.	**Jarak dan Durasi Perjalanan**
    - Mayoritas perjalanan bersifat jarak dekat dan singkat (≤ 2 mil dan ≤ 10 menit).
    - Tarif tinggi untuk perjalanan jauh kemungkinan membatasi penggunaan taksi hanya untuk jarak pendek.
4.	**Metode Pembayaran**
    - Mayoritas pengguna memilih kartu kredit dibandingkan pembayaran tunai.
5.	**Hubungan Tipe Perjalanan dan Jarak Perjalanan**
    - *Street-hail* lebih banyak digunakan untuk perjalanan jarak dekat dan sedang.
    - *Dispatch* lebih sering dipilih untuk perjalanan jarak dekat dan jauh.

