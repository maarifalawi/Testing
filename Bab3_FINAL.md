# BAB 3 - METODE PENELITIAN

> **Versi:** FINAL (Revisi sinkronisasi dengan Bab 4)
> **Tanggal:** Mei 2026
> **Status:** Master Reference — gunakan sebagai acuan saat apply patch ke file Word

---

## 3.1 Tahapan Penelitian

Penelitian ini disusun ke dalam tujuh tahap yang dilaksanakan secara berurutan, yaitu studi literatur, pengumpulan data, analisis sistem, perancangan sistem, pengembangan sistem, *deployment* sistem, dan pengujian sistem. Setiap tahap menghasilkan keluaran yang menjadi masukan bagi tahap berikutnya, sehingga rangkaian tahap tersebut membentuk alur penelitian yang utuh dari pengkajian referensi ilmiah hingga pengukuran tingkat penerimaan sistem oleh pengguna. Gambaran umum ketujuh tahap penelitian disajikan pada Gambar 3.1.

**Gambar 3.1** Tahapan Penelitian Metode *Waterfall*

Gambar 3.1 memperlihatkan urutan ketujuh tahap penelitian yang disusun secara linier mengikuti pendekatan model air terjun. Tahap pertama adalah studi literatur yang berfungsi untuk memperoleh landasan teori dan referensi penelitian terdahulu. Tahap kedua adalah pengumpulan data yang berfungsi untuk memperoleh data primer dari akun yang dijadikan studi kasus. Tahap ketiga adalah analisis sistem yang menerjemahkan hasil studi literatur dan pengumpulan data menjadi spesifikasi kebutuhan. Tahap keempat adalah perancangan sistem yang menerjemahkan spesifikasi kebutuhan menjadi rancangan sistem yang siap dikembangkan. Tahap kelima adalah pengembangan sistem yang menerjemahkan rancangan menjadi kode program yang dapat dieksekusi. Tahap keenam adalah *deployment* sistem yang memindahkan sistem dari lingkungan pengembangan ke lingkungan produksi. Tahap ketujuh adalah pengujian sistem yang memverifikasi pemenuhan kebutuhan dan mengukur tingkat penerimaan sistem oleh pengguna. Penjabaran rinci setiap tahap beserta sub-tahapnya disajikan pada bagian-bagian berikut.

---

## 3.2 Studi Literatur

Studi literatur dilakukan untuk memperoleh data sekunder berupa landasan teori dan referensi penelitian terdahulu yang relevan dengan topik penelitian. Sumber pustaka yang digunakan meliputi jurnal ilmiah internasional dan nasional yang diterbitkan dalam rentang waktu lima tahun terakhir, buku teks rekayasa perangkat lunak, serta dokumentasi resmi dari pustaka dan layanan yang digunakan dalam pengembangan sistem. Hasil studi literatur digunakan untuk menyusun latar belakang masalah, tinjauan pustaka, justifikasi pemilihan metode, dan justifikasi pemilihan metrik analisis pada penelitian ini.

---

## 3.3 Pengumpulan Data

Pengumpulan data dilakukan untuk memperoleh data primer melalui pengamatan langsung terhadap aktivitas pengelolaan konten media sosial pada akun yang dijadikan studi kasus. Tahap ini menjadi penting karena data yang diperoleh akan digunakan sebagai bahan utama dalam pengujian sistem yang dibangun, sehingga sistem dapat divalidasi pada kondisi data yang sesungguhnya. Tahap ini terdiri atas dua sub-tahap, yaitu identifikasi akun studi kasus dan pengumpulan data unggahan konten. Rincian sub-tahap pada tahap pengumpulan data disajikan pada Gambar 3.2.

**Gambar 3.2** Rincian Tahap Pengumpulan Data

### 3.3.1 Identifikasi Akun Studi Kasus

