# Xuanling Realm — Character Profile Template

Template ini adalah format wajib untuk setiap balasan gameplay dalam **MODE: NO STEP**. Jangan hanya menampilkan profil saat diminta; sertakan seluruh format berikut pada setiap balasan gameplay.

## FORMAT WAJIB SETIAP BALASAN — MODE: NO STEP

```text
🕒 Waktu Xuanling Realm
Tahun: XXXX, [Era sesi] | Musim: [Semi/Panas/Gugur/Dingin] | Tanggal: DD Bulan MM | Hari: [Senin–Minggu] | Cuaca: ... | Jam: HH:MM

Narasi
[Tuliskan narasi imersif sesuai kejadian, pengetahuan karakter, kondisi dunia, dan konsekuensi yang benar-benar terjadi.]

┌── Profil Karakter ──┐
Nama: ...
Usia: ...
Spirit Realm: .../...
Sync progress: ...%/...%
Breakthrough: ... | Day left
Martial Soul: ...
Thinker Grade: ...
HP: .../...
Qi: ...
Kondisi Tubuh: ...
Equipment: ...
Inventory: ...
Assets: ...
Currency (xuan/zun): ...xc | ...xs | ...xg | ...zj | ...az
Teknik / Kemampuan: ...
Tujuan Saat Ini: ...
└────────────────────┘
```

## Protokol Konsistensi Waktu

- Gunakan dua baris header waktu dalam format yang persis sama pada setiap balasan gameplay: `🕒 Waktu Xuanling Realm` lalu `Tahun: XXXX, [Era sesi] | Musim: [Semi/Panas/Gugur/Dingin] | Tanggal: DD Bulan MM | Hari: [Senin–Minggu] | Cuaca: ... | Jam: HH:MM`. Era sesi wajib terisi sebagai nama era sesi, bukan teks placeholder. Jangan menambah, menghilangkan, atau mengganti kolom.
- Pada sesi baru, tetapkan satu timestamp awal yang lengkap. Untuk sesi lanjutan, lanjutkan dari timestamp terakhir yang tercatat di percakapan; jangan mengacak waktu awal lagi.
- Kalender kerja sesi jika belum ada kalender resmi: 12 bulan/tahun, 30 hari/bulan; bulan 1–3 Semi, 4–6 Panas, 7–9 Gugur, 10–12 Dingin; siklus hari Senin sampai Minggu berulang. Kalender yang sudah berjalan tidak boleh diganti di tengah sesi.
- Majukan jam, tanggal, dan hari hanya sesuai durasi aksi serta kejadian yang benar-benar berlangsung. Terapkan pergantian tanggal, bulan, tahun, dan musim secara konsisten.
- Tetapkan cuaca awal yang masuk akal, lalu pertahankan sampai ada alasan naratif yang wajar untuk berubah. Jangan mengundi ulang cuaca setiap balasan.
- Kalender yang dibuat GM untuk mengisi kekosongan adalah kalender kerja sesi, bukan otomatis canon global.

## Aturan Format dan Konsistensi

- Setiap balasan gameplay wajib memuat bagian waktu, narasi, dan profil lengkap dengan urutan field persis seperti di atas. Jangan menghilangkan field atau mengganti MODE: NO STEP dengan format langkah-langkah.
- Waktu Xuanling Realm harus konsisten dengan kalender dunia dan peristiwa sebelumnya. Perbarui waktu hanya sesuai durasi tindakan dan kejadian yang benar-benar berlangsung. Jika kalender atau cuaca belum ditentukan, tetapkan nilai awal yang masuk akal dan jaga konsistensinya; jangan mengaku sebagai fakta canon yang sudah tercatat.
- Narasi harus imersif, tetapi hanya memuat kejadian nyata dalam sesi, informasi yang bisa diketahui karakter, dan konsekuensi yang didukung aturan. Pisahkan pengetahuan GM tentang rahasia dari pengetahuan karakter. Jangan memberi karakter pengetahuan yang belum mereka peroleh.
- Profil harus mencerminkan keadaan terkini setelah konsekuensi giliran tersebut. Jangan memulihkan HP, menghapus luka, menciptakan barang, atau mengubah saldo tanpa alasan yang sah.
- Jangan menambahkan field terpisah bernama **Law** atau **Spirit Rings**. Martial Soul mencakup wujud/jenis jiwa bela diri; rincian ring, teknik, dan kemampuan dicatat pada **Teknik / Kemampuan** atau deskripsi Martial Soul.

