# 📋 PATCH REVISI BAB 1, 2, DAN 3

**Tujuan:** Sinkronisasi Bab 1-3 dengan revisi Bab 4 final (sudah 3x revisi).
**Total Perubahan:** 16 revisi (5 KRITIS + 7 PENTING + 4 POLISHING)
**Estimasi Waktu Apply:** 2 jam

---

## 🚀 CARA PAKAI PATCH INI

1. Buka file `.docx` Bab yang akan direvisi (contoh: `SKRIPSI BAB 1 PART 2.docx`)
2. **Save As** dengan nama baru: `SKRIPSI BAB 1 PART 3.docx` (jangan timpa file lama)
3. Cari setiap **TEKS LAMA** menggunakan **Ctrl + F** atau **Find & Replace** (Ctrl + H)
4. Ganti dengan **TEKS BARU**
5. Setelah selesai semua, save dokumen

---

## 🔴 KATEGORI: KRITIS — Wajib Apply (5 Revisi)

### 🔧 REVISI #1 — Bab 3.3.5: Rumus Engagement Rate

**LOKASI:** Bab 3 → Sub-bab 3.3 Analisis Sistem → 3.3.5 Analisis Kebutuhan Data → paragraf terakhir, kalimat terakhir.

**TEKS LAMA (HAPUS):**
> Tingkat keterlibatan dihitung secara dinamis pada lapisan logika aplikasi menggunakan formula jumlah interaksi dibagi jumlah pengikut dikalikan seratus persen.

**TEKS BARU (GANTI):**
> Tingkat keterlibatan dihitung secara otomatis pada lapisan basis data menggunakan kolom hasil perhitungan otomatis (*generated column*) dengan formula jumlah interaksi dibagi jumlah jangkauan dikalikan seratus persen, di mana jumlah interaksi merupakan total dari jumlah suka, jumlah komentar, jumlah bagikan, dan jumlah simpan. Apabila jumlah jangkauan bernilai nol, nilai tingkat keterlibatan ditetapkan menjadi nol untuk menghindari pembagian dengan nol. Pemilihan jangkauan sebagai pembagi dilakukan karena jangkauan merepresentasikan jumlah akun yang benar-benar terjangkau oleh unggahan, sehingga lebih akurat dalam mengukur tingkat keterlibatan audiens dibandingkan jumlah pengikut yang juga mencakup pengikut pasif.

**ALASAN:** Rumus aktual sistem menggunakan **reach (jangkauan)**, bukan followers (pengikut). Bab 4 final dan kode SQL migrasi sudah konsisten pakai reach. Kalau dibiarkan, akan kontradiksi langsung dengan Bab 4.

---

### 🔧 REVISI #2 — Bab 3.6.5: Layanan Kecerdasan Buatan

**LOKASI:** Bab 3 → Sub-bab 3.6 Pengembangan Sistem → 3.6.5 Pengkodean Layanan Kecerdasan Buatan → ganti seluruh paragraf.

**TEKS LAMA (HAPUS SELURUH PARAGRAF):**
> Pengkodean layanan kecerdasan buatan dilakukan untuk mengintegrasikan model bahasa Gemini ke dalam sistem sebagai mesin penghasil ringkasan insight. Integrasi dilakukan melalui Edge Function yang berjalan pada lingkungan Deno di sisi peladen Supabase. Edge Function berfungsi sebagai perantara yang menerima permintaan dari antarmuka pengguna, menyusun prompt yang sesuai dengan konteks data pengguna, mengirimkan permintaan ke layanan Gemini, dan mengembalikan hasilnya kepada antarmuka pengguna dalam format yang dapat langsung ditampilkan.