Pemilihan akun studi kasus dilakukan dengan mempertimbangkan tiga kriteria utama, yaitu akun yang dimiliki oleh pelaku UMKM, akun yang aktif melakukan unggahan konten dalam periode pengamatan, dan akun yang pemiliknya bersedia memberikan akses data unggahan untuk keperluan penelitian. Berdasarkan kriteria tersebut, penulis memilih akun Instagram @maariversea yang bergerak di bidang produk digital, dengan jenis produk meliputi *e-book*, jasa pembuatan website, konten edukasi, dan template digital. Akun tersebut memiliki basis pengikut sekitar enam puluh enam ribu pengguna dengan variasi format konten yang memadai, yaitu *image*, *carousel*, dan *reels*. Periode pengamatan dilakukan pada tanggal 3 Maret 2025 sampai 16 Maret 2025 untuk mendapatkan rekapitulasi data *insight* unggahan yang stabil.

### 3.3.2 Pengumpulan Data Unggahan Konten

Pengumpulan data unggahan konten dilakukan dengan melakukan ekstraksi metrik kinerja dari setiap unggahan akun studi kasus dalam periode pengamatan yang telah ditentukan. Metrik yang dikumpulkan meliputi pengidentifikasi unggahan, jenis konten, waktu unggah, jumlah jangkauan, jumlah suka, jumlah komentar, jumlah bagikan, jumlah simpan, jumlah tayangan, jumlah pengikut saat unggah, dan teks keterangan unggahan. Data yang telah dikumpulkan kemudian disusun ke dalam berkas berformat *Comma Separated Values* yang akan digunakan sebagai masukan pada saat pengujian sistem.

---

## 3.4 Analisis Sistem

Analisis sistem dilakukan untuk menerjemahkan hasil studi literatur dan pengumpulan data menjadi spesifikasi kebutuhan yang akan menjadi acuan pada tahap perancangan. Tahap ini dibagi menjadi lima bagian, yaitu analisis masalah, analisis kebutuhan fungsional, analisis kebutuhan non-fungsional, analisis kebutuhan pengguna, dan analisis kebutuhan data. Pembagian ini bertujuan agar setiap aspek kebutuhan sistem dapat dianalisis secara terstruktur dan tidak ada kebutuhan yang terlewat. Rincian sub-tahap pada tahap analisis sistem disajikan pada Gambar 3.3.

**Gambar 3.3** Rincian Tahap Analisis Sistem

### 3.4.1 Analisis Masalah

Analisis masalah dilakukan untuk mengidentifikasi akar permasalahan yang ingin dipecahkan oleh sistem yang dibangun. Identifikasi dilakukan melalui dua jalur, yaitu identifikasi permasalahan yang dialami langsung oleh pengguna di lapangan, dan identifikasi celah penelitian dari kajian pustaka.

#### 3.4.1.1 Identifikasi Permasalahan Pengguna

Identifikasi permasalahan pengguna dilakukan dengan menelaah kendala yang dihadapi pelaku UMKM dalam memantau dan menganalisis kinerja konten media sosial mereka. Hasil telaah disusun ke dalam daftar permasalahan yang menjadi titik tolak penyusunan kebutuhan fungsional sistem.

#### 3.4.1.2 Identifikasi Celah Penelitian

Identifikasi celah penelitian dilakukan dengan menelaah penelitian terdahulu yang relevan dan mencermati keterbatasan serta saran penelitian lanjutan yang dikemukakan oleh peneliti sebelumnya. Celah penelitian yang ditemukan menjadi alasan akademis bagi penyusunan tujuan dan kontribusi penelitian ini.

### 3.4.2 Analisis Kebutuhan Fungsional

Analisis kebutuhan fungsional dilakukan untuk merumuskan daftar fitur yang harus disediakan oleh sistem agar dapat menjawab permasalahan yang telah diidentifikasi. Setiap kebutuhan fungsional dirumuskan dalam bentuk pernyataan kebutuhan yang spesifik, dapat diukur, dan dapat diuji, kemudian diberi kode unik untuk memudahkan penelusuran pada tahap pengembangan dan pengujian.

### 3.4.3 Analisis Kebutuhan Non-Fungsional

