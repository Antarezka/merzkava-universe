# Merzkava Universe — Hunger and Metabolism

**Status:** Modul mekanik resmi.  
**Cakupan:** Satiety, jadwal makan, pengurangan karena waktu aktif, tidur malam, Spirit Realm, kondisi tubuh, dan pengubah biologis/supranatural.

Modul ini adalah satu-satunya sumber angka untuk Hunger dan Metabolism. Jangan membuat rumus hunger tandingan di modul lain.

## 1. Stat Satiety

### Konsumsi item yang belum teridentifikasi

Jika item yang dikonsumsi belum memiliki identitas/jenis pasti atau detail relevan yang ditetapkan oleh kanon/GM, sebut item itu dengan label persis `*Unknown* *membutuhkan appraisal untuk lebih pastinya*` dalam laporan konsumsi dan ledger. Jangan menebak efek nutrisi, tier, atau nilai Satiety dari label tersebut. Konsumsi hanya boleh diproses jika konteks mendukung bahwa benda itu memang layak dimakan; jika tidak, identitas dan efeknya tetap belum diketahui sampai diperiksa/appraised secara sah. Makanan sehari-hari yang sudah jelas tetap mengikuti aturan konsumsi rutin dan tidak perlu appraisal.


Format stat wajib:

`Satiety: nilai/100`

- Satiety adalah ukuran rasa kenyang dan cadangan makan jangka pendek untuk gameplay, bukan HP atau Qi.
- Nilainya berada pada rentang 0–100. Jangan melebihi 100 atau mengurangi di bawah 0.
- Makanan/minuman yang layak dikonsumsi menambah Satiety sesuai efek resminya; semua waktu terjaga diklasifikasikan sebagai istirahat atau aktivitas dan mengurangi Satiety sesuai kategori §4. Istirahat tidak pernah memulihkan Satiety; hanya memperlambat pengurangannya.
- Satiety 0 berarti karakter kehabisan rasa kenyang dan perlu makan. Itu **tidak otomatis** berarti pingsan, kehilangan HP, atau mati. Konsekuensi tambahan harus memiliki aturan atau sebab yang sah.
- Makanan/minuman yang aman dan layak dikonsumsi menambah Satiety sesuai efek resmi item atau kategori porsi §2. Racun, makanan rusak/terkontaminasi, benda yang tidak layak dimakan, dan konsumsi dengan efek khusus mengikuti aturan item/kejadian; jangan otomatis memberinya efek positif.
- Jangan mengubah Satiety tanpa waktu terjaga yang berlalu, konsumsi yang benar-benar terjadi, atau pengubah yang sah.
- Nilai Satiety 100 hanya boleh dipertahankan bila state sebelumnya dan perhitungan interval membenarkannya, atau ada konsumsi/pengubah resmi yang benar-benar menaikkannya. Penampilan prima, stamina tinggi, tidak mengeluh lapar, atau deskripsi kualitatif seperti 'jarang merasa lapar' tidak membatalkan pengurangan numerik. Efek biologis khusus hanya mengubah angka jika sumber resmi menetapkan faktor numerik yang sah.

## 2. Jadwal Makan Normal

Tiga jendela makan harian:

| Waktu lokal dunia | Jendela makan |
|---|---|
| 06.00–11.00 | Pagi |
| 12.00–18.00 | Siang |
| 19.00–01.00 | Malam |