**TEKS BARU (GANTI):**
> Pengkodean layanan kecerdasan buatan dilakukan untuk mengintegrasikan model bahasa Gemini ke dalam sistem sebagai mesin penyusun keterangan unggahan otomatis (*Generator Caption AI*). Integrasi dilakukan melalui *Edge Function* yang berjalan pada lingkungan Deno di sisi peladen Supabase. *Edge Function* berfungsi sebagai perantara yang menerima permintaan dari antarmuka pengguna, menyusun *prompt* berdasarkan masukan deskripsi konten, gaya bahasa, panjang caption, opsi *hashtag*, opsi emoji, dan tujuan caption yang dipilih pengguna, kemudian mengirimkan permintaan ke layanan Gemini dan mengembalikan beberapa alternatif caption ke antarmuka pengguna. Pengkodean dilakukan dengan menerapkan strategi *multi-model fallback* yang mencoba beberapa varian model Gemini secara berurutan untuk meningkatkan keandalan layanan, serta dilengkapi mekanisme *exponential backoff* pada setiap percobaan ulang. Sementara itu, fitur ringkasan wawasan disusun menggunakan pendekatan berbasis aturan dan template dari hasil perhitungan analitik tanpa melibatkan pemanggilan layanan AI eksternal.

**ALASAN:** Bab 4 menyatakan Gemini hanya digunakan untuk Generator Caption AI, bukan ringkasan insight. Ringkasan Insight menggunakan rule-based approach, bukan AI.

---

### 🔧 REVISI #3 — Bab 1 Latar Belakang Paragraf 4: Hapus Klaim Ringkasan Wawasan AI

**LOKASI:** Bab 1 → 1.1 Latar Belakang → paragraf 4 (yang membahas Soori et al.).

**TEKS LAMA (HAPUS BAGIAN AKHIR):**
> Kemampuan ini memungkinkan sistem analitik untuk tidak hanya menyajikan data mentah, tetapi juga memberikan rekomendasi dan ringkasan wawasan yang dapat dipahami langsung oleh pengguna tanpa latar belakang teknis sekalipun.

**TEKS BARU (GANTI):**
> Kemampuan ini memungkinkan sistem analitik untuk tidak hanya menyajikan data mentah, tetapi juga memberikan ringkasan wawasan otomatis berbasis aturan analitik serta dukungan kecerdasan buatan generatif untuk membantu penyusunan keterangan unggahan, sehingga dapat dipahami langsung oleh pengguna tanpa latar belakang teknis sekalipun.

---

### 🔧 REVISI #4 — Bab 1 Latar Belakang Paragraf 6: Daftar Fitur Penelitian

**LOKASI:** Bab 1 → 1.1 Latar Belakang → paragraf 6 (paragraf terakhir sebelum Ruang Lingkup).

**TEKS LAMA (HAPUS SELURUH PARAGRAF):**
> Berdasarkan kondisi tersebut, dibutuhkan sebuah platform analitik media sosial yang dirancang secara khusus untuk pelaku usaha mikro, kecil, dan menengah dengan karakteristik mudah digunakan, terjangkau, dan dilengkapi dengan dukungan kecerdasan buatan untuk meringkas wawasan kinerja konten dan membantu penyusunan keterangan unggahan. Penelitian ini merancang dan membangun platform analitik media sosial berbasis web yang mengintegrasikan fitur visualisasi metrik kinerja konten, ringkasan wawasan berbantuan kecerdasan buatan, analisis waktu terbaik posting, perbandingan kompetitor, penetapan dan pemantauan target KPI, serta caption generator berbasis kecerdasan buatan, yang seluruhnya dirancang untuk membantu pelaku usaha mikro, kecil, dan menengah dalam menganalisis kinerja konten media sosial dan menyusun strategi konten yang lebih berbasis data.

**TEKS BARU (GANTI):**
> Berdasarkan kondisi tersebut, dibutuhkan sebuah platform analitik media sosial yang dirancang secara khusus untuk pelaku usaha mikro, kecil, dan menengah (UMKM) dengan karakteristik mudah digunakan, terjangkau, dilengkapi dengan ringkasan wawasan otomatis berdasarkan hasil perhitungan analitik, serta didukung kecerdasan buatan generatif untuk membantu penyusunan keterangan unggahan. Penelitian ini merancang dan membangun platform analitik media sosial berbasis web yang mengintegrasikan fitur visualisasi metrik kinerja konten, ringkasan wawasan otomatis berbasis aturan dan template, analisis waktu terbaik posting, analisis audiens dan pertumbuhan, penetapan dan pemantauan target *Key Performance Indicator*, pengelolaan kampanye konten, perbandingan kompetitor, *Generator Caption AI* berbasis model bahasa Gemini, perbandingan dataset, serta penyusun laporan berdasarkan rentang tanggal yang dipilih pengguna. Seluruh fitur tersebut dirancang untuk membantu UMKM dalam menganalisis kinerja konten media sosial dan menyusun strategi konten yang lebih berbasis data.