Analisis kebutuhan non-fungsional dilakukan untuk merumuskan aspek kualitas yang harus dipenuhi oleh sistem di luar kebutuhan fitur. Aspek yang dianalisis meliputi kinerja, keamanan, kebergunaan, portabilitas, dan kemampurawatan. Setiap aspek dirumuskan dalam bentuk pernyataan kebutuhan terukur dan diberi kode unik agar mudah dirujuk pada tahap perancangan dan pengujian.

### 3.4.4 Analisis Kebutuhan Pengguna

Analisis kebutuhan pengguna dilakukan untuk mengidentifikasi peran-peran yang akan berinteraksi dengan sistem beserta kewenangan dan karakteristik masing-masing peran. Identifikasi peran ini menjadi dasar penyusunan diagram kasus penggunaan dan pengaturan kewenangan akses pada tahap perancangan dan pengembangan.

### 3.4.5 Analisis Kebutuhan Data

Analisis kebutuhan data dilakukan untuk mengidentifikasi entitas-entitas utama yang harus disimpan oleh sistem beserta atribut-atribut penyusunnya. Penentuan atribut metrik kinerja konten dalam penelitian ini mengacu pada metrik-metrik utama yang diidentifikasi oleh Elango, Sithambalam, dan Haque (2023), yang menyatakan bahwa pengukuran keterlibatan pengguna pada platform media sosial mencakup metrik-metrik seperti *reach*, jumlah suka, jumlah komentar, jumlah bagikan, jumlah tayangan, pertumbuhan pengikut, dan *engagement rate* sebagai indikator kinerja konten digital. Berdasarkan acuan tersebut dan disesuaikan dengan fitur bawaan platform Instagram, penulis menentukan tujuh metrik utama yang dianalisis sistem, yaitu jangkauan, jumlah suka, jumlah komentar, jumlah bagikan, jumlah simpan, jumlah tayangan, dan tingkat keterlibatan. Tingkat keterlibatan dihitung secara otomatis pada lapisan basis data menggunakan kolom hasil perhitungan otomatis (*generated column*) dengan formula jumlah interaksi dibagi jumlah jangkauan dikalikan seratus persen, di mana jumlah interaksi merupakan total dari jumlah suka, jumlah komentar, jumlah bagikan, dan jumlah simpan. Apabila jumlah jangkauan bernilai nol, nilai tingkat keterlibatan ditetapkan menjadi nol untuk menghindari pembagian dengan nol. Pemilihan jangkauan sebagai pembagi dilakukan karena jangkauan merepresentasikan jumlah akun yang benar-benar terjangkau oleh unggahan, sehingga lebih akurat dalam mengukur tingkat keterlibatan audiens dibandingkan jumlah pengikut yang juga mencakup pengikut pasif.

---

## 3.5 Perancangan Sistem

Perancangan sistem dilakukan untuk menerjemahkan hasil analisis sistem menjadi rancangan yang siap dikembangkan. Perancangan dibagi menjadi lima bagian, yaitu perancangan arsitektur sistem, perancangan proses bisnis, perancangan basis data, perancangan struktur navigasi, dan perancangan antarmuka pengguna. Pembagian ini mengikuti praktik standar dalam pengembangan perangkat lunak yang memisahkan rancangan struktural, rancangan perilaku, dan rancangan visual agar setiap aspek dapat dirancang secara fokus. Rincian sub-tahap pada tahap perancangan sistem disajikan pada Gambar 3.4.

**Gambar 3.4** Rincian Tahap Perancangan Sistem

### 3.5.1 Perancangan Arsitektur Sistem

Perancangan arsitektur sistem dilakukan menggunakan pendekatan tiga lapis yang memisahkan lapisan antarmuka pengguna, lapisan logika aplikasi, dan lapisan layanan basis data. Pendekatan ini dipilih karena memberikan pemisahan tanggung jawab yang jelas antar lapisan, sehingga sistem mudah dipelihara dan dikembangkan lebih lanjut. Hasil perancangan arsitektur dituangkan dalam bentuk diagram arsitektur yang menggambarkan komponen sistem beserta protokol komunikasi antar komponen.

### 3.5.2 Perancangan Proses Bisnis

