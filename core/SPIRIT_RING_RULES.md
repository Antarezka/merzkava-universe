# Xuanling Realm — Spirit Ring Rules

Status: Modul mekanik resmi; formula v1 untuk kompatibilitas, power scale, dan Qi dirancang dari arahan pemilik proyek.
Cakupan: usia dan warna Spirit Ring, kemunculan ring, penyerapan, sinkronisasi, power scale, Qi, serta hubungan dengan bottleneck dan breakthrough.

Aturan dalam modul ini harus dipertahankan secara konsisten. Jangan menghapus atau mengganti mekanik yang telah disepakati hanya karena rinciannya tidak tertulis di WORLD.md.

---

## 1. Sumber Spirit Ring

Spirit Ring diperoleh melalui Spirit Beast dan proses perolehan yang sah.

- Setelah Spirit Beast dikalahkan, Spirit Ring muncul mengambang di atas tubuh Beast.
- Perburuan dan penaklukan Beast dapat berlangsung di hutan atau lokasi berbahaya.
- Jangan mewajibkan pemburu membawa Beast ke tempat meditasi aman sebelum perburuan selesai.
- Mengalahkan Beast memunculkan ring, tetapi tidak berarti karakter otomatis berhasil menyerapnya.
- Kemampuan yang didapat dari ring harus sesuai dengan Beast dan hasil penyerapan yang benar-benar terjadi. Jangan mengarang kemampuan baru tanpa dasar.

## 2. Usia Spirit Ring dan Toleransi Tubuh

Tidak ada batas usia Spirit Ring yang mutlak hanya berdasarkan angka usia atau Realm. Rekomendasi usia ring harus mempertimbangkan toleransi tubuh, kompatibilitas, dan keadaan kultivator.

- Jangan menetapkan batas usia maksimum universal untuk setiap Realm.
- Jangan menganggap kultivator pasti mampu menyerap ring hanya karena berhasil mengalahkan Beast.
- Ring berusia lebih tinggi dapat membawa risiko bagi tubuh yang tidak mampu menoleransinya; keberhasilan tidak boleh dianggap otomatis.
- Usia ring adalah faktor dominan untuk power scale. Tier Beast yang menghasilkan ring terutama memengaruhi kompatibilitasnya, bukan menjadi pengganti nilai usia ring.

## 3. Warna Ring

| Warna | Usia Spirit Ring |
|---|---:|
| Putih | 10–99 tahun |
| Kuning | 100–999 tahun |
| Ungu | 1.000–9.999 tahun |
| Hitam | 10.000–49.999 tahun |
| Merah | 50.000–99.999 tahun |
| Emas | 100.000–499.999 tahun |

Warna untuk ring berusia 500.000 tahun atau lebih masih **Undefined**. Jangan menciptakan warna atau kategori baru. Rentang di atas 500.000 tahun tidak menetapkan batas maksimum usia ring; hanya warnanya yang belum diputuskan. Rentang warna di bawah 10 tahun juga belum ditetapkan.

## 4. Awakening, Slot, dan Bottleneck

- Awakening Martial Soul berlangsung pada usia empat tahun atau lebih.
- Awakening tidak otomatis memberikan Spirit Ring pertama; ring pertama harus diperoleh melalui proses tersendiri.
- Sistem memiliki sembilan Realm dan satu slot Spirit Ring untuk setiap Realm, sehingga Realm 1 membuka satu slot dan Realm 9 membuka sembilan slot.
- Urutan Realm: Spirit Initiate, Spirit Adept, Spirit Elder, Spirit Monarch, Spirit King, Spirit Ancestor, Spirit Emperor, Spirit Sovereign, Spirit Primordial.
- Progres 100% tidak otomatis berarti Sync progress sudah mencapai cap ring; gunakan format progres saat ini/cap ring.
- Menerobos memerlukan seluruh syarat di `core/CULTIVATION_SYSTEM.md`: bottleneck dalam jarak kurang dari 10 poin persentase dari cap, ring berikutnya tersedia, item wajib untuk Beast target tersedia, dan jeda minimum antar-penyerapan telah terpenuhi.
- Penyerapan ring berikutnya menambah jumlah ring hanya jika benar-benar berhasil. Realm baru hanya dicatat setelah seluruh proses breakthrough berhasil.
- Qi mortal sebelum awakening bernilai 0; setelah awakening tetapi sebelum ring pertama diserap, Qi belum terbentuk.
## 5. Penyerapan Spirit Ring, Kultivasi, Sync progress, dan Bottleneck

