# Alaya: Cek Harga Rumah di Jabodetabek
Aplikasi ini adalah bentuk proyek akhir dari program AI Mastery, Orbit Future Academy batch 4.
Dengan menerapkan algoritma Data Science, saya bersama temen-temen kelompok saya membangun suatu aplikasi prediksi harga rumah di Jabodetabek. Data yang kami gunakan adalah data yang saya dapatkan dari dosen saya, Pak Taufik Edy Sutanto, Ph. D, ketika mengampu mata kuliah Data Mining & Business Intelligence TA 2022/2023 di Prodi Statistika Universitas Indonesia. Data yang saya sertakan di siniadalah data yang telah melewati tahap preprocessing sehingga menghasilkan data yang siap dilakukan pemodelan. Dari data awal, saya melakukan preprocessing sebagai berikut:
1. Menghapus kolom yang semua barisnya kosong
2. Menghapus baris yang semua kolomnya kosong
3. Menghapus variabel yang dianggap tidak diperlukan
4. Mengganti nama kecamatan menjadi Kabupaten/Kota
5. Menghapus/mengganti data dengan noise
5.a. Untuk data dengan noise di kolom LT, dihapus
5.b. Untuk data dengan noise di listrik, dibubah ke angka paling mendekati
6. Menghapus data dengan daya listrik lebih dari 5500 VA
7. Menambahkan variabel garasi_carport untuk menggantikan variabel garasi dan carport
8. Imputasi missing values dengan KNNImputer

Setelah melakukan preprocessing, dilanjutkan mengksplorasi dan visualisasi data. Dari tahap ini ditemukan bahwa data yang kami gunakan memiliki cukup banyak outlier. Karena keterbatasan data, kami tidak menghapus outlier tersebut melainkan melakukan transformasi logaritma natural ke variabel harga yang menjadi variabel target pada pemodelan. Selain itu, untuk menangani outlier kami juga menggunakan model regresi yang robust terhadap outlier. Model yang kami coba gunakan adalah RANSACRegressor, DecisionTreeRegressor, dan RandomForestRegressor. Dari ketiga model tersebut, kami memilih RandomForestRegressor untuk kasus ini karena memiliki nilai matriks evaluasi yang terbaik dari model lainnya. 