Perancangan proses bisnis dilakukan menggunakan notasi *Unified Modeling Language* (UML) dalam bentuk diagram kasus penggunaan dan diagram aktivitas. Diagram kasus penggunaan digunakan untuk menggambarkan interaksi antara aktor dengan sistem secara umum, sedangkan diagram aktivitas digunakan untuk menggambarkan alur kerja setiap kasus penggunaan secara rinci. Notasi UML dipilih karena merupakan notasi standar yang banyak digunakan dalam dokumentasi pengembangan perangkat lunak.

### 3.5.3 Perancangan Basis Data

Perancangan basis data dilakukan menggunakan pendekatan diagram entitas relasi dengan notasi *Crow's Foot* untuk menggambarkan kardinalitas relasi antar entitas. Perancangan dimulai dengan mengidentifikasi entitas utama dari hasil analisis kebutuhan data, dilanjutkan dengan menentukan atribut, kunci primer, kunci asing, serta relasi antar entitas. Sistem manajemen basis data yang digunakan adalah PostgreSQL melalui layanan terkelola Supabase yang mendukung kebijakan keamanan baris (*Row Level Security*) untuk pengaturan kewenangan akses data.

### 3.5.4 Perancangan Struktur Navigasi

Perancangan struktur navigasi dilakukan menggunakan pola hierarkis dengan halaman *dashboard* sebagai titik pusat navigasi setelah pengguna berhasil masuk ke sistem. Pola ini dipilih agar pengguna dapat selalu kembali ke titik pusat dengan satu kali sentuhan dari halaman manapun, sehingga mengurangi kebingungan dalam menentukan langkah berikutnya. Hasil perancangan struktur navigasi dituangkan dalam bentuk diagram struktur navigasi yang menggambarkan hubungan antar halaman.

### 3.5.5 Perancangan Antarmuka Pengguna

Perancangan antarmuka pengguna dilakukan dengan pendekatan *mobile first* agar tata letak tetap optimal pada layar berukuran kecil dan kemudian diadaptasi untuk layar berukuran besar. Skema warna utama yang digunakan adalah kombinasi warna biru dan putih yang memberikan kesan profesional dan tenang, sedangkan tipografi yang digunakan adalah keluarga huruf *sans-serif* yang memberikan keterbacaan optimal pada layar. Hasil perancangan antarmuka dituangkan dalam bentuk *wireframe* untuk setiap halaman utama sistem.

---

## 3.6 Pengembangan Sistem

Pengembangan sistem dilakukan untuk menerjemahkan hasil perancangan menjadi kode program yang dapat dieksekusi. Pengembangan dibagi menjadi lima bagian, yaitu penyiapan lingkungan pengembangan, pengkodean antarmuka pengguna, pengkodean logika aplikasi, pengkodean layanan basis data, dan pengkodean layanan kecerdasan buatan. Pembagian ini bertujuan agar setiap modul sistem dikembangkan secara terstruktur dan mudah ditelusuri pada tahap pengujian. Rincian sub-tahap pada tahap pengembangan sistem disajikan pada Gambar 3.5.

**Gambar 3.5** Rincian Tahap Pengembangan Sistem

### 3.6.1 Penyiapan Lingkungan Pengembangan

Penyiapan lingkungan pengembangan dilakukan dengan memasang seluruh perangkat lunak dan pustaka yang dibutuhkan untuk membangun sistem. Lingkungan pengembangan utama yang digunakan adalah Node.js versi terkini sebagai *runtime* JavaScript, npm sebagai pengelola paket, dan Visual Studio Code sebagai editor kode. Pustaka inti yang dipasang meliputi React sebagai kerangka kerja antarmuka pengguna, Vite sebagai *bundler*, Tailwind CSS sebagai kerangka pemformatan, dan *client* resmi Supabase sebagai jembatan ke layanan basis data.

### 3.6.2 Pengkodean Antarmuka Pengguna