Istilah proses mekanik yang digunakan hanya:
- **Penyerapan Spirit Ring:** proses memperoleh dan menambahkan satu Spirit Ring ke jumlah ring yang dimiliki.
- **Kultivasi:** proses meningkatkan Sync progress menuju cap kompatibilitas maksimum ring yang sedang diproses.
- **Menerobos:** proses terpisah yang hanya berhasil apabila seluruh syarat resmi terpenuhi.

Meditasi atau kegiatan lain bukan Penyerapan Spirit Ring maupun Kultivasi. Kegiatan tersebut tidak otomatis menambah ring, menaikkan Sync progress, atau memenuhi syarat breakthrough.

Untuk setiap ring baru, hitung kompatibilitas ring tersebut (`Cᵢ`) menggunakan rumus §6.1. Nilai `Cᵢ` menjadi cap kompatibilitas maksimum bagi Sync progress ring itu. Format wajib: `Sync progress: [progres saat ini]%/[Cᵢ]%`. Contoh `Sync progress: 0%/78%` hanya berlaku jika rumus resmi menghasilkan cap 78%.

Cap dapat berbeda pada setiap ring dan tidak otomatis 100%. Kultivasi dapat menaikkan Sync progress hingga cap, tetapi tidak melewatinya. Jarak dari cap dihitung sebagai cap dikurangi Sync progress saat ini.

Syarat bottleneck untuk menerobos: jarak Sync progress ke cap harus kurang dari 10 poin persentase. Jika jaraknya 10 poin atau lebih, karakter belum memenuhi syarat bottleneck untuk menerobos.

Setiap breakthrough juga memerlukan ring berikutnya yang benar-benar tersedia, item wajib yang sesuai dengan Spirit Beast target, dan jeda minimum sejak penyerapan ring sebelumnya yang berhasil:
- Ring 1 → Ring 2: 2 minggu.
- Ring 2 → Ring 3: 1 bulan.
- Ring 3 → Ring 4: 3 bulan.
- Ring 4 → Ring 5: 6 bulan.
- Ring 5 → Ring 6: 1 tahun.
- Ring 6 → Ring 7: 2 tahun.
- Ring 7 → Ring 8: 3 tahun.
- Ring 8 → Ring 9: 4 tahun.

Jika persyaratan item khusus Beast belum ditetapkan, jangan mengarangnya atau menganggapnya tidak diperlukan. Periksa `bestiary/SPIRIT_BEAST_RULES.md`.

Deviasi: makin besar jarak Sync progress dari cap ketika breakthrough dipaksakan, makin tinggi dampaknya. Memaksakan Penyerapan Spirit Ring sebelum jeda minimum juga meningkatkan dampak deviasi. Gunakan formula dan tabel berikut sebagai satu-satunya sumber numerik deviasi.

### 5.1. Persentase deviasi dan tingkat ring

Persentase deviasi (**D**) menunjukkan seberapa besar deviasi yang terjadi, dari 1% sampai 100%. Kehilangan HP dasar dihitung sebagai persentase dari **HP maksimum karakter saat percobaan**, lalu dikalikan faktor tingkat ring. Dengan demikian, hasil menyesuaikan total cap HP karakter dan meningkat seiring nomor ring.

- **D = 1–100%** sesuai tingkat deviasi aktual.
- Pada deviasi 100%, Ring 1 kehilangan HP dasar sebesar 30% dari HP maksimum karakter.
- Faktor ring meningkat secara bertahap dari ×1,00 pada Ring 1 hingga ×2,00 pada Ring 9.
- Nomor ring yang dipakai adalah ring yang sedang diproses, **N = 1–9**.
- Gunakan HP maksimum sesuai Realm dan Stage karakter pada `core/HP_SYSTEM.md`; jangan memakai HP saat ini sebagai dasar persentase.
- Jangan menyamakan persentase deviasi dengan kategori risiko. Kategori risiko tetap ditentukan dari poin HP yang benar-benar hilang pada §5.3.

### 5.2. Rumus dan tabel kehilangan HP dasar

Gunakan:
- **H** = HP maksimum karakter saat percobaan, sesuai `core/HP_SYSTEM.md`.
- **N** = nomor Spirit Ring yang sedang diproses (1–9).
- **D** = persentase deviasi (1–100%).

Rumus tunggal:

`Faktor ring = 1 + ((N − 1) / 8)`

`Kehilangan HP dasar = round(H × 0,30 × (D / 100) × Faktor ring)`