- Karakter normal umumnya makan tiga kali sehari.
- Satu **porsi makan standar** memulihkan **34 Satiety**. Cukup untuk membuat tiga porsi sehari secara teori memulihkan 102 poin sebelum batas maksimum 100 diterapkan.
- Porsi kecil/camilan memulihkan 10 poin; porsi besar memulihkan 50 poin. Gunakan nilai ini hanya bila jenis dan jumlah makanan mendukung kategori tersebut.
- Satiety dari makanan ditambahkan ke nilai sekarang dan dibatasi maksimum 100. Makan tidak otomatis mengisi ke 100 jika porsinya tidak cukup.
- Jika item memiliki nilai pemulihan Satiety resmi yang spesifik, gunakan nilai itu; jika tidak, pilih kategori porsi hanya berdasarkan jenis dan jumlah yang jelas mendukungnya. **Tier item tidak menentukan nilai Satiety.** Saat melaporkan konsumsi, sebutkan nama item, jumlah, efek Satiety aktual, serta nilai sebelum → sesudah; cantumkan tier/kualitas hanya jika sudah diketahui atau relevan. Makanan sehari-hari yang jelas memakai kategori ekonomi rutin dan harga pasar lokal dari `core/10_ECONOMY_SYSTEM.md`; jangan mewajibkan appraisal hanya karena makanan itu tidak memiliki tier khusus. Gunakan `core/TIER_ASSESSMENT_AND_APPRAISAL.md` hanya bila identitas atau klasifikasi khusus memang penting: dahulukan ruling MAA untuk objek yang diperiksa, atau prediksi GM berskor dengan bukti cukup dan label provisional. Jika bukti tidak cukup, nyatakan klasifikasi belum ditetapkan; jangan menghambat transaksi atau konsumsi rutin karena tidak ada appraisal.
- Makan di luar jendela tetap memulihkan Satiety sesuai porsi. Setelah makanan yang layak benar-benar dikonsumsi, hitungan beruntun jam makan terlewat direset; riwayat jendela yang sebelumnya terlewat tidak dihapus dari catatan kejadian.
- Jam makan yang terlewat dihitung saat jendela berakhir tanpa karakter makan, **hanya jika karakter terjaga dan punya kesempatan wajar untuk makan**. Jendela yang berlalu saat tidur tidak dihitung sebagai jam makan terlewat.
- Jika karakter tidak punya akses makanan atau tidak bisa makan karena situasi, jangan menganggap ia sengaja melewatkan makan; catat keadaan itu dan terapkan pengali jam makan terlewat hanya sesuai ketentuan di §5.

## 3. Laju Dasar Menurut Tingkat

Laju dasar menunjukkan waktu terjaga yang diperlukan untuk mengurangi 100 Satiety dari penuh ke 0 sebelum pengali kategori aktivitas, kondisi tubuh, jendela makan terlewat, dan efek khusus yang sah diterapkan.

| Tingkat tubuh/kultivasi | Waktu aktif per 100 Satiety |
|---|---:|
| Mortal (belum memasuki sembilan Spirit Realm) | 24 jam |
| Spirit Initiate | 2 hari |
| Spirit Adept | 4 hari |
| Spirit Elder | 8 hari |
| Spirit Monarch | 16 hari |
| Spirit King | 32 hari |
| Spirit Ancestor | 64 hari |
| Spirit Emperor | 128 hari |
| Spirit Sovereign | 256 hari |
| Spirit Primordial | 365 hari |

Gunakan Spirit Realm yang benar-benar tercatat dan jangan menyingkat tingkat kultivasi menjadi `Realm`. Mortal adalah status dasar sebelum sembilan Spirit Realm. Jangan menaikkan tingkat metabolisme hanya karena karakter memiliki Martial Soul langka, ring berusia tinggi, kekayaan, status sosial, atau kekuatan yang belum ditetapkan. Pengaruh khusus harus memenuhi §7.

## 4. Rumus Pengurangan Satiety dan Intensitas Aktivitas

Gunakan satu rumus dasar untuk setiap interval waktu terjaga:

Pengurangan dasar = (Jam terjaga dalam interval / Waktu dasar per 100 Satiety dalam jam) × 100

Pengurangan akhir = min(Satiety saat ini, Pengurangan dasar × A × F × B × S)

