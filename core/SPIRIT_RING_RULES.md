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

Deviasi: makin besar jarak Sync progress dari cap ketika breakthrough dipaksakan, makin tinggi tingkat deviasi. Memaksakan Penyerapan Spirit Ring sebelum jeda minimum juga menyebabkan deviasi. Persentase paparan deviasi ditentukan oleh nomor ring: Ring 1 memiliki paparan 100% (tertinggi), dan persentasenya harus lebih rendah untuk setiap nomor ring berikutnya. Nilai persis untuk Ring 2–9 belum ditetapkan; jangan mengarang tabel persentase.

**Tingkat risiko ditentukan oleh jumlah poin status yang benar-benar hilang**, bukan oleh persentase paparan deviasi. Dengan demikian, persentase paparan dan tingkat risiko adalah dua hal berbeda. Patokan yang telah dikonfirmasi: kehilangan 15–19 poin status termasuk kategori **Menengah Rendah**. Rentang numerik untuk kategori risiko lain belum ditetapkan.

Setiap deviasi wajib mencatat:
1. Persentase paparan deviasi sesuai nomor ring, jika nilai resminya tersedia.
2. Jumlah poin status yang hilang dan kategori risiko berdasarkan jumlah kehilangan tersebut.
3. Pengurangan cap kompatibilitas maksimum ring berikutnya dan cap baru yang berlaku.
4. Damage HP serta cedera/kondisi tubuh yang benar-benar terjadi.

Jika rumus numerik untuk persentase Ring 2–9, rentang kategori risiko lain, pengurangan cap, damage, atau pemulihan belum ditetapkan, jangan mengarang angka seolah-olah canon. Tandai nilai tersebut sebagai belum ditentukan dan catat konsekuensi yang memang didukung sumber.

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
