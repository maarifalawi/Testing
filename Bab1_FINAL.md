# BAB 1 - PENDAHULUAN

> **Versi:** FINAL (Revisi sinkronisasi dengan Bab 4)
> **Tanggal:** Mei 2026
> **Status:** Master Reference — gunakan sebagai acuan saat apply patch ke file Word

---

## 1.1 Latar Belakang

Era digital telah mendorong pergeseran besar dalam cara masyarakat mengakses informasi, berinteraksi, dan melakukan transaksi. Seiring dengan meningkatnya penetrasi internet dan penggunaan perangkat bergerak, media sosial berkembang menjadi bagian yang tidak terpisahkan dari kehidupan sehari-hari sekaligus mengubah lanskap pemasaran secara fundamental. Platform-platform media sosial seperti Instagram, Facebook, dan TikTok kini tidak hanya berfungsi sebagai sarana komunikasi, melainkan juga telah bertransformasi menjadi kanal pemasaran utama bagi pelaku usaha dari berbagai skala. Tingginya penetrasi media sosial di Indonesia, dengan lebih dari 212 juta pengguna internet dan tingkat penetrasi media sosial sekitar 77 persen dari total populasi (Saifulloh, Putri, dan Hamzah, 2026), menjadikan platform digital sebagai ruang yang sangat potensial sekaligus sangat kompetitif bagi pelaku usaha.

Kebutuhan untuk memahami kinerja konten media sosial secara sistematis melahirkan bidang yang dikenal sebagai *social media analytics*. Elango, Sithambalam, dan Haque (2023) mendefinisikan *social media analytics* sebagai praktik pengumpulan, pengukuran, dan evaluasi data dari jaringan media sosial untuk mendukung pengambilan keputusan bisnis yang lebih terinformasi. Penelitian tersebut mengidentifikasi metrik-metrik utama yang digunakan dalam pengukuran keterlibatan pengguna, antara lain *engagement rate*, *reach*, *impressions*, pertumbuhan pengikut, dan *click-through rate*, sebagai indikator kinerja konten digital. Nugroho dan Angela (2024) memperkuat hal tersebut dengan menemukan bahwa pemanfaatan *social media analytics* secara signifikan meningkatkan inovasi organisasi dan adaptabilitas usaha kecil dan menengah, yang pada akhirnya berdampak positif terhadap kualitas pengambilan keputusan strategis. Penelitian tersebut juga menegaskan bahwa *social media analytics* telah mendemokratisasi akses terhadap *big data* yang sebelumnya hanya dapat dimanfaatkan oleh perusahaan berskala besar.

Meskipun urgensi *social media analytics* telah diakui secara luas, penerapannya oleh pelaku usaha berskala kecil masih menghadapi sejumlah hambatan. Saifulloh, Putri, dan Hamzah (2026) dalam penelitiannya mengenai implementasi *social media analytics* pada mahasiswa entrepreneur menemukan bahwa pemanfaatan data analitik masih terbatas pada indikator permukaan seperti jumlah pengikut dan tingkat keterlibatan, sementara analisis mendalam terkait tren dan konversi pemasaran jarang dilakukan secara konsisten. Strategi komunikasi digital yang terbentuk lebih bersifat intuitif dan reaktif terhadap tren, bukan berbasis evaluasi sistematis berbasis data. Temuan ini mengindikasikan adanya kesenjangan literasi digital yang signifikan antara potensi yang ditawarkan oleh *social media analytics* dan kemampuan aktual pelaku usaha berskala kecil dalam memanfaatkannya secara optimal.

Di sisi lain, kemajuan teknologi kecerdasan buatan dalam beberapa tahun terakhir membuka peluang baru bagi penyederhanaan proses analisis dan penyusunan konten pemasaran. Soori dkk. (2026) dalam kajian komprehensif mengenai sistem pendukung keputusan berbasis kecerdasan buatan menyoroti bahwa sistem berbasis *machine learning* dan *natural language processing* kini mampu memproses data berskala besar, mengenali pola tersembunyi, dan menghasilkan wawasan yang dapat ditindaklanjuti secara otomatis. Kemampuan ini memungkinkan sistem analitik untuk tidak hanya menyajikan data mentah, tetapi juga memberikan ringkasan wawasan otomatis berbasis aturan analitik serta dukungan kecerdasan buatan generatif untuk membantu penyusunan keterangan unggahan, sehingga dapat dipahami langsung oleh pengguna tanpa latar belakang teknis sekalipun.