Pengkodean antarmuka pengguna dilakukan menggunakan kerangka kerja React dengan bahasa pemrograman TypeScript untuk memastikan keamanan tipe data pada saat kompilasi. Pustaka komponen *shadcn-ui* digunakan untuk menyediakan komponen antarmuka yang konsisten secara visual, sedangkan Tailwind CSS digunakan untuk pemformatan secara utilitas. Setiap halaman sistem dikodekan sebagai komponen React mandiri yang dapat dipelihara dan dikembangkan secara terpisah.

### 3.6.3 Pengkodean Logika Aplikasi

Pengkodean logika aplikasi dilakukan untuk mengimplementasikan aturan bisnis sistem, antara lain validasi data masukan, transformasi data dari format mentah menjadi format yang siap ditampilkan, penyusunan ringkasan wawasan otomatis berbasis aturan dan template dari hasil analitik, dan pengaturan navigasi antar halaman. Logika aplikasi diorganisasi ke dalam modul-modul terpisah berdasarkan tanggung jawabnya untuk menjaga prinsip pemisahan tugas.

### 3.6.4 Pengkodean Layanan Basis Data

Pengkodean layanan basis data dilakukan dengan menyusun berkas migrasi yang berisi perintah pembuatan tabel, kunci primer, kunci asing, indeks, kolom hasil perhitungan otomatis (*generated column*) untuk total interaksi dan tingkat keterlibatan, serta kebijakan keamanan baris (*Row Level Security*). Berkas migrasi disusun menggunakan bahasa SQL dan dijalankan secara berurutan agar struktur basis data dapat direkonstruksi pada lingkungan pengembangan, lingkungan pengujian, maupun lingkungan produksi.

### 3.6.5 Pengkodean Layanan Kecerdasan Buatan

Pengkodean layanan kecerdasan buatan dilakukan untuk mengintegrasikan model bahasa Gemini ke dalam sistem sebagai mesin penyusun keterangan unggahan otomatis (*Generator Caption AI*). Integrasi dilakukan melalui *Edge Function* yang berjalan pada lingkungan Deno di sisi peladen Supabase. *Edge Function* berfungsi sebagai perantara yang menerima permintaan dari antarmuka pengguna, menyusun *prompt* berdasarkan masukan deskripsi konten, gaya bahasa, panjang caption, opsi *hashtag*, opsi emoji, dan tujuan caption yang dipilih pengguna, kemudian mengirimkan permintaan ke layanan Gemini dan mengembalikan beberapa alternatif caption ke antarmuka pengguna. Pengkodean dilakukan dengan menerapkan strategi *multi-model fallback* yang mencoba beberapa varian model Gemini secara berurutan untuk meningkatkan keandalan layanan, serta dilengkapi mekanisme *exponential backoff* pada setiap percobaan ulang. Sementara itu, fitur ringkasan wawasan disusun menggunakan pendekatan berbasis aturan dan template dari hasil perhitungan analitik tanpa melibatkan pemanggilan layanan AI eksternal.

---

## 3.7 Deployment Sistem

*Deployment* sistem dilakukan untuk memindahkan sistem dari lingkungan pengembangan ke lingkungan produksi yang dapat diakses oleh pengguna akhir. *Deployment* dibagi menjadi dua bagian, yaitu penyiapan lingkungan produksi dan penerapan sistem ke lingkungan produksi. Rincian sub-tahap pada tahap *deployment* sistem disajikan pada Gambar 3.6.

**Gambar 3.6** Rincian Tahap Deployment Sistem

### 3.7.1 Penyiapan Lingkungan Produksi

Penyiapan lingkungan produksi dilakukan dengan menyiapkan platform Vercel sebagai layanan *hosting* untuk antarmuka pengguna, menyiapkan proyek Supabase untuk lingkungan produksi sebagai layanan *backend*, mengonfigurasi variabel lingkungan, mengonfigurasi nama domain, dan mengonfigurasi sertifikat *Hypertext Transfer Protocol Secure*. Pemilihan Vercel didasarkan pada dukungannya yang baik untuk kerangka kerja React dengan *bundler* Vite, fitur *Continuous Deployment* otomatis dari repositori Git, dan integrasi sertifikat *Hypertext Transfer Protocol Secure* bawaan. Variabel lingkungan yang dikonfigurasi meliputi alamat layanan Supabase, kunci anonim Supabase, kunci API model bahasa Gemini, dan kunci API layanan pengiriman surel.

