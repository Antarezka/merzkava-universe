# Xuanling Realm — Player Character Registry

File ini adalah daftar karakter pemain yang terdaftar untuk memulai sesi roleplay.

## Format Wajib Setiap Balasan Gameplay — MODE: NO STEP

Setiap balasan gameplay wajib memakai urutan berikut, tanpa menghilangkan bagian waktu, narasi, atau satu pun field profil. Struktur header waktu harus sama persis dengan `templates/CHARACTER_PROFILE_TEMPLATE.md` dan `templates/GM_PROMPT.md`:

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

Gunakan juga aturan rinci di `templates/CHARACTER_PROFILE_TEMPLATE.md`. Mode NO STEP berarti jangan mengubah balasan menjadi daftar langkah atau menu tindakan.

### Protokol Konsistensi Waktu dan Kalender — WAJIB

- Gunakan dua baris header waktu di atas **secara persis** pada setiap balasan gameplay. Jangan mengganti nama label, urutan kolom, atau menghilangkan bagian `Era sesi`.
- Pada sesi baru tanpa timestamp sebelumnya, tetapkan satu waktu awal yang lengkap: tahun, era sesi, musim, tanggal, hari, cuaca, dan jam. Setelah itu, semua giliran wajib berlanjut dari timestamp terakhir yang benar-benar ditampilkan.
- Untuk sesi yang berlanjut, jangan mengulang waktu awal atau membuat timestamp baru secara acak. Riwayat percakapan dan timestamp terakhir adalah acuan utama.
- Jika belum ada kalender resmi yang dapat diakses, gunakan kalender kerja sesi: 12 bulan per tahun, 30 hari per bulan; bulan 1–3 Semi, 4–6 Panas, 7–9 Gugur, 10–12 Dingin; hari berulang Senin–Minggu. Hitung pergantian hari, bulan, tahun, dan musim sesuai kalender ini.
- Jangan mengganti sistem kalender di tengah sesi. Jika kalender resmi ditemukan kemudian dan bertentangan dengan kalender kerja sesi, jangan mengubah tanggal secara diam-diam; tandai konflik dan ikuti sumber resmi setelah konflik diselesaikan.
- Majukan jam hanya sesuai durasi aksi atau kejadian yang benar-benar berlangsung. Jangan memajukan waktu tanpa sebab, dan jangan menganggap satu balasan selalu sama dengan durasi tertentu.
- Tetapkan cuaca awal yang masuk akal dan pertahankan sampai ada alasan waktu/lokasi/naratif yang masuk akal untuk mengubahnya. Jangan mengundi ulang cuaca setiap giliran.
- Kalender atau era yang diimprovisasi untuk menutup kekosongan hanya berlaku sebagai **kalender kerja sesi**, bukan otomatis canon global. Jangan mengarang nama era resmi; jika era resmi tidak diketahui, pakai label era sesi yang netral dan konsisten.
- Jangan memakai placeholder seperti `...`, `XXXX`, atau `???` untuk timestamp gameplay setelah sesi dimulai. Placeholder hanya boleh ada pada contoh template, bukan pada balasan permainan.

### Aturan Wajib Data yang Tidak Disebutkan

- Jika latar belakang tidak menyebut jumlah uang, aset, inventaris, perlengkapan, teknik bawaan, kondisi tubuh tersembunyi, kebiasaan biologis, atau detail praktis lain, GM **wajib membuat perkiraan kasar yang masuk akal** berdasarkan latar karakter. Jangan otomatis memakai `???` untuk hal yang bisa diperkirakan.
- Tetapkan saldo awal dan isi inventaris secara konkret. Isi semua pecahan Currency; angka tersebut adalah estimasi awal GM, bukan fakta eksplisit dari pemain. Untuk transaksi dan konversi, gunakan hanya kurs resmi dari `core/10_ECONOMY_SYSTEM.md`; jangan menciptakan kurs baru atau harta luar biasa tanpa dasar.
- Tetapkan keterampilan biasa, naluri, potensi pasif, dan kondisi tersembunyi yang wajar jika didukung latar. Pisahkan informasi khusus GM dari hal yang diketahui karakter. Bakat tersembunyi tidak otomatis berarti karakter menguasai teknik aktif.
- Gunakan `???` hanya untuk misteri inti atau hal yang memang tidak dapat diperkirakan secara bertanggung jawab. Jangan menciptakan garis keturunan, artefak kuat, atau rahasia besar tanpa petunjuk.

### Aturan Wajib Penentuan Lokasi Awal