Permasalahan di atas menjadi semakin relevan ketika dikaitkan dengan konteks usaha mikro, kecil, dan menengah (UMKM) di Indonesia. UMKM merupakan salah satu pilar utama perekonomian Indonesia dengan kontribusi terhadap produk domestik bruto yang melebihi enam puluh persen serta menyerap sekitar sembilan puluh tujuh persen dari total tenaga kerja nasional (Awaludin dkk., 2025). Besarnya peran tersebut menjadikan kelangsungan dan pertumbuhan UMKM sebagai isu strategis yang perlu mendapat perhatian serius. Namun demikian, Awaludin dkk. (2025) menemukan bahwa sebagian besar pelaku UMKM masih menghadapi hambatan dalam mengintegrasikan sistem manajemen, strategi pemasaran digital, dan analisis data secara komprehensif, yang pada akhirnya menghambat efisiensi operasional dan proses pengambilan keputusan berbasis data.

Berdasarkan kondisi tersebut, dibutuhkan sebuah platform analitik media sosial yang dirancang secara khusus untuk pelaku UMKM dengan karakteristik mudah digunakan, terjangkau, dilengkapi dengan ringkasan wawasan otomatis berdasarkan hasil perhitungan analitik, serta didukung kecerdasan buatan generatif untuk membantu penyusunan keterangan unggahan. Penelitian ini merancang dan membangun platform analitik media sosial berbasis web yang mengintegrasikan fitur visualisasi metrik kinerja konten, ringkasan wawasan otomatis berbasis aturan dan template, analisis waktu terbaik posting, analisis audiens dan pertumbuhan, penetapan dan pemantauan target *Key Performance Indicator*, pengelolaan kampanye konten, perbandingan kompetitor, *Generator Caption AI* berbasis model bahasa Gemini, perbandingan dataset, serta penyusun laporan berdasarkan rentang tanggal yang dipilih pengguna. Seluruh fitur tersebut dirancang untuk membantu UMKM dalam menganalisis kinerja konten media sosial dan menyusun strategi konten yang lebih berbasis data.

---

## 1.2 Ruang Lingkup

Pembahasan pada penelitian ini dibatasi oleh ruang lingkup sebagai berikut:

1. Platform yang dibangun merupakan aplikasi berbasis web yang dapat diakses melalui peramban modern pada perangkat komputer maupun perangkat bergerak, dengan sumber data berupa unggahan konten Instagram yang diunggah ke sistem dalam bentuk berkas berformat *Comma Separated Values* (CSV).

2. Metrik kinerja yang dianalisis meliputi jangkauan, jumlah suka, jumlah komentar, jumlah bagikan, jumlah simpan, jumlah tayangan, dan tingkat keterlibatan, yang disajikan melalui beberapa kelompok fitur, yaitu (a) fitur pengelolaan data berupa impor data dari berkas *Comma Separated Values*, *Google Sheets*, dan data sampel; (b) fitur analitik berupa papan informasi ringkasan kinerja (*Dashboard*), analisis performa per konten, analisis waktu terbaik posting, analisis audiens dan pertumbuhan, serta ringkasan wawasan otomatis berbasis aturan dan template; (c) fitur perencanaan strategi berupa pengelolaan target *Key Performance Indicator* dan kampanye konten; (d) fitur alat berupa penyusun keterangan unggahan (*Generator Caption AI*) berbasis model bahasa Gemini dan analisis kompetitor; (e) fitur laporan berupa penyusun laporan berdasarkan rentang tanggal yang dipilih pengguna dalam format *Portable Document Format* (PDF) dan perbandingan antar dataset; serta (f) fitur kolaborasi dan bantuan berupa pengelolaan anggota proyek dan layanan tanya jawab dengan admin.

3. Studi kasus penelitian dilakukan pada satu akun Instagram pelaku UMKM yang bergerak di bidang produk digital.

4. Pengujian sistem dilakukan melalui pengujian kotak hitam (*black box testing*) untuk memverifikasi pemenuhan kebutuhan fungsional, validasi perhitungan KPI dan analitik untuk memverifikasi kesesuaian rumus *engagement rate*, evaluasi keluaran model bahasa Gemini pada fitur *Generator Caption AI*, dan pengujian penerimaan menggunakan instrumen *System Usability Scale* (SUS) untuk mengukur tingkat kebergunaan sistem.

---

## 1.3 Tujuan Penelitian

