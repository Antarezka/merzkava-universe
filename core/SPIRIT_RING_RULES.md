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
- Setiap perpindahan ke Realm berikutnya membutuhkan Spirit Ring berikutnya yang sah.
- Progres 100% berarti mencapai bottleneck, bukan breakthrough otomatis.
- Penyerapan ring berikutnya menjadi bagian dari proses kultivasi dan breakthrough. Realm baru hanya dicatat setelah proses benar-benar berhasil.
- Qi mortal sebelum awakening bernilai 0; mereka menggunakan stamina biasa. Setelah awakening tetapi sebelum ring pertama diserap, Qi belum terbentuk dan dicatat sebagai belum ada cincin, bukan sebagai Qi positif.

## 5. Penyerapan, Meditasi, dan Sinkronisasi

- Penyerapan Spirit Ring merupakan bagian dari proses kultivasi dan breakthrough.
- Meditasi kultivasi untuk meningkatkan kekuatan dan kompatibilitas harus dilakukan di tempat yang aman dan stasioner. Catat progres persentase kekuatan kultivasi dan kompatibilitas di dalam penjelasan/log meditasi yang sama agar perubahan status punya konteks.
- Ketentuan meditasi aman tidak berarti perburuan Beast harus dilakukan di tempat aman atau Beast harus dibawa ke lokasi meditasi sebelum dikalahkan.
- Penyerapan paksa membuat sinkronisasi 100% nyaris mustahil.
- Jika Spirit Beast secara sukarela menyerahkan ringnya, sinkronisasi 100% menjadi lebih mungkin. Ini bukan jaminan bahwa penyerapan pasti berhasil.
- Jangan menyamakan sinkronisasi yang tinggi dengan keberhasilan otomatis, dan jangan menganggap kegagalan atau keberhasilan tanpa menyelesaikan proses yang relevan.

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

Setiap kali ring berhasil diserap, GM harus menyatakan nomor ring terbaru dan jumlah total ring yang kini dimiliki, lalu mencatat usia, warna (jika diketahui), sumber/tier Beast, kemampuan yang diperoleh, Cᵢ dalam persen, C_total yang diperbarui, AgeTotal, PowerScale, dan Qi sesuai jumlah ring. Jika input formula belum diketahui, tandai input itu sebagai belum diketahui dan jangan berpura-pura hasilnya presisi.

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