- Ring 1 menggunakan faktor ×1,00; Ring 9 menggunakan faktor ×2,00.
- Pada deviasi 100%, Ring 1 mengurangi 30% HP maksimum; Ring 9 mengurangi 60% HP maksimum. Ring di antaranya meningkat bertahap.
- Pembulatan ke bilangan bulat terdekat; nilai tepat x,5 dibulatkan ke atas.
- Hasil rumus adalah poin HP. Setelah pengali pemaksaan diterapkan, kehilangan aktual tidak boleh melebihi HP saat ini.
- Jangan gunakan rentang acak 15–19 HP lama; rumus berbasis HP maksimum ini menggantikannya.

Tabel faktor ring pada deviasi 100%:

| Nomor Spirit Ring | Nama Realm terkait | Faktor ring | Kehilangan HP dasar sebagai persentase HP maksimum |
|---:|---|---:|---:|
| 1 | Spirit Initiate | ×1,00 | 30% |
| 2 | Spirit Adept | ×1,125 | 33,75% |
| 3 | Spirit Elder | ×1,25 | 37,5% |
| 4 | Spirit Monarch | ×1,375 | 41,25% |
| 5 | Spirit King | ×1,50 | 45% |
| 6 | Spirit Ancestor | ×1,625 | 48,75% |
| 7 | Spirit Emperor | ×1,75 | 52,5% |
| 8 | Spirit Sovereign | ×1,875 | 56,25% |
| 9 | Spirit Primordial | ×2,00 | 60% |

Untuk deviasi di bawah 100%, kalikan hasil persentase pada tabel dengan D/100. Contoh: karakter dengan HP maksimum 1.000 yang memproses Ring 3 pada deviasi 50% kehilangan `round(1.000 × 0,30 × 0,50 × 1,25) = 188 HP` dasar. Karakter dengan HP maksimum 8.950 yang memproses Ring 9 pada deviasi 100% kehilangan `round(8.950 × 0,30 × 1,00 × 2,00) = 5.370 HP` dasar. Jadi, hasil menyesuaikan HP maksimum karakter dan tingkat ring; nilai Ring 100% selalu meningkat saat nomor ring bertambah.

### 5.3. Kategori risiko berdasarkan poin HP yang hilang

Kategori risiko ditentukan dari jumlah HP yang benar-benar hilang setelah batas HP saat ini diterapkan, bukan langsung dari persentase deviasi; persentase hanya digunakan untuk menghitung kehilangan HP dasar.

| HP yang benar-benar hilang | Kategori risiko |
|---:|---|
| 1–4 poin | Sangat Rendah |
| 5–9 poin | Rendah |
| 10–19 poin | Menengah Rendah |
| 20–29 poin | Menengah Tinggi |
| 30–39 poin | Tinggi |
| 40 poin atau lebih | Sangat Tinggi |

Dengan tabel ini, kehilangan 15–19 poin selalu masuk **Menengah Rendah**, sebagaimana patokan pemilik. Jika HP saat ini lebih rendah daripada angka kehilangan yang dihitung, HP tidak boleh turun di bawah 0: kehilangan aktual dibatasi pada HP yang masih tersisa, lalu kategori risiko memakai kehilangan aktual tersebut.

### 5.4. Pengubah karena breakthrough dipaksakan

Rentang pada §5.2 adalah dampak dasar ketika tidak ada pelanggaran tambahan. Jika karakter memaksakan proses, gunakan pengali berikut pada kehilangan HP dasar sebelum menerapkan batas HP yang tersisa:

| Kondisi saat proses dipaksakan | Pengali dampak |
|---|---:|
| Gap 0–2 poin persentase dan jeda minimum terpenuhi | ×1,00 |
| Gap 3–5 poin persentase dan jeda minimum terpenuhi | ×1,25 |
| Gap 6–9 poin persentase dan jeda minimum terpenuhi | ×1,50 |
| Jeda minimum belum terpenuhi | ×1,50 |
| Gap ≥10 poin persentase tetapi proses tetap dipaksakan | ×2,00 |

`Gap = cap kompatibilitas − Sync progress saat ini`. Pengali gap dan pengali pelanggaran jeda **tidak ditumpuk**: gunakan pengali terbesar yang berlaku. Ini mencegah hukuman berlipat ganda dari satu kejadian yang sama. Jika Gap ≥10, proses tetap tidak sah menurut syarat bottleneck; pengali ×2,00 hanya dipakai bila narasi/kejadian secara eksplisit menyatakan karakter tetap memaksakan proses dan GM menyelesaikan konsekuensinya.

Setelah pengali diterapkan, bulatkan hasil ke bilangan bulat terdekat (x,5 ke atas), batasi kehilangan aktual agar tidak melebihi HP saat ini, lalu tentukan kategori risiko dari kehilangan aktual. Contoh: karakter dengan HP maksimum 1.000 yang memproses Ring 3 pada deviasi 50% memiliki kehilangan dasar 188 HP; jika pengali ×1,50 berlaku, hasilnya 282 HP sebelum batas HP saat ini. Kategori risiko ditentukan dari kehilangan aktual setelah batas HP saat ini diterapkan.