---

### 🔧 REVISI #5 — Bab 1.2 Ruang Lingkup Butir 2: Daftar Fitur Lengkap

**LOKASI:** Bab 1 → 1.2 Ruang Lingkup → butir nomor 2.

**TEKS LAMA (HAPUS):**
> Metrik kinerja yang dianalisis meliputi jangkauan, jumlah suka, jumlah komentar, jumlah bagikan, jumlah simpan, jumlah tayangan, dan tingkat keterlibatan, yang disajikan melalui fitur papan informasi ringkasan kinerja, analisis performa per konten, ringkasan wawasan berbantu kecerdasan buatan menggunakan model bahasa Gemini, penyusun keterangan unggahan berbantu kecerdasan buatan, dan penyusun laporan periodik dalam format *Portable Document Format* (PDF).

**TEKS BARU (GANTI):**
> Metrik kinerja yang dianalisis meliputi jangkauan, jumlah suka, jumlah komentar, jumlah bagikan, jumlah simpan, jumlah tayangan, dan tingkat keterlibatan, yang disajikan melalui beberapa kelompok fitur, yaitu (a) fitur pengelolaan data berupa impor data dari berkas *Comma Separated Values*, *Google Sheets*, dan data sampel; (b) fitur analitik berupa papan informasi ringkasan kinerja (*Dashboard*), analisis performa per konten, analisis waktu terbaik posting, analisis audiens dan pertumbuhan, serta ringkasan wawasan otomatis berbasis aturan dan template; (c) fitur perencanaan strategi berupa pengelolaan target *Key Performance Indicator* dan kampanye konten; (d) fitur alat berupa penyusun keterangan unggahan (*Generator Caption AI*) berbasis model bahasa Gemini dan analisis kompetitor; (e) fitur laporan berupa penyusun laporan berdasarkan rentang tanggal yang dipilih pengguna dalam format *Portable Document Format* (PDF) dan perbandingan antar dataset; serta (f) fitur kolaborasi dan bantuan berupa pengelolaan anggota proyek dan layanan tanya jawab dengan admin.

---

## 🟡 KATEGORI: PENTING — Sangat Dianjurkan (7 Revisi)

### 🔧 REVISI #6 — Bab 3.8: Tambah Sub-bab Baru Pengujian KPI dan Gemini

**LOKASI:** Bab 3 → 3.8 Pengujian Sistem → tambahkan dua sub-bab baru SETELAH **3.8.1 Pengujian Black Box Testing** dan SEBELUM **3.8.2 Pengujian Penerimaan Pengguna**.

**TINDAKAN:** Sebelum mengubah, ubah dulu nomor sub-bab "Pengujian Penerimaan Pengguna" dari **3.8.2** menjadi **3.8.4**, lalu tambahkan dua sub-bab baru di antaranya.

**TEKS BARU UNTUK 3.8.2 (TAMBAHKAN):**

> **3.8.2 Validasi Perhitungan KPI dan Analitik**
>
> Validasi perhitungan KPI dan analitik dilakukan untuk memastikan bahwa nilai metrik yang ditampilkan oleh sistem konsisten dengan hasil perhitungan manual. Validasi dilakukan dengan membandingkan nilai *engagement rate* yang dihasilkan sistem terhadap nilai *engagement rate* yang dihitung secara manual menggunakan formula yang sama, yaitu jumlah interaksi dibagi jumlah jangkauan dikalikan seratus persen. Validasi dilakukan terhadap seluruh data unggahan pada dataset uji, dengan toleransi pembulatan kurang dari atau sama dengan nol koma nol satu poin persentase. Hasil validasi dinyatakan sesuai apabila selisih antara nilai sistem dan nilai validasi manual berada dalam batas toleransi tersebut. Hasil validasi disajikan dalam bentuk tabel ringkasan dan tabel sampel perhitungan untuk menunjukkan akurasi perhitungan sistem secara menyeluruh.