### 3.7.2 Penerapan Sistem ke Lingkungan Produksi

Penerapan sistem ke lingkungan produksi dilakukan dengan membangun antarmuka pengguna ke dalam berkas statis melalui proses *build*, mengunggah berkas hasil *build* ke layanan *hosting*, menjalankan migrasi basis data ke proyek Supabase produksi, dan menerapkan *Edge Function* ke lingkungan produksi. Setelah seluruh komponen siap, sistem diuji secara cepat untuk memastikan dapat diakses dengan baik melalui nama domain yang telah dikonfigurasi.

---

## 3.8 Pengujian Sistem

Pengujian sistem dilakukan untuk memverifikasi bahwa sistem yang dibangun telah memenuhi seluruh kebutuhan fungsional dan non-fungsional yang telah dirumuskan pada tahap analisis. Pengujian dibagi menjadi empat bagian, yaitu pengujian kotak hitam (*black box testing*), validasi perhitungan KPI dan analitik, evaluasi keluaran model bahasa Gemini, dan pengujian penerimaan pengguna. Rincian sub-tahap pada tahap pengujian sistem disajikan pada Gambar 3.7.

**Gambar 3.7** Rincian Tahap Pengujian Sistem

### 3.8.1 Pengujian Black Box Testing

Pengujian *black box testing* dilakukan untuk memverifikasi fungsionalitas sistem dari sudut pandang pengguna tanpa memperhatikan struktur kode internal. Pengujian ini berfokus pada masukan dan keluaran setiap modul sistem. Skenario pengujian disusun berdasarkan kategori fitur dan kondisi penggunaan yang mungkin terjadi, mencakup skenario penggunaan normal, masukan tidak valid, data kosong, batas karakter, akses tanpa hak, kondisi tanpa dataset, proteksi halaman, responsivitas tampilan, *loading state*, dan penanganan kesalahan.

#### 3.8.1.1 Penyusunan Skenario Pengujian

Penyusunan skenario pengujian dilakukan dengan menjabarkan setiap kebutuhan fungsional menjadi satu atau lebih skenario pengujian. Setiap skenario memuat informasi modul yang diuji, langkah-langkah pengujian, masukan yang diberikan, dan keluaran yang diharapkan. Hasil penyusunan dituangkan dalam dokumen pengujian yang disusun secara terpisah dari naskah penelitian ini.

#### 3.8.1.2 Pelaksanaan Pengujian Modul

Pelaksanaan pengujian modul dilakukan dengan mengeksekusi setiap skenario pengujian secara berurutan dan mencatat hasilnya. Hasil pengujian dibandingkan dengan keluaran yang diharapkan, kemudian status pengujian ditetapkan sebagai berhasil apabila keluaran yang dihasilkan sesuai, atau gagal apabila terdapat ketidaksesuaian. Skenario yang gagal akan ditelusuri penyebabnya dan diperbaiki, kemudian diuji ulang sampai berstatus berhasil.

### 3.8.2 Validasi Perhitungan KPI dan Analitik

Validasi perhitungan KPI dan analitik dilakukan untuk memastikan bahwa nilai metrik yang ditampilkan oleh sistem konsisten dengan hasil perhitungan manual. Validasi dilakukan dengan membandingkan nilai *engagement rate* yang dihasilkan sistem terhadap nilai *engagement rate* yang dihitung secara manual menggunakan formula yang sama, yaitu jumlah interaksi dibagi jumlah jangkauan dikalikan seratus persen. Validasi dilakukan terhadap seluruh data unggahan pada dataset uji, dengan toleransi pembulatan kurang dari atau sama dengan nol koma nol satu poin persentase. Hasil validasi dinyatakan sesuai apabila selisih antara nilai sistem dan nilai validasi manual berada dalam batas toleransi tersebut. Hasil validasi disajikan dalam bentuk tabel ringkasan dan tabel sampel perhitungan untuk menunjukkan akurasi perhitungan sistem secara menyeluruh.