Tujuan dari penelitian ini adalah merancang dan membangun sebuah platform analitik media sosial berbasis web yang dilengkapi dengan dukungan kecerdasan buatan untuk membantu pelaku UMKM dalam menganalisis kinerja konten media sosial dan menyusun strategi konten yang lebih berbasis data. Tujuan tersebut dijabarkan ke dalam beberapa tujuan khusus sebagai berikut:

1. Mengidentifikasi kebutuhan fungsional dan kebutuhan non-fungsional dari sebuah platform analitik media sosial yang sesuai dengan karakteristik pelaku UMKM.

2. Merancang arsitektur sistem, basis data, struktur navigasi, dan antarmuka pengguna platform analitik media sosial yang mudah digunakan tanpa memerlukan latar belakang teknis.

3. Mengimplementasikan rancangan tersebut ke dalam platform analitik media sosial menggunakan kerangka kerja React, layanan terkelola Supabase, dan model bahasa Gemini sebagai pendukung fitur *Generator Caption AI*, serta menerapkan platform yang telah dibangun ke lingkungan produksi sehingga dapat diakses secara daring.

---

## 1.4 Sistematika Penulisan

Penelitian ini disusun ke dalam lima bagian utama yang saling berkaitan satu sama lain. Sistematika penulisan dijabarkan sebagai berikut.

**BAB I PENDAHULUAN** memuat latar belakang penelitian, ruang lingkup yang membatasi pembahasan, tujuan yang ingin dicapai melalui penelitian, dan sistematika penulisan secara keseluruhan.

**BAB II LANDASAN TEORI** memuat tinjauan pustaka yang berisi konsep dan teori yang melandasi penelitian, antara lain konsep UMKM, konsep media sosial dan pemasaran digital, konsep *social media analytics*, konsep kecerdasan buatan generatif, dan konsep teknologi yang digunakan dalam pengembangan sistem. Bagian ini juga memuat tinjauan terhadap penelitian terdahulu yang relevan dengan topik penelitian.

**BAB III METODE PENELITIAN** memuat tahapan penelitian yang dilaksanakan, mulai dari tahap studi literatur, pengumpulan data, analisis sistem, perancangan sistem, pengembangan sistem, penerapan sistem ke lingkungan produksi, hingga pengujian sistem. Setiap tahap dijelaskan secara rinci beserta sub-tahap dan keluarannya.

**BAB IV HASIL DAN PEMBAHASAN** memuat hasil pelaksanaan setiap tahap penelitian, mulai dari hasil pengumpulan data, hasil analisis kebutuhan sistem, hasil perancangan sistem, hasil pengembangan sistem, hasil penerapan sistem, hingga hasil pengujian sistem. Bagian ini juga memuat pembahasan terhadap temuan-temuan yang diperoleh selama pelaksanaan penelitian.

**BAB V PENUTUP** memuat kesimpulan yang menjawab tujuan penelitian dan saran yang dapat dijadikan acuan bagi pengembangan penelitian selanjutnya.

---

## 📋 CATATAN REVISI DARI BAB 1 SEBELUMNYA

Perubahan utama yang dilakukan pada Bab 1 ini:

1. **Paragraf 4** — Dihapus klaim "memberikan rekomendasi dan ringkasan wawasan" dari konteks AI; diganti dengan klarifikasi bahwa ringkasan wawasan menggunakan aturan analitik, sementara AI digunakan untuk caption.

2. **Paragraf 5** — Singkatan UMKM diperkenalkan di kemunculan pertama, lalu konsisten digunakan di seluruh dokumen.

3. **Paragraf 6** — Daftar fitur dilengkapi sesuai implementasi Bab 4 final (audiens & pertumbuhan, kampanye, perbandingan dataset, dll.).

4. **Sub-bab 1.2 butir 2** — Daftar fitur direstruktur menjadi 6 kelompok (pengelolaan data, analitik, perencanaan, alat, laporan, kolaborasi) dengan istilah konsisten.

5. **Sub-bab 1.2 butir 4** — Pengujian ditambah menjadi 4 jenis (Black Box, Validasi KPI, Evaluasi Gemini, SUS) sesuai Bab 4 final.

6. **Sub-bab 1.3 butir 3** — Diklarifikasi bahwa Gemini digunakan sebagai pendukung *Generator Caption AI*, bukan untuk seluruh fitur AI.

7. **Penghapusan istilah** — "laporan periodik" diganti menjadi "laporan berdasarkan rentang tanggal yang dipilih pengguna".

8. **Italic istilah asing** — Semua istilah teknis bahasa asing sudah diberi format italic.