**TEKS BARU UNTUK 3.8.3 (TAMBAHKAN):**

> **3.8.3 Evaluasi Keluaran Model Bahasa Gemini**
>
> Evaluasi keluaran model bahasa Gemini dilakukan untuk menilai kelayakan hasil yang dihasilkan oleh fitur *Generator Caption AI* sebagai draf awal keterangan unggahan. Evaluasi dilakukan menggunakan dua skenario pengujian, yaitu skenario promosi produk dan skenario edukasi atau motivasi, yang masing-masing menggunakan masukan yang relevan dengan karakter konten akun studi kasus. Penilaian dilakukan berdasarkan empat aspek, yaitu kesesuaian konteks, kejelasan bahasa, relevansi hasil, dan kelayakan penggunaan. Hasil evaluasi disajikan dalam bentuk tabel evaluasi dengan catatan kualitatif untuk setiap skenario sehingga dapat menunjukkan kemampuan sistem dalam menghasilkan caption yang dapat digunakan sebagai draf awal oleh pengguna.

---

### 🔧 REVISI #7 — Bab 3.8.4 (sebelumnya 3.8.2): Tambah Info Jumlah Responden

**LOKASI:** Bab 3 → 3.8 Pengujian Sistem → 3.8.4 Pengujian Penerimaan Pengguna (yang sudah ada).

**TEKS LAMA (HAPUS):**
> Pengujian dilakukan dengan melibatkan responden yang merupakan pelaku UMKM. Responden diminta untuk menggunakan sistem dengan menjalankan beberapa skenario penggunaan, kemudian mengisi kuesioner yang disusun mengacu pada instrumen System Usability Scale.

**TEKS BARU (GANTI):**
> Pengujian dilakukan dengan melibatkan dua puluh responden yang terdiri dari mahasiswa, konten kreator, pengelola media sosial, pelaku UMKM, dan pengguna lain yang relevan dengan target pengguna sistem. Responden diminta untuk menggunakan sistem dengan menjalankan beberapa skenario penggunaan, kemudian mengisi kuesioner yang disusun mengacu pada instrumen *System Usability Scale*.

---

### 🔧 REVISI #8 — Bab 3.7.1 Penyiapan Lingkungan Produksi: Tambah Vercel

**LOKASI:** Bab 3 → 3.7 Deployment Sistem → 3.7.1 Penyiapan Lingkungan Produksi.

**TEKS LAMA (HAPUS):**
> Penyiapan lingkungan produksi dilakukan dengan menyiapkan layanan hosting untuk antarmuka pengguna, menyiapkan proyek Supabase untuk lingkungan produksi, mengonfigurasi variabel lingkungan, mengonfigurasi nama domain, dan mengonfigurasi sertifikat Hypertext Transfer Protocol Secure.

**TEKS BARU (GANTI):**
> Penyiapan lingkungan produksi dilakukan dengan menyiapkan platform Vercel sebagai layanan *hosting* untuk antarmuka pengguna, menyiapkan proyek Supabase untuk lingkungan produksi sebagai layanan *backend*, mengonfigurasi variabel lingkungan, mengonfigurasi nama domain, dan mengonfigurasi sertifikat *Hypertext Transfer Protocol Secure*. Pemilihan Vercel didasarkan pada dukungannya yang baik untuk kerangka kerja React dengan *bundler* Vite, fitur *Continuous Deployment* otomatis dari repositori Git, dan integrasi sertifikat *Hypertext Transfer Protocol Secure* bawaan.

---

### 🔧 REVISI #9 — Bab 3.2.1 Identifikasi Akun Studi Kasus: Spesifikkan Akun

**LOKASI:** Bab 3 → 3.2 Pengumpulan Data → 3.2.1 Identifikasi Akun Studi Kasus.