### 5.5. Alur wajib GM

1. Tentukan nomor ring yang sedang diserap dan persentase deviasi aktual (1–100%) dari §5.1.
2. Hitung kehilangan HP dasar memakai HP maksimum karakter, nomor ring, dan persentase deviasi sesuai §5.2.
3. Hitung Gap dan periksa jeda minimum. Jika ada pelanggaran, pilih satu pengali menurut §5.4; jangan menumpuk pengali.
4. Kalikan kehilangan dasar dengan pengali, lalu bulatkan sesuai aturan.
5. Terapkan damage HP: kehilangan aktual tidak boleh melebihi HP saat ini dan HP tidak boleh turun di bawah 0.
6. Tentukan kategori risiko dari kehilangan HP aktual menggunakan §5.3.
7. Catat nomor ring, persentase deviasi, kehilangan dasar, pengali dan alasannya, kehilangan HP akhir/aktual, kategori risiko, cap kompatibilitas ring berikutnya yang berkurang, serta cedera dan kondisi tubuh yang terjadi.
8. Pengurangan cap kompatibilitas ring berikutnya dan durasi pemulihan belum memiliki formula numerik. Catat bahwa keduanya belum ditentukan; jangan menyimpulkan angkanya dari tabel damage.

Jika penyerapan gagal, jangan menambahkan ring ke jumlah yang dimiliki. Terapkan konsekuensi kegagalan dan deviasi sesuai kejadian yang benar-benar terjadi.

Penyerapan paksa membuat sinkronisasi 100% nyaris mustahil. Penyerahan sukarela oleh Spirit Beast membuat sinkronisasi 100% lebih mungkin, tetapi tidak menjamin keberhasilan.
## 6. Rumus Kompatibilitas, Power Scale, dan Qi

### 6.1. Kompatibilitas setiap ring

Setiap kali karakter mencoba menyerap Spirit Ring baru, GM wajib menghitung dan mencatat kompatibilitas ring TERBARU itu. Ini berlaku untuk **setiap nomor ring dari 1 sampai 9**, bukan hanya ring ketiga. Jika penyerapan berhasil, jumlah ring total bertambah satu; jika gagal, jangan menambahkan ring ke jumlah yang dimiliki.

Beri nilai 0–100 untuk empat faktor berdasarkan fakta yang sudah tercatat, bukan tebakan:
- **B — toleransi tubuh:** kemampuan tubuh kultivator saat ini menahan tekanan ring kandidat, berdasarkan kondisi tubuh, Realm, dan Qi yang tersedia.
- **M — kecocokan Martial Soul:** seberapa cocok Beast/ring kandidat dengan Martial Soul karakter.
- **T — kecocokan tier Beast:** kecocokan tier Spirit Beast kandidat terhadap kapasitas kultivator saat ini. Gunakan klasifikasi tier dari modul bestiary ketika tersedia; jangan menciptakan tier Beast yang belum ditetapkan.
- **A — cara perolehan:** 100 untuk penyerahan sukarela yang benar-benar terjadi; 80 untuk penyerapan paksa. Untuk keadaan lain, tentukan nilai hanya jika ada aturan dan bukti yang mendukungnya.

Formula kompatibilitas v1:

**Cᵢ = min(100, 0,30Bᵢ + 0,30Mᵢ + 0,25Tᵢ + 0,15Aᵢ)**

Hasil Cᵢ adalah persentase kompatibilitas ring ke-i. Bobot ini merupakan rancangan sistem awal: tubuh dan kecocokan Martial Soul paling berpengaruh, tier Beast berikutnya, lalu cara perolehan. Penyerapan paksa memiliki batas teoretis 97% bahkan ketika faktor lainnya 100%, sehingga sinkronisasi 100% nyaris mustahil; penyerahan sukarela tetap tidak menjamin hasil 100% karena faktor lain dapat lebih rendah. Jangan mengarang nilai input tanpa bukti atau aturan yang dapat diterapkan.

### 6.2. Kompatibilitas keseluruhan semua ring

Setelah setiap ring berhasil diserap, hitung ulang kompatibilitas keseluruhan dari seluruh ring yang dimiliki. Gunakan rata-rata geometrik agar kompatibilitas rendah pada satu ring tetap berpengaruh dan tidak tertutup sepenuhnya oleh ring lain:

**C_total = (C₁ × C₂ × … × Cₙ)^(1/n)**

