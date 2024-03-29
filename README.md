---

# Laporan Proyek Machine Learning - Prediksi Gaji - Muhammad Thayyib

## Domain Proyek

Dalam konteks proyek ini, fokus utama adalah pada pembuatan model machine learning untuk memprediksi gaji seseorang berdasarkan beberapa fitur seperti usia, jenis kelamin, tingkat pendidikan, jabatan pekerjaan, dan tahun-tahun pengalaman. Prediksi gaji memiliki banyak aplikasi dalam industri, termasuk dalam proses rekrutmen dan penggajian karyawan.

### Latar Belakang

Penggajian karyawan merupakan salah satu aspek penting dalam pengelolaan sumber daya manusia di sebuah perusahaan. Penentuan gaji yang tepat dapat memengaruhi kepuasan dan motivasi karyawan, serta memberikan dampak pada kinerja dan produktivitas perusahaan secara keseluruhan[1]. Oleh karena itu, pengembangan model prediksi gaji menjadi relevan dalam mendukung pengambilan keputusan yang akurat dalam manajemen sumber daya manusia.

### Masalah dan Urgensi

Masalah yang dihadapi adalah bagaimana menghasilkan prediksi gaji yang akurat berdasarkan karakteristik individu karyawan[1]. Urgensinya adalah untuk meningkatkan efisiensi dalam proses penggajian, memastikan keadilan dalam penetapan gaji, serta mendukung pengambilan keputusan strategis dalam pengelolaan sumber daya manusia.


## Business Understanding

### Problem Statements

Dalam proyek ini, kami bertujuan untuk menjawab dua pernyataan masalah berikut:
1. Bagaimana memprediksi gaji seseorang berdasarkan fitur-fitur yang diberikan?
2. Faktor-faktor apa saja yang memengaruhi besaran gaji seseorang?

### Goals

Tujuan proyek ini adalah:
1. Membangun model machine learning yang dapat memprediksi gaji berdasarkan fitur-fitur yang diberikan.
2. Mengidentifikasi faktor-faktor yang memiliki pengaruh signifikan terhadap besaran gaji.

#### Latar Belakang

Dalam dunia bisnis modern, pengelolaan sumber daya manusia merupakan salah satu aspek penting yang memengaruhi kesuksesan sebuah perusahaan. Penggajian karyawan adalah salah satu bagian dari manajemen sumber daya manusia yang memiliki dampak signifikan terhadap produktivitas, kepuasan karyawan, dan keberlanjutan bisnis secara keseluruhan. Oleh karena itu, penting bagi perusahaan untuk memiliki sistem penggajian yang adil, transparan, dan efisien.

Penetapan gaji merupakan proses yang kompleks dan memerlukan pertimbangan berbagai faktor, termasuk pengalaman kerja, tingkat pendidikan, jabatan pekerjaan, dan faktor-faktor lainnya. Namun, dalam banyak kasus, proses ini dapat menjadi subjektif dan rentan terhadap bias.

Dalam konteks ini, penggunaan model machine learning untuk memprediksi gaji seseorang dapat memberikan keuntungan yang signifikan bagi perusahaan. Dengan memanfaatkan data historis tentang karyawan dan faktor-faktor yang memengaruhi gaji, perusahaan dapat mengembangkan model yang dapat memberikan perkiraan gaji yang lebih objektif dan terukur.

#### Dampak dan Urgensi

Penerapan model machine learning untuk memprediksi gaji memiliki dampak yang luas dalam konteks bisnis dan ekonomi, antara lain:

1. **Keputusan Penggajian yang Lebih Adil**: Dengan menggunakan model yang didasarkan pada data objektif, perusahaan dapat memastikan bahwa keputusan penggajian didasarkan pada faktor-faktor yang relevan dan tidak terpengaruh oleh bias individu. Hal ini dapat membantu menciptakan lingkungan kerja yang lebih adil dan merata bagi semua karyawan.

2. **Efisiensi dalam Manajemen Sumber Daya Manusia**: Dengan adanya model prediksi gaji yang akurat, perusahaan dapat mengoptimalkan alokasi sumber daya manusia dan merencanakan anggaran dengan lebih efisien. Hal ini memungkinkan perusahaan untuk mengalokasikan sumber daya dengan lebih baik sesuai dengan kebutuhan operasional dan strategis.

3. **Peningkatan Kepuasan Karyawan**: Dengan memiliki proses penggajian yang transparan dan terukur, karyawan akan merasa lebih dihargai dan diakui atas kontribusi mereka. Hal ini dapat meningkatkan tingkat kepuasan karyawan, yang pada gilirannya dapat berkontribusi pada produktivitas dan retensi karyawan yang lebih tinggi.

#### Contoh Penggunaan Hasil Prediksi Gaji dalam Pengambilan Keputusan Bisnis