**TEKS LAMA (HAPUS):**
> Pemilihan akun studi kasus dilakukan dengan mempertimbangkan tiga kriteria utama, yaitu akun yang dimiliki oleh pelaku UMKM, akun yang aktif melakukan unggahan konten dalam periode pengamatan, dan akun yang pemiliknya bersedia memberikan akses data unggahan untuk keperluan penelitian. Berdasarkan kriteria tersebut, penulis memilih satu akun Instagram milik UMKM yang bergerak di bidang produk digital sebagai studi kasus utama.

**TEKS BARU (GANTI):**
> Pemilihan akun studi kasus dilakukan dengan mempertimbangkan tiga kriteria utama, yaitu akun yang dimiliki oleh pelaku UMKM, akun yang aktif melakukan unggahan konten dalam periode pengamatan, dan akun yang pemiliknya bersedia memberikan akses data unggahan untuk keperluan penelitian. Berdasarkan kriteria tersebut, penulis memilih akun Instagram @maariversea yang bergerak di bidang produk digital, dengan jenis produk meliputi *e-book*, jasa pembuatan website, konten edukasi, dan template digital. Akun tersebut memiliki basis pengikut sekitar enam puluh enam ribu pengguna dengan variasi format konten yang memadai, yaitu *image*, *carousel*, dan *reels*. Periode pengamatan dilakukan pada tanggal 3 Maret 2025 sampai 16 Maret 2025 untuk mendapatkan rekapitulasi data *insight* unggahan yang stabil.

---

### 🔧 REVISI #10 — Bab 2: Tambah Sub-bab System Usability Scale

**LOKASI:** Bab 2 → tambahkan sub-bab baru SETELAH "Pengujian Kotak Hitam (Black Box Testing)" dan SEBELUM "Penelitian Terdahulu".

**TINDAKAN:** Tambah sub-bab baru.

**TEKS BARU (TAMBAHKAN):**

> **System Usability Scale (SUS)**
>
> *System Usability Scale* (SUS) adalah instrumen pengukuran tingkat kebergunaan sistem yang dikembangkan oleh John Brooke pada tahun 1986 dan masih banyak digunakan sebagai standar industri hingga saat ini. SUS terdiri dari sepuluh pernyataan yang dijawab oleh responden menggunakan skala Likert lima poin, dari sangat tidak setuju sampai sangat setuju. Skor akhir SUS dihitung menggunakan formula khusus yang menghasilkan rentang nilai dari nol sampai dengan seratus, di mana untuk pernyataan bernomor ganjil skor dihitung dari nilai jawaban dikurangi satu, dan untuk pernyataan bernomor genap skor dihitung dari lima dikurangi nilai jawaban, kemudian seluruh hasil konversi dijumlahkan dan dikalikan dua koma lima.
>
> Sukma dkk. (2023) menyusun pengelompokan skor SUS yang lebih rinci dengan mempertimbangkan tiga dimensi penilaian, yaitu *Acceptability Range*, *Grade Scale*, dan *Adjective Rating*. Pada klasifikasi tersebut, skor 78,9 sampai 80,7 termasuk dalam *Grade Scale* A-, *Adjective Rating* Good, dan *Acceptability Range* Acceptable. Klasifikasi ini digunakan untuk menginterpretasikan skor SUS yang diperoleh dari hasil pengujian penerimaan pengguna agar hasil pengujian dapat dinyatakan dalam kategori yang lebih komprehensif dibandingkan hanya berdasarkan rentang penerimaan saja.

---

### 🔧 REVISI #11 — Bab 2: Tambah Sub-bab Vite

**LOKASI:** Bab 2 → tambahkan sub-bab baru SETELAH "React" dan SEBELUM "Tailwind CSS".

**TEKS BARU (TAMBAHKAN):**

> **Vite**
>
> Vite adalah perkakas *build* modern berbasis *ECMAScript Modules* native yang menyediakan server pengembangan dengan *Hot Module Replacement* (HMR) cepat dan *bundling* produksi yang efisien menggunakan Rollup. Vite mendukung berbagai kerangka kerja antarmuka termasuk React, Vue, dan Svelte, serta dirancang untuk mempercepat proses pengembangan aplikasi web modern dengan waktu kompilasi yang jauh lebih singkat dibandingkan *bundler* tradisional seperti Webpack (Mahendra & Saputra, 2024).