Jika salah satu Cᵢ bernilai 0, C_total juga 0. Jangan menghilangkan kompatibilitas ring lama saat ring baru diperoleh.

### 6.3. Power scale

Catat usia ring Aᵢ dalam tahun. Jumlahkan usia seluruh ring yang telah berhasil diserap:

**AgeTotal = A₁ + A₂ + … + Aₙ**

Hitung power scale ring dengan usia sebagai faktor dominan dan kompatibilitas keseluruhan sebagai faktor pengubah yang lebih kecil:

**PowerScale = AgeTotal × (0,75 + 0,25 × C_total / 100)**

Artinya, usia semua ring merupakan fondasi utama kekuatan; kompatibilitas keseluruhan memengaruhi hasil paling banyak 25%. Tier Beast memengaruhi power scale melalui nilai kompatibilitas, bukan sebagai pengali usia tambahan. Jangan menyamakan dua karakter hanya karena jumlah ringnya sama: usia dan kompatibilitas ring mereka bisa berbeda. PowerScale adalah indeks perbandingan kekuatan dari sistem ring, bukan otomatis angka damage atau jaminan menang dalam pertarungan.

### 6.4. Qi berdasarkan jumlah ring

Qi adalah sumber daya yang muncul setelah ring pertama berhasil diserap. Sebelum awakening, mortal memiliki **Qi = 0** dan menggunakan stamina. Setelah awakening tetapi sebelum ring pertama diserap, catat **Qi: belum terbentuk (belum ada cincin)**, bukan nilai Qi positif. Setelah ring pertama berhasil diserap, Qi dasar dimulai dari 100.

Untuk Qi dasar berdasarkan jumlah ring n, gunakan pertumbuhan geometrik berikut:

**Qiₙ = round(100 × 452341^( (n − 1) / 8 ))**

Nilai acuan yang dibulatkan:

| Jumlah ring berhasil diserap | Qi dasar |
|---:|---:|
| 1 | 100 |
| 2 | 509 |
| 3 | 2.593 |
| 4 | 13.207 |
| 5 | 67.256 |
| 6 | 342.504 |
| 7 | 1.744.213 |
| 8 | 8.882.449 |
| 9 | 45.234.100 |

Dengan demikian, pemilik sembilan ring memiliki Qi dasar tepat **45.234.100**. Qi mengikuti jumlah ring yang benar-benar berhasil diserap; jangan menaikkan Qi hanya karena karakter membuka slot Realm atau mengalahkan Beast. Usia ring dan kompatibilitas dihitung dalam PowerScale terpisah, sehingga Qi dasar tidak disalahartikan sebagai ukuran tunggal kekuatan tempur.

### 6.5. Wajib dicatat setelah setiap penyerapan

Setiap kali ring berhasil diserap, GM harus menyatakan nomor ring terbaru dan jumlah total ring yang kini dimiliki, lalu mencatat usia, warna (jika diketahui), sumber/tier Beast, kemampuan yang diperoleh, cap kompatibilitas Cᵢ, C_total yang diperbarui, AgeTotal, PowerScale, Qi, dan waktu penyerapan. Catat pula item wajib yang digunakan dan seluruh deviasi, damage HP, serta cedera jika terjadi. Jika input formula belum diketahui, tandai input itu sebagai belum diketahui dan jangan berpura-pura hasilnya presisi.

## 7. Pencatatan Profil

Jangan menambahkan field profil terpisah bernama Spirit Rings atau Law.

Jumlah slot mengikuti Realm. Informasi ring yang telah diperoleh—sumber, usia, warna, kemampuan, dan hasil proses yang diketahui—dicatat dalam bagian Teknik / Kemampuan atau deskripsi Martial Soul yang sudah ada. Jangan memberikan kemampuan ring sebelum ring benar-benar berhasil diserap.

## 8. Konsistensi Sumber

- Gunakan modul ini untuk mekanik Spirit Ring.
- Gunakan `core/CULTIVATION_SYSTEM.md` untuk Realm, Stage, progres, bottleneck, dan breakthrough.
- Gunakan `core/MARTIAL_SOUL.md` untuk Martial Soul dan awakening.
- Gunakan `bestiary/SPIRIT_BEAST_RULES.md` ketika modul tersebut tersedia untuk rincian Spirit Beast.
- Jangan mengubah keputusan dalam modul ini hanya karena WORLD.md tidak memuat setiap detail mekanik.
- Jika aturan baru bertentangan dengan aturan ini, tandai konflik dan minta keputusan pemilik; jangan menghapus aturan yang sudah disepakati secara diam-diam.