- Jam terjaga dalam interval: durasi dunia yang benar-benar berlalu dalam satu segmen aktivitas, tidak termasuk tidur malam yang dilindungi §6.
- Waktu dasar: nilai pada tabel §3 yang dikonversi ke jam.
- A: pengali kategori aktivitas di bawah.
- F: pengali jendela makan terlewat di §5.
- B: pengali kondisi tubuh di §7.
- S: pengali biologis/supranatural hanya jika ada angka resmi yang sah. Jika tidak ada, gunakan ×1,00.
- Batas pengali gabungan: setelah mengalikan faktor yang sah, gunakan nilai akhir maksimum ×8,00 untuk satu interval. Batas ini mencegah kombinasi pengali membuat Satiety habis secara matematis dalam beberapa menit, tetapi aktivitas Survival tetap sangat menguras.
- Pengali aktivitas adalah kategori eksklusif untuk segmen waktu yang sama. Jangan mengalikan Ringan × Sedang × Berat × Survival sekaligus. Jika aktivitas berubah, pisahkan durasinya menjadi segmen berbeda.
- Pengali kondisi tubuh tetap faktor terpisah dari aktivitas hanya jika kelelahan benar-benar terjadi dan memiliki dasar. Jangan menghitung dampak yang sama dua kali sebagai kategori aktivitas dan pengubah khusus.
- Hitung seluruh interval dengan presisi internal penuh. **Bulatkan hanya nilai yang ditampilkan di laporan dan profil ke 0,1 Satiety**; jangan membulatkan state internal setelah setiap aktivitas. Jika perubahan internal kurang dari 0,05 sehingga tampilan satu desimal tidak berubah, tetap laporkan perubahan presisi internal, nilai tampilan yang tetap, dan catat peristiwa tersebut di ledger. Jangan kehilangan sisa pecahan akibat pembulatan tampilan.
- Pengurangan aktual tidak boleh melebihi Satiety yang tersedia. Nilai akhir tidak pernah kurang dari 0.
- Jika tidak ada waktu terjaga yang berlalu, tidak ada pengurangan karena waktu kecuali mekanik khusus resmi menyatakan sebaliknya.

### Kategori aktivitas — wajib untuk setiap interval terjaga

| Kategori | Pengali A | Contoh dan batas |
|---|---:|---|
| Istirahat terjaga | ×0,50 | Duduk/berbaring untuk memulihkan tenaga, berhenti sejenak, atau istirahat aman tanpa aktivitas fisik berarti. Memperlambat pengurangan; **tidak menambah Satiety**. |
| Ringan | ×1,25 | Berjalan santai, berbelanja, mengobrol sambil bergerak, tugas ringan, aktivitas sehari-hari tanpa tuntutan fisik berarti. |
| Sedang | ×1,75 | Berjalan jauh, perjalanan aktif, latihan rutin, kultivasi/meditasi terfokus yang berkelanjutan, pekerjaan fisik berkelanjutan, atau eksplorasi yang terus menguras tenaga. |
| Berat | ×2,50 | Berlari lama, membawa beban berat, latihan intensif, pertarungan singkat yang menguras tenaga, atau kerja fisik berat. |
| Survival | ×4,00 | Keadaan darurat nyata: bertahan/berjuang di medan perang, bencana, kabur dari ancaman yang terus berlangsung, atau combat berkepanjangan yang memicu tekanan fisik dan adrenalin. |

- Setiap interval waktu terjaga harus diklasifikasikan sebagai satu kategori aktivitas yang paling sesuai, termasuk Istirahat terjaga bila memang sedang beristirahat. Jangan membiarkan waktu aktif tanpa kategori.
- Survival bukan sinonim untuk aktivitas yang sekadar sulit atau lokasi berbahaya. Harus ada ancaman darurat yang nyata dan perjuangan aktif/berkelanjutan. Berdiri di medan perang tanpa mengerahkan tenaga atau berada di dekat bencana tidak otomatis membuat seluruh waktu menjadi Survival.
- Adrenalin adalah alasan naratif untuk mengklasifikasikan kejadian sebagai Survival bila syaratnya terpenuhi; jangan menambahkan pengali adrenalin kedua di atas ×4,00.
- Jika kategori berubah dalam satu aksi, hitung setiap segmen dengan durasi dan pengalinya sendiri, lalu jumlahkan pengurangannya. Jangan menghitung durasi yang sama dua kali.
- Jika aktivitas menimbulkan kelelahan yang didukung kejadian, pengali kondisi tubuh §7 boleh berlaku bersamaan. Kategori aktivitas dan kondisi tubuh mengukur hal berbeda, tetapi pengali gabungan tetap tunduk pada batas ×8,00.