---

### 🔧 REVISI #12 — Bab 2: Tambah Sub-bab Recharts dan React Router DOM

**LOKASI:** Bab 2 → tambahkan dua sub-bab baru di antara "React" dan "PostgreSQL".

**TEKS BARU (TAMBAHKAN):**

> **Recharts**
>
> Recharts adalah pustaka visualisasi data berbasis React yang dibangun di atas D3.js. Pustaka ini menyediakan komponen grafik siap pakai seperti *LineChart*, *BarChart*, *ScatterChart*, dan *PieChart* yang dapat dikustomisasi melalui konfigurasi properti komponen. Recharts mendukung interaktivitas seperti *tooltip*, *legend*, dan animasi transisi, sehingga memudahkan pengembang dalam menampilkan data analitik secara visual dan interaktif pada aplikasi berbasis React (Putra & Lestari, 2024).
>
> **React Router DOM**
>
> *React Router DOM* adalah pustaka penanganan navigasi berbasis URL untuk aplikasi React. Pustaka ini menyediakan komponen seperti *BrowserRouter*, *Routes*, dan *Route* untuk mengatur perpindahan halaman tanpa perlu memuat ulang seluruh halaman, sehingga memberikan pengalaman aplikasi tunggal laman (*Single Page Application*) yang halus. *React Router DOM* juga mendukung fitur navigasi terprogram, parameter URL, dan rute bersarang yang memudahkan pengembangan aplikasi web yang kompleks (Wijaya, 2025).

---

## 🟢 KATEGORI: POLISHING — Optional (4 Revisi)

### 🔧 REVISI #13 — Bab 1 Paragraf 5: Tambah Singkatan UMKM

**LOKASI:** Bab 1 → 1.1 Latar Belakang → paragraf 5 (yang membahas peran UMKM di Indonesia).

**TEKS LAMA (HAPUS):**
> Permasalahan di atas menjadi semakin relevan ketika dikaitkan dengan konteks usaha mikro, kecil, dan menengah di Indonesia. Usaha mikro, kecil, dan menengah merupakan salah satu pilar utama perekonomian Indonesia

**TEKS BARU (GANTI):**
> Permasalahan di atas menjadi semakin relevan ketika dikaitkan dengan konteks usaha mikro, kecil, dan menengah (UMKM) di Indonesia. UMKM merupakan salah satu pilar utama perekonomian Indonesia

**TINDAKAN LANJUTAN:** Pada paragraf 5 dan setelahnya, ganti semua "usaha mikro, kecil, dan menengah" menjadi "UMKM" (kemunculan kedua dan seterusnya). Sisakan frasa lengkap hanya di kemunculan pertama.

---

### 🔧 REVISI #14 — Bab 2.18 Gemini: Tambah Info Multi-Model Fallback

**LOKASI:** Bab 2 → sub-bab "Gemini" → tambahkan kalimat di akhir paragraf.

**TEKS LAMA (akhir paragraf Gemini):**
> ...Versi Ultra merupakan model LLM pertama yang mampu melampaui kemampuan manusia dalam tes Massive Multitask Language Understanding (MMLU). Tes ini mencakup 57 bidang ilmu, seperti hukum, sejarah, kimia, fisika, matematika, kedokteran, dan etika, di mana Gemini Ultra berhasil meraih skor 90%, lebih tinggi dari GPT-4 yang memperoleh 86,4% (Ahmad & Nasution, 2025).

**TEKS BARU (TAMBAHKAN PARAGRAF SETELAH KALIMAT TERSEBUT):**
> Selain ketiga versi utama tersebut, Gemini juga tersedia dalam beberapa varian model yang dapat diakses melalui antarmuka pemrograman aplikasi (*Application Programming Interface*), antara lain *gemini-flash-latest* sebagai versi paling baru, *gemini-2.5-flash* dan *gemini-2.0-flash* sebagai versi yang lebih stabil, serta *gemini-flash-lite-latest* sebagai varian ringan. Variasi model tersebut memungkinkan integrator menerapkan strategi *multi-model fallback* untuk meningkatkan keandalan layanan ketika model utama mengalami kondisi *overload* atau *rate limit*, di mana sistem dapat secara otomatis berpindah ke model cadangan apabila model sebelumnya mengalami kendala.