- **GM wajib menetapkan lokasi awal konkret sebelum gameplay dimulai** apabila lokasi karakter belum ditulis eksplisit. Dilarang membiarkan field lokasi awal tetap `???` jika latar memberi petunjuk yang bisa digunakan.
- Baca latar karakter secara aktif dan tarik kesimpulan dari tempat ia dibesarkan, pekerjaan saat ini, lingkungan sosial, relasi, kondisi ekonomi, kebiasaan, serta kejadian yang disebutkan. Pilih lokasi yang paling dekat dan logis dari petunjuk itu.
- Jika karakter dibesarkan dan bekerja di suatu tempat, lokasi awal default adalah tempat tersebut atau lokasi terdekat yang masuk akal—bukan tempat acak yang tidak berhubungan dengan latarnya.
- Jika nama resmi bangunan atau alamat tepat tidak diketahui, tetapkan lokasi pada tingkat yang cukup konkret, misalnya **paviliun hiburan tempat karakter dibesarkan, di kawasan hiburan kota kekaisaran**. Jangan mengarang nama tempat canon atau organisasi baru tanpa dasar.
- Tulis hasilnya langsung pada field **Lokasi awal** di entri karakter dan gunakan lokasi yang sama ketika membuka sesi. Menulis aturan umum saja tidak cukup; GM harus benar-benar mengisi field karakter.
- Tandai lokasi sebagai **estimasi awal GM berdasarkan latar**, bukan fakta eksplisit pemain. Setelah ditetapkan, pertahankan konsistensinya sampai ada kejadian yang sah mengubah lokasi.
- Jika ada beberapa pilihan, pilih yang paling kuat didukung latar. Hanya jika latar sama sekali tidak memberi petunjuk, pilih lokasi netral yang wajar dan tandai sebagai estimasi GM. Bahkan dalam kasus itu, jangan biarkan field lokasi kosong atau `???`.

### Aturan Wajib Latar Belakang Orisinal

- Latar belakang wajib disalin dan dipertahankan secara **lengkap sesuai teks orisinal yang diberikan pemain**. Jangan meringkas, memangkas, menghilangkan detail, mengubah makna, atau menulis ulang dengan kata-kata sendiri.
- Jika latar belakang orisinal perlu dipindahkan ke file ini, masukkan seluruh teksnya tanpa mengurangi bagian apa pun. Pertahankan detail, hubungan, deskripsi, kejadian, dan misteri seperti yang ditulis pemain.
- **Yang boleh diperbarui seiring gameplay hanya data karakter yang memang dapat berubah**, misalnya uang/harta, inventaris, perlengkapan, kondisi tubuh, luka, teknik, kemampuan yang telah dipelajari, status perkembangan, dan informasi progres lainnya.
- Perubahan pada data yang dapat berkembang tidak boleh digunakan sebagai alasan untuk mengubah latar belakang orisinal. Jika pemain ingin merevisi latar belakang, lakukan hanya atas permintaan eksplisit pemain.
- Field profil wajib mengikuti nama dan urutan resmi dalam template. Informasi tambahan yang diperlukan GM boleh dicatat pada bagian catatan canon/GM setelah profil, tanpa mengubah atau menghilangkan field wajib.
- Tambahkan dan tetapkan informasi ekonomi, perlengkapan, inventaris, teknik/kemampuan, Martial Soul, bakat, garis keturunan, serta kondisi tersembunyi berdasarkan latar. Jika jumlah atau detail praktis tidak disebutkan, gunakan estimasi kasar GM yang masuk akal dan tandai sebagai estimasi. Bedakan fakta tersembunyi yang diketahui GM dari hal yang diketahui karakter.
- Jangan menciptakan keistimewaan luar biasa tanpa petunjuk. Namun, **jumlah uang, inventaris dasar, keterampilan praktis, dan kondisi tubuh tersembunyi yang masuk akal wajib diperkirakan**, bukan dibiarkan kosong atau ditulis `???` hanya karena tidak disebutkan eksplisit.

## Aturan Penggunaan

- Saat sesi baru dimulai sebagai karakter terdaftar, AI GM wajib membaca file ini dan memuat entri karakter yang cocok.
- Data di sini adalah titik awal karakter, bukan save otomatis atau catatan progres terbaru.
- AI GM tidak boleh mengubah file ini selama gameplay tanpa permintaan eksplisit pemilik/pemain yang berwenang.
- Jangan mengarang entri karakter yang belum terdaftar.
- Pemain/pemilik repository dapat menambahkan karakter baru menggunakan format yang sama.

---

### Gerbang Bootstrap — Jangan Campur State Awal dan State Berjalan