**Contoh Mortal:** 6 jam aktivitas Ringan, kondisi normal, tanpa jendela makan terlewat: (6/24 × 100) × 1,25 = 31,25, dibulatkan menjadi **31,3 Satiety**.

**Contoh Mortal Survival:** 1 jam Survival, kelelahan ekstrem, dan 3+ jendela makan terlewat: pengali mentah 4,00 × 2,50 × 4,00 = 40,00, dibatasi menjadi ×8,00; pengurangan maksimum dari interval 1 jam ialah 33,3 Satiety sebelum dibatasi oleh Satiety yang tersedia.

**Contoh Spirit Primordial:** 24 jam aktivitas Ringan dalam kondisi normal tanpa jendela makan terlewat: pengurangan internal ≈ 0,014 Satiety; tampilan satu desimal dapat tetap sama pada interval ini, tetapi sisa presisi tetap disimpan dan diakumulasikan pada interval berikutnya.

## 5. Jam Makan Terlewat

Hitung jendela makan yang terlewat secara beruntun saat karakter terjaga dan memiliki kesempatan yang wajar untuk makan. Terapkan **satu pengali aktif** berikut untuk interval terjaga berikutnya; jangan menumpuk pengali per jendela dan jangan mengubah perhitungan interval yang sudah selesai secara retroaktif.

| Jendela makan terlewat berturut-turut | Pengali F |
|---|---:|
| 0 | ×1,00 |
| 1 | ×1,75 |
| 2 | ×2,75 |
| 3 atau lebih | ×4,00 |

- Sebuah jendela dihitung terlewat ketika jendela itu berakhir tanpa karakter makan, selama karakter terjaga dan punya kesempatan yang wajar untuk makan. Jendela yang berlalu saat tidur malam yang dilindungi tidak dihitung.
- Pengali baru mulai berlaku pada interval terjaga setelah jendela dinyatakan terlewat. Jangan menerapkannya kembali ke interval yang sudah dihitung.
- Setelah karakter benar-benar mengonsumsi makanan atau minuman bernutrisi yang secara wajar memenuhi kebutuhan makan, reset hitungan jendela makan terlewat menjadi 0 untuk interval berikutnya. Air biasa atau konsumsi nonnutritif tidak otomatis mereset hitungan kecuali aturan item resmi menyatakan sebaliknya. Konsumsi tetap memulihkan Satiety sesuai efek resmi item meskipun terjadi di luar jendela makan.
- Jika karakter terkurung, tidak sadar, terikat, atau situasi nyata lain menghalangi akses/kemampuan makan, jangan menyebutnya sengaja melewatkan makan. Hitung hanya kesempatan makan yang benar-benar ada; jangan menambahkan pengali saat karakter tidak punya pilihan wajar.
- Jangan menambahkan pengurangan tetap khusus hanya karena sebuah jendela terlewat. Dampaknya diterapkan melalui pengali F terhadap pengurangan selama waktu terjaga berikutnya.

## 6. Tidur Malam dan Penguncian Satiety

Tidur malam normal adalah kebutuhan biologis dan pengecualian resmi dari batas durasi aksi biasa.

- Ketika karakter mulai tidur malam, catat nilai Satiety terakhir sebagai nilai terkunci.
- Selama tidur malam normal, **Satiety tidak berkurang**. Jangan menerapkan pengurangan waktu aktif, pengali kondisi tubuh, atau jam makan terlewat selama periode tidur yang dilindungi.
- Ketika karakter bangun, lanjutkan perhitungan dari nilai Satiety yang terkunci dan mulai menghitung waktu aktif kembali dari waktu bangun.
- Tidur malam boleh melewati batas aksi biasa 3 jam dalam `gameplay/TIME_AND_ACTION_RULES.md`; jangan memaksa pemain membagi tidur normal menjadi aksi tiga jam.
- Tidur tidak otomatis memulihkan Satiety, HP, Qi, atau injury. Tidur hanya mengunci pengurangan Satiety selama periode tidur normal; pemulihan sistem lain mengikuti aturan masing-masing.
- Jika tidur terganggu dan karakter benar-benar terjaga untuk periode tertentu, hitung pengurangan hanya selama waktu terjaga tersebut. Jangan menghukum waktu tidur yang benar-benar terjadi.
- Tidur siang atau pingsan tidak otomatis dianggap tidur malam yang dilindungi. Perlakukan sesuai fakta kejadian; jangan gunakan tidur sebagai alasan untuk mengabaikan kebutuhan darurat atau konsekuensi yang telah ditetapkan.