---

### 🔧 REVISI #15 — Konsistensi: "caption generator" → "Generator Caption AI"

**LOKASI:** Seluruh Bab 1 dan Bab 2 (gunakan Find & Replace).

**TINDAKAN:** Cari semua kemunculan istilah berikut dan ganti:

| Cari (Find) | Ganti dengan (Replace) |
|-------------|------------------------|
| caption generator berbasis kecerdasan buatan | *Generator Caption AI* berbasis model bahasa Gemini |
| caption generator berbasis AI | *Generator Caption AI* |
| Caption generator | *Generator Caption AI* |

**ALASAN:** Bab 4 final konsisten menggunakan "Generator Caption AI" sebagai nama resmi fitur. Konsistensi terminologi memperkuat profesionalitas dokumen.

---

### 🔧 REVISI #16 — Italic Istilah Asing (Polishing)

**LOKASI:** Seluruh Bab 1, 2, 3.

**TINDAKAN:** Pakai **Find & Replace** dengan opsi **Format → Italic** untuk istilah berikut:

| Istilah Asing | Status |
|---------------|--------|
| engagement rate | *engagement rate* |
| reach | *reach* |
| likes | *likes* |
| comments | *comments* |
| shares | *shares* |
| saved | *saved* |
| views | *views* |
| followers | *followers* |
| frontend | *frontend* |
| backend | *backend* |
| serverless | *serverless* |
| Edge Function | *Edge Function* |
| machine learning | *machine learning* |
| natural language processing | *natural language processing* |
| click-through rate | *click-through rate* |
| follower growth | *follower growth* |
| impressions | *impressions* |
| dashboard | *dashboard* |
| big data | *big data* |
| social media analytics | *social media analytics* |

**CATATAN:** Akronim teknis (CSV, JSON, PDF, API, UML, SUS, KPI, BSD, DBMS, HTTPS) tetap **tegak**, bukan italic.

---

## 📊 RINGKASAN APPLY

| Kategori | Jumlah Revisi | Estimasi Waktu |
|----------|---------------|----------------|
| 🔴 KRITIS (wajib) | 5 | 30 menit |
| 🟡 PENTING (sangat dianjurkan) | 7 | 60 menit |
| 🟢 POLISHING (optional) | 4 | 30 menit |
| **TOTAL** | **16** | **2 jam** |

---

## ✅ CHECKLIST APPLY

Setelah selesai apply patch ini, lakukan:

- [ ] Bab 1: Apply Revisi #3, #4, #5, #13
- [ ] Bab 2: Apply Revisi #10, #11, #12, #14
- [ ] Bab 3: Apply Revisi #1, #2, #6, #7, #8, #9
- [ ] Konsistensi global (Revisi #15, #16): Apply di Bab 1, 2, 3
- [ ] Tambahkan referensi baru ke Daftar Pustaka (lihat `DaftarPustaka_FINAL.md`)
- [ ] Save dengan nama baru: `SKRIPSI BAB 1 PART 3.docx`, dst.
- [ ] Compare dengan `Bab1_FINAL.md`, `Bab2_FINAL.md`, `Bab3_FINAL.md` untuk verifikasi
- [ ] Submit ulang ke Turnitin (kemungkinan turun ke 13-14%)

---

## 📚 REFERENSI BARU YANG DITAMBAHKAN

Pastikan tambahkan ke Daftar Pustaka (lihat detail di `DaftarPustaka_FINAL.md`):

1. **Sukma dkk. (2023)** — untuk klasifikasi skor SUS
2. **Mahendra & Saputra (2024)** — untuk Vite
3. **Putra & Lestari (2024)** — untuk Recharts
4. **Wijaya (2025)** — untuk React Router DOM (perlu cek apakah Wijaya 2025 yang sudah ada di daftar pustaka cocok, atau perlu sumber baru)

---

**Disusun oleh:** Sistem AI Reviewer (Kiro)  
**Tanggal:** Mei 2026  
**Versi:** 1.0