Sebelum memulai atau melanjutkan gameplay, GM wajib menentukan mode:

- **Sesi baru sebagai karakter terdaftar:** cari nama karakter di registry ini dan gunakan entri tersebut sebagai snapshot awal sesi. Baca template profil dan modul relevan. Tetapkan timestamp awal sekali, lalu mulai dari lokasi awal yang tercatat. Jangan menciptakan riwayat transaksi, klien, luka, atau kejadian sebelum sesi.
- **Sesi berlanjut dalam percakapan yang sama:** profil gameplay terakhir dan kejadian sesudahnya adalah state aktif. Registry ini bukan save otomatis; jangan menimpa progres, waktu, inventaris, atau saldo dengan data awal.
- **Karakter baru yang belum terdaftar:** jangan mengarang entri registry. Gunakan latar/input pemain dan template untuk membuat profil awal di percakapan; tanyakan hanya informasi yang benar-benar diperlukan.
- **Sumber penting gagal diakses:** nyatakan file yang gagal, jangan mengklaim telah membacanya, dan jangan mengarang isi yang hilang.

Setelah memilih mode, urutan respons pertama adalah: timestamp lengkap → narasi pembuka dari state yang sah → profil lengkap. Jangan tampilkan laporan teknis bootstrap sebagai pengganti gameplay.

### Gerbang Pencatatan Uang

- Saldo awal dalam registry adalah state awal, bukan bukti bahwa transaksi baru saja terjadi.
- Setiap transaksi harus menyebut perubahan saldo yang dapat dihitung dan memakai `core/10_ECONOMY_SYSTEM.md` untuk kurs, harga, tier kualitas, kelangkaan, dan penyesuaian pasar.
- Catat transaksi secara ringkas di narasi/riwayat gameplay; bingkai profil tetap memakai field Currency yang ada.
- Jika tidak ada transaksi atau peristiwa ekonomi yang sah, saldo wajib tetap sama. Jangan mengubah saldo saat bootstrap atau hanya untuk menormalkan pecahan.

## Daftar Karakter

### Yuha

#### Profil Karakter

- **Nama:** Yuha
- **Usia:** 14 tahun (tersirat dari petunjuk warisan yang ditinggalkan untuknya tepat empat belas tahun kemudian).
- **Spirit Realm:** Mortal/0
- **Sync progress:** ???%/???%
- **Breakthrough:** ??? | ??? Day left
- **Martial Soul:** ???
- **Thinker Grade:** ???
- **HP:** ???/100
- **Qi:** ...
- **Kondisi Tubuh:** ???
- **Equipment:** Hanfu hitam polos berlengan panjang; kacamata tipis; tongkat jalan.
- **Inventory:** Sepuluh giok kecil peninggalan; hanfu hitam polos cadangan sederhana; kantong uang; sisir kayu; kain lap/kain saputangan; botol air kecil; bekal ringan; perlengkapan kebersihan dasar. Semua barang selain sepuluh giok adalah **estimasi awal GM** berdasarkan keseharian dan pekerjaan Yuha. Fungsi khusus dan nilai giok tetap belum diketahui.
- **Assets:** Memperoleh bayaran yang cukup besar dari pekerjaan sebagai escort/teman bicara bagi para putri bangsawan. **Estimasi awal GM:** tabungan dan uang tunai yang masih tersisa tergolong cukup untuk kebutuhan pribadi sederhana, tetapi bukan kekayaan besar; penghasilan masa lalu tidak dianggap seluruhnya masih tersimpan. Utang besar tidak ditetapkan tanpa bukti.
- **Currency (xuan/zun):** 18xc | 6xs | 2xg | 0zj | 0az (**estimasi saldo awal GM**; bukan transaksi atau penghasilan baru yang terjadi di awal sesi. Saat ada transaksi, gunakan kurs resmi `core/10_ECONOMY_SYSTEM.md` dan catat perubahan secara eksplisit).
- **Teknik / Kemampuan:** Kemampuan percakapan, mendengarkan, menjaga rahasia percakapan, dan membaca suasana sosial—keterampilan praktis yang masuk akal dari pekerjaannya sebagai pendamping. Stamina ekstrem dan indra gerak luar biasa dicatat sebagai potensi/kondisi bawaan pasif, bukan teknik kultivasi atau jurus tempur yang telah dikuasai.
- **Tujuan Saat Ini:** Menjalani pekerjaan yang paling disukainya sebagai pendamping dan teman bicara berbayar; asal-usul serta potensi sejatinya masih belum diketahui olehnya.

#### Latar Belakang Orisinal (Wajib Dipertahankan Utuh)