## 7. Kondisi Tubuh dan Pengubah Khusus

Kondisi tubuh mengubah laju pengurangan Satiety dengan faktor B. Pilih satu kategori kelelahan yang paling sesuai dengan kondisi aktual; kategori yang saling tumpang tindih tidak boleh ditumpuk.

| Kondisi tubuh | Pengali B |
|---|---:|
| Normal / lelah ringan | ×1,00 |
| Kelelahan nyata | ×1,25 |
| Kelelahan berat | ×1,75 |
| Kelelahan ekstrem | ×2,50 |

- Kelelahan harus memiliki dasar kejadian, misalnya aktivitas berkepanjangan, perjalanan berat, latihan intensif, kurang istirahat, atau perjuangan survival.
- Pengali kondisi tubuh adalah kategori alternatif. Jika karakter mengalami kelelahan ekstrem, gunakan ×2,50 saja, bukan ×1,25 ×1,75 ×2,50.
- Cedera, penyakit, racun, demam, kehamilan, usia, cuaca, atau kondisi khusus lain tidak mendapat pengali default dari modul ini. Terapkan hanya jika ada aturan resmi lain atau efek spesifik yang telah ditetapkan.
- Jangan memberikan pengali kelelahan otomatis hanya karena giliran berlalu. Klasifikasi harus didukung aktivitas, kondisi, atau kejadian yang benar-benar terjadi.
- Aktivitas dan kondisi tubuh boleh menjadi faktor terpisah hanya jika keduanya menggambarkan efek independen. Batas gabungan pengali ×8,00 pada §4 tetap berlaku.

### Keunggulan atau kelemahan biologis/supranatural

Genetik, garis keturunan, kutukan, berkah langit, konstitusi khusus, Martial Soul, obat, teknik, relik, atau efek supernatural boleh mengubah metabolisme, tetapi tidak otomatis melakukannya.

1. Pastikan sifat atau efek tersebut tercatat atau diperoleh melalui kejadian yang sah.
2. Tentukan apakah efek secara eksplisit memengaruhi kebutuhan makan/metabolisme.
3. Jika efek memiliki besaran numerik resmi, gunakan sebagai faktor S.
4. Jika efek hanya kualitatif, jangan menciptakan angka. Catat dampak naratifnya tanpa mengubah laju Satiety numerik sampai nilai resmi ditetapkan.
5. Jangan menyimpulkan bahwa keturunan kuat otomatis tidak lapar, kutukan otomatis meningkatkan hunger, atau berkah otomatis menurunkan hunger tanpa sumber yang sah.

Semua pengubah independen boleh dikalikan sebelum batas gabungan ×8,00 diterapkan, tetapi jangan menghitung efek yang sama dua kali, menumpuk kategori kelelahan, atau mengarang angka.

## 8. Urutan Resolusi Wajib GM

Setiap kali waktu berlalu, aktivitas berubah, makanan/minuman dikonsumsi, atau kondisi tubuh berubah:

1. Ambil timestamp terakhir yang sah dan tentukan durasi dunia yang benar-benar berlalu.
2. Pisahkan durasi menjadi segmen jika jenis aktivitas, kondisi tubuh, status terjaga, pengali, konsumsi, atau batas akhir jendela makan berubah. Ketika jendela makan berakhir di tengah interval, hitung segmen sebelum dan sesudah batas secara terpisah agar pengali baru tidak diterapkan secara retroaktif.
3. Kecualikan tidur malam yang dilindungi §6. Selama tidur itu, Satiety terkunci pada nilai saat tidur dimulai.
4. Tentukan Spirit Realm/status tubuh dan waktu dasar dari §3.
5. Klasifikasikan setiap interval terjaga dengan tepat satu kategori aktivitas dari §4.
6. Perbarui hitungan jendela makan hanya ketika jendela berakhir dan syarat kesempatan makan terpenuhi. Pengali baru berlaku ke interval berikutnya.
7. Tentukan satu pengali kondisi tubuh dan faktor khusus yang benar-benar didukung sumber resmi.
8. Hitung pengurangan per segmen memakai §4, terapkan batas pengali gabungan ×8,00, jumlahkan segmen, dan batasi pengurangan pada Satiety yang tersedia.
9. Terapkan efek konsumsi hanya jika item benar-benar dimakan/diminum. Gunakan efek Satiety resmi item jika tersedia; jika tidak, gunakan kategori porsi §2 berdasarkan jenis dan jumlah yang jelas mendukungnya. Jangan menyimpulkan efek dari tier saja.
10. Batasi nilai akhir pada 0–100 dan simpan nilai terbaru pada profil serta riwayat sesi.
11. Untuk setiap aktivitas terbaru, sebutkan Satiety dalam respons: tampilkan perubahan dan nilai sebelum → sesudah bila berubah; jika tidak berubah, nyatakan nilai tetap dan alasan (misalnya tidur malam yang dilindungi atau tidak ada waktu terjaga yang berlalu). Sebelum memakai 100/100, audit state sebelumnya dan hitung semua interval terjaga yang sudah berlalu; jangan menyimpulkan Satiety penuh dari kondisi prima atau sifat 'jarang lapar'.
12. Untuk setiap aktivitas terbaru, gunakan laporan yang konsisten. Jika Satiety berubah karena aktivitas: “Satiety berkurang −X (sebelum/100 → sesudah/100) akibat [kategori aktivitas] selama [durasi].” Jika dikonsumsi: “Dengan mengonsumsi **[nama item]** *Tier [tier resmi atau ‘Tier belum ditetapkan’]* ×[jumlah], Satiety bertambah/berkurang [±X] (sebelum/100 → sesudah/100).” Pakai kata bertambah atau berkurang sesuai efek aktual, bukan asumsi. Setelah kalimat perubahan terverifikasi, tulis persis inline-code `Log tercatat!`, lalu satu `LEDGER LOG` untuk semua perubahan state dari tindakan itu. Jika nilai tampilan satu desimal tidak berubah karena perubahan internal sangat kecil, sebutkan delta presisi internal dan nilai tampilan yang tetap, lalu catat perubahan tersebut. Jangan tampilkan penanda atau ledger jika tidak ada perubahan state aktual.
13. Jangan mengubah HP, Qi, injury, atau kondisi lain hanya karena Satiety berubah, kecuali sumber resmi lain atau kejadian sah menetapkan hubungan itu. Format dan urutan laporan gabungan mengikuti `templates/AUTHORITY_ORDER.md`, `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`, dan `core/10_ECONOMY_SYSTEM.md`.

Jika timestamp, Spirit Realm, periode tidur, kategori aktivitas, atau kondisi penting tidak diketahui, jangan menebak angka secara diam-diam. Gunakan data terverifikasi yang tersedia dan ungkapkan celahnya; minta klarifikasi hanya jika tanpa itu hasil tidak bisa diselesaikan dengan aman dan konsisten.

## 9. Format Profil

Tambahkan field berikut ke profil gameplay:

`Satiety: nilai/100`

Nilai harus berasal dari profil terakhir dan perubahan yang benar-benar terjadi. Jika state awal Satiety belum pernah ditetapkan, GM dapat menetapkan nilai awal yang masuk akal untuk karakter baru dan menandainya sebagai estimasi awal; jangan menganggap semua karakter yang sudah berjalan otomatis berada di 100.