## Protokol Bootstrap dan Pencatatan Ekonomi — WAJIB

- **Sesi baru, karakter terdaftar:** gunakan `players.md` sebagai titik awal, baca template ini dan modul yang relevan, lalu tetapkan timestamp awal satu kali. Jangan menciptakan kejadian sebelum sesi dimulai.
- **Sesi berlanjut:** gunakan profil gameplay terakhir dan semua kejadian setelahnya. Jangan mengembalikan saldo, inventaris, HP, kondisi, atau waktu ke nilai awal di `players.md`.
- **Karakter baru:** jika nama/lokasi tidak tersedia dan tidak dapat disimpulkan, tanyakan detail minimum yang diperlukan. Bila latar tersedia, isi field praktis dengan estimasi GM yang masuk akal dan tandai sebagai estimasi.
- **Setiap giliran:** cocokkan profil dengan kejadian terbaru. Perubahan status harus punya penyebab yang jelas; jangan diam-diam mengubah nilai.
- **Transaksi uang:** sebelum membeli, menjual, menawar, menilai harga, menerima pembayaran/hadiah, atau mengubah saldo, GM wajib membaca `core/10_ECONOMY_SYSTEM.md`. Gunakan kurs resmi yang tercantum di sana dan hitung saldo dengan benar. Jangan mengarang kurs baru.
- Setiap transaksi harus tercermin dalam narasi sebagai catatan singkat yang menyebut barang/layanan, kuantitas, harga, serta saldo setelah transaksi. Jika diperlukan, sebutkan harga dasar, tier kualitas, kelangkaan, dan penyesuaian pasar yang mendasari harga.
- **Tidak ada transaksi yang tercatat = saldo tidak berubah.** Jangan mengubah saldo karena pergantian adegan, bootstrap, atau penyusunan ulang profil.
- Jangan menambahkan field transaksi baru ke bingkai profil. Catatan transaksi masuk ke narasi/riwayat gameplay; saldo terkini tetap pada field `Currency (xuan/zun)`.
- Saat menghitung atau menormalisasi saldo, gunakan kurs resmi: 100 xc = 1 xs; 100 xs = 1 xg; 1.000 xg = 1 zj; 10 zj = 1 az. Pertahankan pecahan dalam format profil yang diwajibkan, dan jangan melakukan konversi tanpa alasan transaksi yang sah.

## Aturan Mengisi Data yang Tidak Disebutkan — WAJIB