### 3.8.3 Evaluasi Keluaran Model Bahasa Gemini

Evaluasi keluaran model bahasa Gemini dilakukan untuk menilai kelayakan hasil yang dihasilkan oleh fitur *Generator Caption AI* sebagai draf awal keterangan unggahan. Evaluasi dilakukan menggunakan dua skenario pengujian, yaitu skenario promosi produk dan skenario edukasi atau motivasi, yang masing-masing menggunakan masukan yang relevan dengan karakter konten akun studi kasus. Penilaian dilakukan berdasarkan empat aspek, yaitu kesesuaian konteks, kejelasan bahasa, relevansi hasil, dan kelayakan penggunaan. Hasil evaluasi disajikan dalam bentuk tabel evaluasi dengan catatan kualitatif untuk setiap skenario sehingga dapat menunjukkan kemampuan sistem dalam menghasilkan caption yang dapat digunakan sebagai draf awal oleh pengguna.

### 3.8.4 Pengujian Penerimaan Pengguna

Pengujian penerimaan pengguna (*user acceptance test*) dilakukan untuk mengukur tingkat penerimaan sistem oleh calon pengguna akhir. Pengujian dilakukan dengan melibatkan dua puluh responden yang terdiri dari mahasiswa, konten kreator, pengelola media sosial, pelaku UMKM, dan pengguna lain yang relevan dengan target pengguna sistem. Responden diminta untuk menggunakan sistem dengan menjalankan beberapa skenario penggunaan, kemudian mengisi kuesioner yang disusun mengacu pada instrumen *System Usability Scale*. Hasil pengisian kuesioner kemudian dihitung skor akhirnya, dan diinterpretasikan menggunakan skala penerimaan yang merujuk pada klasifikasi Sukma dkk. (2023) yang mencakup tiga dimensi, yaitu *Acceptability Range*, *Grade Scale*, dan *Adjective Rating*, untuk menentukan tingkat penerimaan sistem.

---

## 📋 CATATAN REVISI DARI BAB 3 SEBELUMNYA

Perubahan utama yang dilakukan pada Bab 3 ini:

1. **Sub-bab 3.3.1** — Studi kasus dispesifikkan ke @maariversea dengan periode 3-16 Maret 2025, jenis konten, dan jumlah pengikut.

2. **Sub-bab 3.4.5 (Analisis Kebutuhan Data)** — Rumus *engagement rate* dikoreksi dari "dibagi jumlah pengikut" menjadi "dibagi jumlah jangkauan", dan dijelaskan bahwa perhitungan dilakukan pada lapisan basis data sebagai *generated column*.

3. **Sub-bab 3.6.5 (Pengkodean Layanan AI)** — Diperjelas bahwa Gemini digunakan untuk *Generator Caption AI* (bukan ringkasan insight), dilengkapi penjelasan strategi *multi-model fallback* dan *exponential backoff*.

4. **Sub-bab 3.6.4** — Ditambah penjelasan bahwa basis data memiliki *generated column* untuk perhitungan otomatis.

5. **Sub-bab 3.7.1 (Penyiapan Lingkungan Produksi)** — Dispesifikkan platform Vercel sebagai layanan *hosting* dengan justifikasi pemilihan.

6. **Sub-bab 3.8 (Pengujian Sistem)** — Diperluas dari 2 jenis pengujian menjadi 4 jenis pengujian (Black Box + Validasi KPI + Evaluasi Gemini + SUS).

7. **Sub-bab 3.8.4** — Dispesifikkan jumlah responden 20 orang dengan komposisi yang jelas, dan ditambah referensi Sukma dkk. (2023) untuk klasifikasi SUS.

8. **Italic istilah asing** — Semua istilah teknis bahasa asing sudah diberi format italic.

9. **Penghapusan catatan internal** — Catatan "Berkas ini berisi naskah seluruh sub-bagian Bab 3 sesuai revisi terbaru..." sudah dihapus karena tidak boleh muncul di skripsi final.