Misalnya, sebuah perusahaan teknologi sedang melakukan evaluasi kinerja karyawan dan merencanakan peningkatan gaji tahunan. Dengan menggunakan model prediksi gaji, perusahaan dapat:

- Mengidentifikasi karyawan yang mungkin memiliki gaji di bawah rata-rata untuk tingkat pendidikan dan pengalaman kerjanya, dan memberikan peningkatan gaji yang sesuai untuk menjaga keseimbangan internal dan menghindari masalah kepuasan karyawan.
- Menganalisis dampak peningkatan gaji terhadap anggaran perusahaan dan menentukan alokasi dana yang optimal untuk memenuhi kebutuhan penggajian tanpa mengorbankan stabilitas keuangan perusahaan.

Dengan demikian, penggunaan model prediksi gaji dapat membantu perusahaan dalam mengambil keputusan yang lebih tepat dan strategis dalam pengelolaan sumber daya manusia mereka.


## Data Understanding

Dataset yang digunakan dalam proyek ini berisi informasi tentang gaji karyawan di sebuah perusahaan. Setiap baris mewakili seorang karyawan, dan kolom-kolomnya mencakup informasi seperti usia, jenis kelamin, tingkat pendidikan, jabatan pekerjaan, tahun-tahun pengalaman, dan gaji.

### Variabel-variabel pada Dataset:

1. **Age (Usia)**: Kolom ini menyajikan usia dari setiap karyawan dalam tahun. Nilai-nilai dalam kolom ini bersifat numerik.
   
2. **Gender (Jenis Kelamin)**: Kolom ini berisi informasi tentang jenis kelamin setiap karyawan, yang dapat berupa laki-laki atau perempuan. Nilai-nilai dalam kolom ini bersifat kategorikal.

3. **Education Level (Tingkat Pendidikan)**: Kolom ini memuat informasi tentang tingkat pendidikan setiap karyawan, yang dapat berupa SMA, sarjana (bachelor's degree), magister (master's degree), atau doktor (PhD). Nilai-nilai dalam kolom ini bersifat kategorikal.

4. **Job Title (Jabatan Pekerjaan)**: Kolom ini berisi jabatan pekerjaan setiap karyawan, yang dapat bervariasi tergantung pada perusahaan dan mencakup posisi seperti manajer, analis, insinyur, atau administrator. Nilai-nilai dalam kolom ini bersifat kategorikal.

5. **Years of Experience (Tahun-tahun Pengalaman)**: Kolom ini mencerminkan jumlah tahun pengalaman kerja dari setiap karyawan. Nilai-nilai dalam kolom ini bersifat numerik.

6. **Salary (Gaji)**: Kolom ini menunjukkan gaji tahunan dari setiap karyawan dalam dolar Amerika Serikat (USD). Nilai-nilai dalam kolom ini bersifat numerik dan dapat bervariasi tergantung pada faktor-faktor seperti jabatan pekerjaan, tahun-tahun pengalaman, dan tingkat pendidikan.

### Analisis

Analisis dilakukan untuk memahami hubungan antara fitur-fitur dalam dataset dengan gaji. Visualisasi histogram distribusi gaji menunjukkan bahwa distribusi gaji cenderung condong ke kanan (right-skewed), dengan sebagian besar responden memiliki gaji di kisaran rendah hingga menengah.

#### Visualisasi Analisis