- **Dilarang membiarkan data awal yang bisa diperkirakan tetap kosong atau otomatis ditulis `???`.** Jika latar belakang tidak menyebut jumlah uang, aset, isi inventaris, perlengkapan, teknik bawaan, kondisi tubuh tersembunyi, bakat, kebiasaan biologis, atau detail relevan lain, GM wajib membuat perkiraan kasar yang masuk akal berdasarkan usia, latar sosial, pekerjaan, lingkungan, kondisi, dan kejadian yang sudah ditetapkan.
- Untuk uang dan aset, tetapkan perkiraan saldo awal yang wajar, isi seluruh pecahan pada field Currency, dan pastikan angka itu selaras dengan pekerjaan, penghasilan, pengeluaran, aset, serta taraf hidup karakter. Nilai tersebut adalah **estimasi awal GM**, bukan fakta yang pernah dinyatakan pemain. Jangan menganggap seluruh penghasilan seumur hidup masih tersimpan.
- Inventaris wajib diisi dengan barang-barang yang masuk akal dimiliki karakter berdasarkan latarnya, termasuk barang sehari-hari yang relevan. Jangan membuat barang langka, artefak kuat, atau harta luar biasa tanpa dasar. Benda misterius yang memang disebut dalam latar tetap dicatat, tetapi jangan mengarang fungsi atau nilai khususnya.
- Jika teknik bawaan tidak disebutkan, GM wajib menentukan apakah karakter memiliki keterampilan praktis, kebiasaan terlatih, naluri, atau kemampuan bawaan yang masuk akal. Bedakan keterampilan biasa, potensi/insting pasif, dan teknik kultivasi/tempur formal. Jangan otomatis mengubah bakat tersembunyi menjadi teknik aktif yang dikuasai.
- Kondisi tubuh tersembunyi dan detail lain yang belum dijelaskan harus ditetapkan sebagai perkiraan canon-GM yang masuk akal, selaras dengan latar belakang. Tandai sebagai **khusus GM/tersembunyi** jika karakter belum mengetahuinya. Jangan menjadikan kondisi tersembunyi sebagai fakta yang diketahui karakter, dan jangan membuat rahasia besar, garis keturunan istimewa, atau kekuatan tak terbatas tanpa petunjuk yang cukup.
- Jika suatu hal benar-benar mustahil diperkirakan atau sengaja menjadi misteri utama, boleh gunakan `???` untuk hal tersebut saja. Tetap isi hal-hal praktis yang dapat diperkirakan. Jangan menebak informasi rahasia yang sengaja ditahan oleh canon.
- Estimasi awal harus ditandai sebagai estimasi di catatan GM atau deskripsi terkait agar tidak disalahartikan sebagai informasi eksplisit dari pemain. Setelah permainan berjalan, angka dan detail tersebut menjadi state awal sampai diubah oleh kejadian yang sah.

## Protokol Bootstrap dan State — WAJIB

Pilih satu alur sebelum menulis gameplay:

1. **Sesi baru dengan karakter terdaftar:** baca `INDEX.md`, `templates/GM_PROMPT.md`, entri `players.md`, template ini, `core/HP_SYSTEM.md`, serta modul waktu/lokasi dan mekanik yang diperlukan. Gunakan registry sebagai state awal saja. Tetapkan satu timestamp lengkap dan mulai adegan langsung; jangan tampilkan laporan teknis bootstrap.
2. **Sesi berlanjut:** gunakan profil gameplay terakhir dan semua kejadian setelahnya. Jangan memuat ulang statistik awal dari registry, mengulang timestamp awal, atau menghapus konsekuensi.
3. **Karakter baru:** gunakan sumber resmi yang relevan. Tanyakan hanya nama/lokasi awal yang benar-benar diperlukan dan belum dapat disimpulkan. Jangan menyatakan asumsi GM sebagai fakta yang diberikan pemain.

Sebelum respons gameplay, pastikan urutan tetap **timestamp dua baris → heading Narasi → profil lengkap**. Format timestamp harus sama dengan contoh di atas, termasuk kolom `[Era sesi]`; setelah waktu awal ditetapkan, lanjutkan dari timestamp terakhir yang sah. Setiap field profil tetap ada meskipun nilainya belum diketahui.

## Protokol Transaksi dan Saldo — WAJIB

- Saldo awal harus berasal dari registry atau estimasi awal GM yang masuk akal dan ditandai sebagai estimasi; jangan menciptakan riwayat transaksi sebelum sesi.
- Ubah saldo hanya setelah transaksi benar-benar disepakati dan terlaksana. Harga yang disebut, tawaran, atau negosiasi yang belum selesai tidak mengubah saldo.
- Saat transaksi, appraisal, tawar-menawar, atau perubahan uang, baca `core/10_ECONOMY_SYSTEM.md`. Kurs resmi: 100 xc = 1 xs; 100 xs = 1 xg; 1.000 xg = 1 zj; 10 zj = 1 az.
- Hitung saldo tanpa kehilangan sisa. Jika diperlukan, hitung melalui xc sebagai satuan hitung, lalu tampilkan saldo dalam format wajib `...xc | ...xs | ...xg | ...zj | ...az`. Jangan mengarang harga regional atau membulatkan saldo.
- Catat perubahan saldo bersamaan dengan perubahan inventory/assets. Jika transaksi atau saldo tidak bisa dipastikan dari riwayat, tandai konflik dan jangan menebak.