Yuha adalah seorang bocah Realm Mortal yang luar biasa tampan dan manis, dibesarkan oleh kakak-kakak perempuan yang tinggal di sebuah paviliun hiburan (bordil). Ia ditemukan di dalam sebuah keranjang dengan balutan kain mahal, ditemani sepuluh giok kecil yang merupakan warisan peninggalan seseorang untuknya di masa depan, tepat empat belas tahun kemudian.

Yuha memiliki rambut hitam berantakan yang menutupi dahinya, kacamata tipis, serta sepasang mata biru tua menyerupai mata paus surgawi. Di balik penampilannya yang manis dan terkesan biasa, ia memiliki stamina yang sangat ekstrem, jarang merasa lapar, serta indra pergerakan luar biasa yang mampu menangkap dan merespons gerakan secepat suara. Namun, Yuha sama sekali tidak menyadari kemampuan istimewanya tersebut.

Dalam kesehariannya, Yuha sering menjadi sasaran perundungan seorang gadis muda pewaris konsorsium lelang ternama, yang diam-diam sebenarnya menyukainya. Meski begitu, Yuha tidak terlalu memusingkan hal tersebut dan tetap menjalani pekerjaan yang paling disukainya: menjadi pendamping sekaligus teman bicara bagi para putri kekaisaran, sekte-sekte besar, dan kalangan pemerintahan. Pekerjaannya bukan sebagai pengawal atau pelayan, melainkan sebagai seorang escort yang dibayar untuk menemani mereka berbincang, mendengarkan keluh kesah, dan menghabiskan waktu bersama.

Yuha selalu mengenakan hanfu hitam polos berlengan panjang, dilengkapi sebuah tongkat jalan yang menjadi ciri khasnya. Berkat kepribadiannya yang manis dan kemampuannya menjadi teman bicara yang menyenangkan, ia memperoleh bayaran yang cukup besar dari para putri bangsawan tersebut, meskipun dirinya hanyalah seorang pemuda misterius dari Realm Mortal yang belum mengetahui asal-usul maupun potensi sejatinya.

#### Catatan Canon dan Informasi Khusus GM

- **Bakat / kondisi tubuh tersembunyi (khusus GM):** Stamina sangat ekstrem; kebutuhan makan terasa lebih jarang daripada orang biasa; indra pergerakan luar biasa yang mampu menangkap dan merespons gerakan secepat suara. Yuha belum menyadari sifat-sifat ini dan belum memahami batasnya. Perlakukan sebagai kondisi/potensi bawaan pasif yang harus terungkap melalui kejadian, bukan teknik aktif, kekebalan, atau jaminan menang.
- **Kondisi tubuh tambahan (estimasi awal GM):** Secara umum mampu menjalani aktivitas harian dan pekerjaan pendamping; tidak ada luka berat atau penyakit kronis yang ditetapkan tanpa petunjuk. Kondisi fisik dan batas sebenarnya dari stamina serta indra geraknya belum dipahami Yuha.
- **Keterampilan praktis (estimasi awal GM):** Terlatih berbicara sopan, mendengarkan, membaca suasana sosial, dan menjaga percakapan tetap nyaman. Ini bukan kemampuan memengaruhi pikiran atau membuat orang otomatis menyukainya.
- **Garis keturunan / asal-usul:** ???. Kemiripan mata dengan paus surgawi tidak membuktikan garis keturunan tertentu.
- **Kemampuan khusus dan kondisi tersembunyi lain:** ???. Jangan mengungkap asal-usul Yuha atau fungsi sepuluh giok tanpa perkembangan cerita yang sah.
- **Lokasi awal:** Paviliun hiburan tempat Yuha dibesarkan, di kawasan hiburan Kota Kekaisaran (**estimasi awal GM berdasarkan latar**: Yuha dibesarkan di paviliun hiburan dan bekerja sebagai pendamping bagi para putri kekaisaran, sekte besar, serta kalangan pemerintahan; nama resmi paviliun belum ditetapkan).
- **Relasi penting:** Seorang gadis muda pewaris konsorsium lelang ternama sering merundung Yuha, tetapi diam-diam menyukainya. Identitas dan detail lain yang belum ditetapkan tetap ???
- **Batas penafsiran:** Pekerjaan Yuha adalah escort/teman bicara berbayar, bukan pengawal atau pelayan. Jangan menetapkan harga/nilai giok, Martial Soul, atau garis keturunan tanpa dasar yang sah. Lokasi awal sudah ditetapkan sebagai estimasi yang paling sesuai dengan latar dan tidak boleh dikembalikan ke `???` tanpa alasan cerita yang sah.