##### Gambar 1: Histogram Distribusi Gaji
![Histogram Distribusi Gaji](https://github.com/mthayyibUnp/Salary-Prediction-Machine-Learning/assets/124302200/ac8a208b-0c18-4e67-bcac-de42e2dba3a7)

Gambar 1 menunjukkan distribusi gaji responden dalam dataset. Sumbu x mewakili gaji, sedangkan sumbu y mewakili jumlah orang yang menerima gaji tersebut. Distribusi gaji cenderung condong ke kanan (right-skewed), dengan sebagian besar responden memiliki gaji di kisaran rendah hingga menengah. Perbedaan antara gaji rata-rata dan gaji median menunjukkan adanya sebagian responden dengan penghasilan jauh lebih tinggi dari rata-rata, yang dapat dipengaruhi oleh faktor-faktor seperti pendidikan, pengalaman kerja, dan lokasi.

##### Gambar 2: Heatmap Korelasi
![Heatmap Korelasi](https://github.com/mthayyibUnp/Salary-Prediction-Machine-Learning/assets/124302200/3f831465-c9e8-4433-bdd8-4d26cf49d8ea)

Gambar 2 merupakan peta panas yang menampilkan korelasi antara variabel usia, masa kerja, dan gaji. Warna pada peta panas menunjukkan kekuatan korelasi antara variabel-variabel tersebut. Terdapat korelasi positif yang kuat antara usia dan gaji, serta antara masa kerja dan gaji. Artinya, semakin bertambah usia atau masa kerja seseorang, gaji cenderung meningkat. Namun, terdapat korelasi positif yang lebih lemah antara usia dan masa kerja.


## Data Preparation

Pada tahap Data Preparation, langkah-langkah spesifik yang diambil mencakup beberapa teknik untuk mempersiapkan data secara optimal sebelum digunakan dalam pembangunan model machine learning. Beberapa langkah tersebut antara lain:

1. **Pemisahan Dataset**: Pertama-tama, dataset perlu dipisahkan menjadi dua bagian utama: data latih (train set) dan data uji (test set). Rasio pemisahan dataset yang umum digunakan adalah 80:20 atau 70:30. Misalnya, dari total data yang tersedia, 80% digunakan untuk melatih model (train set), sementara 20% sisanya digunakan untuk menguji kinerja model (test set).

2. **Penghapusan Nilai Null**: Dilakukan pemeriksaan terhadap dataset untuk mendeteksi keberadaan nilai null atau missing values. Jika ditemukan, langkah selanjutnya adalah memutuskan cara penanganannya. Salah satu pendekatan yang umum adalah menghapus baris atau kolom yang mengandung nilai null tersebut. Misalnya, jika terdapat kolom yang memiliki sebagian besar nilai null dan tidak krusial untuk analisis, kolom tersebut dapat dihapus secara keseluruhan.

3. **Pemrosesan Fitur Kategorikal**: Fitur-fitur kategorikal perlu diubah menjadi bentuk numerik agar dapat dimengerti oleh model machine learning. Teknik yang umum digunakan adalah pengkodean one-hot (one-hot encoding). Dalam teknik ini, setiap kategori pada fitur kategorikal diubah menjadi variabel biner, di mana nilai 1 menunjukkan keberadaan kategori tersebut dan nilai 0 menunjukkan sebaliknya.

4. **Skalasi Fitur Numerik**: Fitur-fitur numerik mungkin memiliki rentang nilai yang berbeda-beda. Untuk memastikan bahwa tidak ada fitur yang mendominasi yang lain, dilakukan proses skalasi. Salah satu metode yang umum digunakan adalah normalisasi. Dalam normalisasi, nilai setiap fitur dikurangi dengan rata-rata fitur dan dibagi dengan standar deviasi fitur.

5. **Penanganan Ketidakseimbangan Kelas (Jika Diperlukan)**: Jika dataset memiliki ketidakseimbangan dalam distribusi kelas, langkah-langkah khusus mungkin diperlukan untuk menangani masalah ini. Misalnya, untuk masalah klasifikasi biner dengan kelas minoritas, teknik seperti oversampling (penambahan duplikat sampel dari kelas minoritas) atau undersampling (pengurangan sampel dari kelas mayoritas) dapat diterapkan.

Dengan menerapkan langkah-langkah di atas dengan benar, data akan siap digunakan untuk melatih model machine learning dengan kinerja yang optimal. Langkah-langkah tersebut membantu memastikan bahwa data yang digunakan bersih, terstruktur, dan siap digunakan untuk pembangunan model yang akurat dan dapat diandalkan.


## Modelling

Dalam tahap Modelling, dilakukan pembangunan model machine learning untuk menyelesaikan permasalahan yang telah diidentifikasi sebelumnya. Model yang dipilih dan diimplementasikan dalam proyek ini adalah **Random Forest Regressor**. Pemilihan model ini didasarkan pada beberapa pertimbangan sebagai berikut:

1. **Random Forest Regressor** dipilih karena memiliki kemampuan untuk menangani dataset dengan banyak fitur dengan baik. Selain itu, model ini memiliki fleksibilitas yang baik dalam menangani data numerik dan kategorikal. Random Forest juga cenderung tidak overfitting dan dapat memberikan hasil yang stabil.

2. **Parameter Random Forest Regressor**:
   - `n_estimators`: Jumlah pohon keputusan dalam ensemble. Semakin banyak pohon, semakin baik modelnya, tetapi juga semakin lama waktu komputasi yang dibutuhkan. Dalam proyek ini, nilai defaultnya adalah 100.
   - `max_depth`: Kedalaman maksimum dari setiap pohon keputusan. Pengaturan nilai yang lebih rendah dapat membantu mencegah overfitting. Nilai defaultnya adalah None, yang berarti setiap node akan diperluas sampai semua daunnya murni.
   - `min_samples_split`: Jumlah sampel minimum yang diperlukan untuk membagi sebuah node internal. Nilai defaultnya adalah 2, yang berarti node akan dibagi jika memiliki setidaknya 2 sampel.
   - `min_samples_leaf`: Jumlah sampel minimum yang diperlukan untuk menjadi daun (node termina) dalam pohon. Nilai defaultnya adalah 1.

3. **Implementasi Model**:
   - Proses pemodelan dimulai dengan menginisialisasi Random Forest Regressor dengan parameter yang telah ditentukan.
   - Kemudian, model dilatih menggunakan data latih (train set) yang telah dipersiapkan sebelumnya.
   - Setelah pelatihan selesai, model dievaluasi menggunakan data uji (test set) untuk mengukur kinerjanya.
   - Jika kinerja model dianggap memuaskan, model tersebut dapat digunakan untuk memprediksi gaji berdasarkan fitur-fitur yang diberikan.

Dengan menggunakan Random Forest Regressor dan melakukan proses pemodelan dengan tepat, diharapkan model yang dihasilkan mampu memberikan prediksi gaji yang akurat dan dapat digunakan untuk mendukung pengambilan keputusan yang lebih baik dalam konteks analisis gaji.


## Evaluasi

Dalam proses evaluasi model machine learning, metrik evaluasi yang dipilih sangat penting untuk mengukur kinerja model. Dalam kasus ini, metrik evaluasi yang digunakan adalah Mean Squared Error (MSE), yang mengukur rata-rata dari kuadrat perbedaan antara nilai sebenarnya (y_test) dan nilai prediksi (y_pred). 

Rumus untuk MSE adalah sebagai berikut:

$$MSE=\frac{1}{n} \sum_{i=1}^n (y_i - \hat{y_i})^2$$

### Evaluasi Menggunakan Mean Squared Error (MSE)

Dalam evaluasi ini, kita menggunakan Mean Squared Error (MSE) sebagai metrik utama untuk mengukur kinerja model. Nilai MSE yang lebih rendah menunjukkan bahwa model lebih baik dalam memprediksi nilai gaji.

Hasil evaluasi Mean Squared Error (MSE) yang diperoleh sebesar 296285366.6666667 menunjukkan bahwa rata-rata kuadrat perbedaan antara nilai gaji yang diprediksi oleh model dengan nilai gaji sebenarnya adalah sebesar itu. Semakin rendah nilai MSE, semakin baik model dalam memprediksi nilai gaji. Dalam konteks ini, meskipun nilai MSE cukup tinggi, kita perlu mempertimbangkan faktor-faktor lain seperti karakteristik dataset dan kebutuhan bisnis sebelum menyimpulkan kualitas model.

### Evaluasi Alternatif

Selain MSE, terdapat juga metrik evaluasi lain yang bisa dipertimbangkan seperti Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), dan koefisien determinasi (R-squared). Evaluasi lebih lanjut dengan menggunakan berbagai metrik evaluasi dapat memberikan pemahaman yang lebih komprehensif tentang kinerja model dan kemungkinan perbaikan yang bisa dilakukan.

### Visualisasi Evaluasi

#### Gambar 3 - Scatter Plot Actual vs Predicted Salary
![Untitled](https://github.com/mthayyibUnp/Salary-Prediction-Machine-Learning/assets/124302200/04aa9a04-7b70-4158-9b30-4b8a23deb181)


Pada gambar 3, ada lebih banyak titik data di sudut kiri bawah grafik. Artinya model tersebut cenderung meremehkan gaji yang tinggi. Misalnya, jika gaji sebenarnya seseorang adalah $200.000, model mungkin memperkirakan gajinya hanya $150.000.  
Ada lebih sedikit titik data yang jauh dari garis diagonal. Artinya, model ini lebih akurat dalam memprediksi gaji di kisaran rata-rata dibandingkan dengan gaji yang sangat tinggi atau rendah.  
  
Secara keseluruhan, plot sebar menunjukkan bahwa model tersebut dapat digunakan untuk memperkirakan gaji, namun penting untuk diingat bahwa prediksi tersebut mungkin tidak sempurna.

Dengan demikian, evaluasi model ini telah memberikan wawasan yang lebih mendalam tentang kinerja model dalam memprediksi gaji berdasarkan fitur-fitur yang diberikan.


---

Demikianlah laporan proyek ini disusun. Terima kasih.

## Referensi

- Das, S., Barik, R., Mukherjee, A. (2020). "Salary Prediction Using Regression Techniques". *Proceedings of Industry Interactive Innovations in Science, Engineering & Technology (I3SET2K19)*.
- [Kaggle - Salary Prediction for Beginners Dataset](https://www.kaggle.com/datasets/rkiattisak/salaly-prediction-for-beginer)
- Pandas Documentation: [https://pandas.pydata.org/docs/](https://pandas.pydata.org/docs/)
- Scikit-learn Documentation: [https://scikit-learn.org/stable/documentation.html](https://scikit-learn.org/stable/documentation.html)
- Seaborn Documentation: [https://seaborn.pydata.org/documentation.html](https://seaborn.pydata.org/documentation.html)
- Matplotlib Documentation: [https://matplotlib.org/stable/contents.html](https://matplotlib.org/stable/contents.html)