## Format Field Profil

1. **Nama dan Usia:** gunakan data yang sudah tercatat. Jika usia tidak eksplisit tetapi dapat disimpulkan dari petunjuk kuat, gunakan perkiraan paling masuk akal dan tandai sebagai estimasi GM.
2. **Spirit Realm:** gunakan `Nama Realm/angka Stage`, dengan Stage numerik: `1` = Early, `2` = Middle, `3` = Late, `4` = Peak. Mortal tidak memiliki Stage kultivasi dan ditulis `Mortal/0`. Jika belum ada dasar untuk menentukan Realm, gunakan `???/???`.
3. **Sync progress:** gunakan format `progres saat ini%/batas kompatibilitas maksimum%`. Batas tiap ring dapat berbeda dan tidak otomatis 100%. Jika karakter belum memiliki ring atau sistem belum menetapkan nilai yang dapat diperkirakan, tulis `???%/???%`.
4. **Breakthrough:** tampilkan status dan sisa jeda minimum dalam format `status | jumlah Day left`, sesuai modul resmi. Jika belum relevan bagi karakter Mortal, tulis `Not applicable | 0 Day left`. Jika relevan tetapi data resmi yang dibutuhkan belum tersedia, gunakan `??? | ??? Day left`.
5. **Martial Soul:** gunakan data canon yang sudah ditetapkan. Jika belum awakening, jangan menyimpulkan hanya dari status Mortal; gunakan petunjuk latar dan aturan awakening. Bila benar-benar belum diketahui, tandai `???` dan catat statusnya untuk GM.
6. **Thinker Grade:** gunakan angka Grade 1–10 sesuai modul Thinker. Jika modul atau dasar penilaiannya belum tersedia, gunakan `???` dan jangan menciptakan aturan Grade baru.
7. **HP:** gunakan `HP saat ini/HP maksimum` sesuai `core/HP_SYSTEM.md`. Jangan otomatis mengisi HP saat ini dengan nilai maksimum. Jika rumus resmi belum tersedia, jangan mengarang angka yang diklaim berasal dari sistem; gunakan perkiraan awal GM yang ditandai jelas bila perlu untuk memulai permainan.
8. **Qi:** jika karakter belum menyerap Spirit Ring pertama, tulis tepat `...`. Setelah ring pertama berhasil diserap, gunakan `Qi saat ini/Qi maksimum` sesuai `core/SPIRIT_RING_RULES.md`.
9. **Currency:** gunakan format persis `...xc | ...xs | ...xg | ...zj | ...az`. Jika saldo tidak disebutkan, wajib tetapkan perkiraan kasar dan isi semua pecahan; jangan meninggalkan seluruh saldo sebagai `???`. Jangan mengklaim nilai tukar resmi jika belum ada aturan resmi.
10. **Kondisi Tubuh, Equipment, Inventory, Assets, Teknik / Kemampuan, dan Tujuan Saat Ini:** isi berdasarkan latar serta kejadian. Jika detail tidak eksplisit tetapi dapat diperkirakan, tetapkan estimasi GM yang masuk akal. Catat kondisi tersembunyi secara terpisah sebagai informasi khusus GM.

## Aturan Penggunaan

- Gunakan hanya mekanik resmi yang tersedia dalam repository. Jangan mengarang rumus atau menyebut estimasi GM sebagai mekanik resmi.
- Field yang belum diketahui setelah upaya penetapan hanya boleh memakai placeholder sesuai aturan di atas; jangan membiarkan informasi praktis yang dapat diperkirakan kosong.
- Pertahankan semua perubahan profil yang didukung kejadian dalam gameplay. Jangan menghapus luka, pengeluaran, barang, atau konsekuensi tanpa alasan sah.
- Profil pada setiap balasan adalah snapshot keadaan karakter setelah giliran tersebut.