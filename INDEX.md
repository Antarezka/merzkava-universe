# Merzkava Universe — Official Index

INDEX ini adalah **pintu masuk tunggal** untuk memulai, melanjutkan, dan menjalankan roleplay Merzkava Universe. Ikuti prosedur bootstrap dan navigasi modul di bawah. Jangan menggandakan aturan mekanik atau format respons lengkap ke file lain.

Repository resmi: https://github.com/Antarezka/merzkava-universe

## Struktur Repositori Wilayah — WAJIB

Struktur wilayah yang dimaksud adalah **tepat tiga kekuasaan besar**, bukan satu repo untuk setiap provinsi, kawasan, kota, atau desa:

1. **Golden Dragon Empire** — satu repositori untuk seluruh wilayah kekaisaran, seluruh subwilayah/permukiman di dalamnya, pemerintahan, faksi, jalur, serta NPC yang berasal atau bernaung di sana.
2. **Tianhai Yunzhou** — satu repositori untuk seluruh Tianhai, termasuk kawasan, kota terapung, akademi, institut, jalur transit, faksi, serta NPC Tianhai.
3. **Beiming Gu** — satu repositori untuk seluruh Beiming Gu, termasuk kawasan-kawasannya, permukiman, jalur darat/laut, faksi, serta NPC Beiming Gu.

**Kunci nama kanonis:** ikuti persis nama yang ditetapkan `world/WORLD.md`: **Golden Dragon Empire**, **Tianhai Yunzhou**, dan **Beiming Gu**. Jangan mengganti nama resmi dengan terjemahan, membuat nama alternatif, atau menulis nama wilayah yang berbeda pada indeks, aturan navigasi, maupun arsitektur repositori.

**Subwilayah bukan repositori tersendiri.** Kota/desa/kawasan dan NPC ditempatkan di dalam repositori kekuasaan besarnya masing-masing. NPC disimpan di repositori wilayah asal/afiliasi kanonisnya, bukan di repositori NPC global terpisah.

- `merzkava-universe` tetap menjadi repo pusat: indeks global, aturan/mekanik lintas wilayah, template, canon global, dan tautan ke tiga repo kekuasaan besar.
- Pola navigasi mengikuti `world/REGIONAL_REPOSITORY_ARCHITECTURE.md` dan pendekatan hub-and-spoke: INDEX pusat → repo kekuasaan yang sesuai → INDEX lokal → modul lokasi/permukiman dan registry NPC → profil NPC relevan.
- Jangan membuat atau menebak URL repositori. Tautan harus mengarah ke repositori nyata dan diverifikasi sebelum dipakai.
- **Status implementasi:** profil lengkap NPC yang sudah terverifikasi kini berada di folder staging `regions/golden-dragon-empire/npcs/`, `regions/tianhai-yunzhou/npcs/`, dan `regions/beiming-gu/npcs/`, masing-masing dengan INDEX/registry sesuai struktur regional. Beiming Gu kini memiliki profil kanonis untuk Beiming Han, Beiming Xenhwa, dan Beiming Jingheng. Path lama `world/NPC_*.md` tetap harus diperlakukan sesuai isi aktualnya; jangan menganggap semua path lama sudah menjadi pointer tanpa memverifikasinya. Ketiga folder staging masih berada di repo pusat karena repositori GitHub wilayah terpisah belum tersedia/terverifikasi; jangan mengklaim pemisahan tiga repo sudah selesai.

## 0. Prosedur Bootstrap (WAJIB)

Saat pemain memakai trigger awal yang merujuk INDEX.md dan players.md, perlakukan pesan itu sebagai perintah untuk menginisialisasi gameplay — bukan permintaan untuk sekadar menganalisis atau merangkum tautan.

**Aturan canon final:** jika ada keputusan owner yang sudah ditetapkan atau konflik antara file, baca `world/CANON_DECISIONS_AND_PRECEDENCE.md` bersama sumber khusus topik. File yang baru ditambahkan tidak otomatis mengalahkan keputusan final yang lebih lama; selaraskan informasi baru dengan canon yang berlaku kecuali owner secara eksplisit merevisinya.

1. **Baca seluruh INDEX.md ini terlebih dahulu.** Gunakan direktori dan aturan navigasi di bawah untuk menemukan sumber resmi; jangan mengandalkan ingatan bebas jika sumber repository dapat diakses.
2. **Fetch dan baca `templates/AUTHORITY_ORDER.md` sebelum memutuskan atau menarasikan hasil gameplay.** File ini menetapkan perilaku GM, anti-cheat, mode sesi, dan resolusi aksi.
3. **Kenali apakah sesi baru atau berlanjut dari pesan pemain dan riwayat chat yang tersedia.** Jangan menganggap semua penyebutan nama karakter sebagai jenis sesi yang sama:
   - **A. Sesi berlanjut / recall:** profil gameplay terakhir atau riwayat karakter masih tersedia di percakapan saat ini. Gunakan state terbaru itu; jangan fetch snapshot awal untuk menimpanya. Jika state terakhir tidak tersedia, minta pemain memberikan profil terakhir yang diperlukan.
   - **B. Calon sesi baru:** tidak ada profil gameplay berjalan untuk karakter itu di percakapan saat ini. Tunda pengecekan registry dan pemilihan snapshot sampai template canonical selesai dimuat pada langkah 4; setelah itu, cocokkan nama karakter dengan `players.md`.
4. **Muat template sebelum memuat snapshot karakter atau menulis respons gameplay.** Fetch dan baca seluruh `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` terlebih dahulu, lalu seluruh `templates/CHARACTER_PROFILE_TEMPLATE.md`. Keduanya wajib; jangan mengganti format canonical dengan daftar bullet atau format buatan sendiri.
5. **Pilih dan inisialisasi state karakter dari sumber yang tepat.** Setelah langkah 4, baca `players.md` untuk memeriksa registry. Jika karakter terdaftar dan sesi baru, fetch tautan RAW file individualnya dan baca seluruh isi sebagai snapshot awal. Jika nama tidak terdaftar dan tidak ada state di riwayat, perlakukan sebagai karakter baru dengan mengikuti template profil dan Authority Order; jangan mengarang rahasia inti atau kemampuan formal. Pertahankan identitas, latar belakang, lokasi awal, hubungan, equipment, inventory, assets, Currency, kemampuan, catatan canon, estimasi awal, batas penafsiran, informasi khusus GM, serta Session Continuity. Bedakan fakta canon, estimasi GM, informasi khusus GM, dan pengetahuan karakter.
6. **Baca modul berdasarkan lokasi, state, dan kebutuhan gameplay.** Tentukan lokasi awal dari snapshot karakter atau input pemain, lalu baca modul world/lokasi yang relevan serta modul mekanik yang dibutuhkan untuk menghitung state awal dan aksi pertama. Jangan fetch seluruh repository sekaligus.
7. **Periksa `world/DYNAMIC_EVENTS.md` sebelum gameplay pertama dan setiap giliran gameplay.** Terapkan hanya event yang benar-benar terdaftar dan relevan. Jika file gagal diakses, ungkapkan kegagalan itu; jangan mengarang event.
8. **Validasi sebelum menjawab.** Cocokkan seluruh data karakter dengan template profil, pastikan field wajib tidak hilang, dan pastikan nilai tercatat tidak diganti dengan placeholder. `???` hanya boleh dipakai untuk identitas karakter yang benar-benar tidak dikenal atau nama Martial Soul yang belum diketahui. Field numerik yang belum memiliki nilai memakai `0`, kecuali HP awal yang diinisialisasi menurut aturan HP dan field hitung-mundur yang memiliki arti mekanik khusus. Untuk karakter tanpa saldo tercatat, pastikan saldo bootstrap satu kali sudah ditetapkan konkret sebelum profil pertama ditampilkan. Gunakan timestamp yang konsisten sesuai modul waktu.
9. **Mulai gameplay langsung** menggunakan `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`. Jangan membalas trigger dengan laporan bootstrap, daftar file yang dibaca, atau ringkasan analisis sebagai pengganti adegan.
10. **Selama permainan, navigasikan modul secara dinamis** memakai tabel pemicu di bawah. Jika modul sudah dibaca di percakapan yang sama dan belum berubah atau tidak ada alasan untuk mengambil ulang, gunakan konteks tersebut secara konsisten.

### Gerbang format → profil player → ekonomi (URUTAN MUTLAK)

Jangan mulai menulis narasi atau profil gameplay sampai tiga sumber ini selesai dimuat, dalam urutan berikut:

1. **Format visual percakapan:** baca seluruh `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`. Format ini mengunci bentuk visual, garis/kotak, urutan field, nama field, catatan, dan penutup. Jangan membuat format sendiri.
2. **Definisi field profil:** baca seluruh `templates/CHARACTER_PROFILE_TEMPLATE.md` agar setiap nilai ditempatkan pada field yang benar.
3. **Profil player:** untuk sesi baru karakter terdaftar, baca `players.md`, lalu baca seluruh `players/<Nama>.md`. Untuk sesi berjalan, gunakan profil gameplay terakhir dan kejadian setelahnya sebagai state aktif; snapshot awal hanya referensi latar yang belum berubah.
4. **Sumber saldo Wallet (bootstrap wajib):** untuk sesi baru, cocokkan nama karakter dengan `players.md`, lalu baca penuh file individual yang tepat `players/<Nama>.md` dan ambil saldo Wallet/Currency yang tercatat di sana. Jangan mengambil saldo dari karakter lain. Jika Authority secara eksplisit menyediakan saldo sah untuk karakter/sesi tersebut, gunakan sumber Authority itu dan abaikan pencarian saldo awal pada snapshot. Untuk sesi berlanjut/recall, gunakan Wallet pada profil gameplay terakhir lalu terapkan hanya transaksi sah setelahnya. `core/10_ECONOMY_SYSTEM.md` adalah sumber aturan kurs, harga, dan transaksi—bukan sumber saldo individual.
   - Jika file karakter yang cocok sudah mencatat saldo awal, gunakan persis saldo tersebut tanpa random ulang. Jika saldo tidak tercatat di snapshot maupun sumber Authority yang berlaku, tetapkan satu saldo awal konkret melalui undian bootstrap satu kali berdasarkan `core/10_ECONOMY_SYSTEM.md` sebelum respons pertama, lalu tampilkan dan pertahankan saldo itu di profil sesi. Undian tidak boleh dihitung dari latar, pekerjaan, Assets, atau penghasilan masa lalu dan bukan klaim transaksi masa lalu.
   - Setelah saldo awal ditetapkan, pertahankan di profil sesi dan jangan mengundi ulang atau mengubahnya hanya karena giliran baru. Setiap transaksi harus memiliki sebab, waktu, nilai masuk/keluar, dan saldo sesudah transaksi yang dapat diverifikasi dari kejadian/riwayat sesi. Catat setiap pemasukan dan pengeluaran sebagai entri ledger berkelanjutan sesuai `core/10_ECONOMY_SYSTEM.md`; saldo Wallet pada profil harus cocok dengan saldo ledger terakhir. Setiap perubahan Inventory, Equipment, atau Assets yang melibatkan item juga wajib dicatat dalam ledger item berkelanjutan di `core/10_ECONOMY_SYSTEM.md`, termasuk item/jumlah sebelum-sesudah, sumber/tujuan, alasan, dan kondisi akhirnya. Pembelian atau penjualan harus memiliki catatan yang saling cocok pada ledger uang dan ledger item; profil harus sesuai dengan catatan terakhir keduanya.
5. **Pemetaan ke bagan:** baru setelah langkah 1–4, tempatkan setiap data pada field template visual. Wallet harus disalin persis dari file karakter yang cocok atau profil sesi aktif setelah menerapkan transaksi sah, kecuali Authority secara eksplisit menetapkan sumber yang lebih berwenang; aset bangunan/properti yang benar-benar dimiliki dicatat di `Assets Bangunan`; uang hanya di `Wallet (wealth)` dan barang bawaan di `Inventory`. Jangan mengubah nilai tercatat menjadi `???`, membulatkan saldo, atau mengganti format mata uang.
6. **Modul mekanik dan dunia:** setelah sumber state dimuat, baca modul yang diperlukan untuk timestamp, Satiety, HP, lokasi, event, dan aksi pertama. Jika sumber wajib gagal dibaca, jangan berpura-pura selesai.

**Gate sebelum respons:** pastikan format visual canonical sudah dimuat; profil/snapshot yang benar sudah dipilih; saldo Currency memiliki sumber yang jelas; Currency cocok dengan semua transaksi sah sejak saldo tersebut; seluruh field wajib dan ornamen visual dipertahankan. Jika satu gate belum terpenuhi, jangan kirim gameplay seolah-olah bootstrap lengkap.

### Protokol pemuatan karakter terdaftar

- `players.md` adalah **indeks karakter**, bukan file yang memuat seluruh ingatan karakter.
- File `players/<Nama>.md` adalah snapshot awal yang wajib dibaca penuh pada sesi baru untuk karakter terdaftar.
- Jangan menghilangkan data yang berada di bagian latar belakang, catatan khusus GM, aset, inventaris, relasi, atau batas penafsiran hanya karena field tersebut tidak tampil sebagai field terpisah di profil gameplay.
- Baca `core/10_ECONOMY_SYSTEM.md` saat menetapkan atau mengubah saldo, aset, transaksi, maupun harga. Pertahankan saldo yang tercatat di snapshot/profil sesi; jangan mengubah estimasi awal menjadi klaim bahwa transaksi masa lalu tertentu benar-benar terjadi.
- Baca `core/HUNGER_AND_METABOLISM.md` saat menetapkan Satiety atau menghitung perubahan karena waktu/makanan. Jangan otomatis menetapkan Satiety ke 100 jika sumber dan prosedur resmi tidak mendukungnya.
- Informasi khusus GM digunakan untuk konsistensi dunia, tetapi tidak otomatis diketahui karakter.
- Jika sumber wajib gagal diakses, sebutkan file yang gagal. Jangan mengklaim sudah membaca sumber yang tidak berhasil diambil.

### 1. Baca modul sesuai kebutuhan
Pilih modul berdasarkan aksi, kondisi, dan lokasi saat ini. Jangan membaca atau mengarang modul yang tidak tersedia hanya karena jalurnya tercantum di peta.

| Kebutuhan | Sumber resmi |
|---|---|
| Definisi field profil dan konsistensi state | `templates/CHARACTER_PROFILE_TEMPLATE.md` |
| Kalender, timestamp, durasi aksi, time skip | `gameplay/TIME_AND_ACTION_RULES.md` |
| Spirit Realm, Stage, Sync, bottleneck, breakthrough | `core/CULTIVATION_SYSTEM.md` |
| Akademi kultivator dan pendidikan dasar | `core/CULTIVATOR_ACADEMIES.md` |
| Keputusan canon final, prioritas sumber, dan aturan sinkronisasi file lama/baru | `world/CANON_DECISIONS_AND_PRECEDENCE.md` |
| Prosedur awakening, tabel rarity, undian dan keputusan mutasi Martial Soul | `core/MARTIAL_SOUL_AWAKENING.md` |
| Lore, bentuk, karakteristik, dan interpretasi Martial Soul | `core/MARTIAL_SOUL.md` |
| Spirit Ring, kompatibilitas, penyerapan, kombinasi kemampuan, Qi, PowerScale, jalur perolehan ring | `core/SPIRIT_RING_RULES.md` |
| Spirit Beast, syarat ring, jeda minimum, deviasi | `bestiary/SPIRIT_BEAST_RULES.md` |
| Combat, serangan beruntun, multi-hit, combo, damage, pertahanan | `gameplay/COMBAT_SYSTEM.md` |
| HP | `core/HP_SYSTEM.md` |
| Cedera dan pemulihan injury | `core/INJURY_SYSTEM.md` |
| Thinker Grade, formulasi, produksi Artificial Artifact | `core/THINKER_AND_FORMULATION.md` |
| Harga, transaksi, kurs, aset, Currency | `core/10_ECONOMY_SYSTEM.md` |
| Total kekayaan global dan persebaran Xuan Gold per wilayah/pemegang | `world/WEALTH_DISTRIBUTION.md` |
| Lapisan sosial, kemiskinan, kawasan kumuh, tunawisma, dan mobilitas sosial | `world/SOCIAL_STRATIFICATION.md` |
| Dunia, tokoh, tiga kekuasaan utama, fondasi lore | `world/WORLD.md` |
| Struktur pemerintahan sipil dan militer Golden Dragon Empire, kementerian, dan jenjang administrasi | `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md` |
| Nama dan jumlah regional, prefektur, county, kota, kota kecil, distrik, serta desa Golden Dragon Empire | `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md` |
| Peta, wilayah, permukiman, rute yang diketahui | `world/MAP_AND_REGIONS.md` |
| Geografi fisik, perjalanan, moda transportasi, dan batas pengetahuan rute | `world/GEOGRAPHY_AND_TRAVEL.md` |
| Bangsa berakal, ciri kelompok, dan konteks perlakuan sosial | `world/INTELLIGENT_PEOPLES.md` |
| Klan, dojo, sekte, organisasi, Medicine Hall Society, Ordo Suci Tianming | `world/FACTIONS.md` |
| Serikat Guild: kontrak lintas jenis pekerjaan, enam tingkat kesulitan, party sementara, perburuan Spirit Beast, blacklist, dan kontrak buruan Deadpool | `world/SPIRIT_HUNTERS_GUILD.md` |
| Geografi dan lore kawasan suci Wanluo, World Knowledge Tower, distrik, jalur ziarah, serta kompleks Ordo Suci Tianming | `world/WANLUO_SACRED_EXPANSE.md` |
| Kronologi, bukti sejarah, peristiwa historis yang sudah mapan | `world/HISTORY.md` |
| Event dunia dinamis yang aktif/berakhir, status event, dampak lintas sesi, dan sumber konfirmasi | `world/DYNAMIC_EVENTS.md` |
| Form proposal untuk menambah/memperbarui event dunia; bukan canon sampai disetujui admin | `templates/WORLD_EVENT_UPDATE_TEMPLATE.md` |
| Kategori Relic/Ancient Artifact dan katalog | `world/ARTIFACTS_AND_RELICS.md` |
| Katalog dan lore Artificial Artifact | `world/ARTIFICIAL_ARTIFACTS.md` |
| Satiety, jadwal makan, metabolisme Spirit Realm, tidur malam, dan pengubah kondisi tubuh | `core/HUNGER_AND_METABOLISM.md` |

Untuk aksi yang menyentuh beberapa sistem, baca semua modul yang relevan. Contoh: combat yang mengubah HP dan menimbulkan luka memerlukan Combat, HP, Injury, Time, dan Hunger/Metabolism bila waktu aktif berlalu. Produksi Artificial Artifact menggunakan mekanik di `core/THINKER_AND_FORMULATION.md`; file lore artefak tidak menggantikan aturan produksi.

### 2. Jalankan giliran
1. Pahami niat player dan periksa lokasi, waktu, kemampuan, kondisi, sumber daya, serta pengetahuan karakter.
2. Resolusi aksi menggunakan modul resmi yang relevan. Satu aksi tidak otomatis berarti satu hit; ikuti Combat System untuk multi-hit dan combo.
3. Terapkan hanya konsekuensi yang didukung mekanik dan kejadian.
4. Perbarui state yang benar-benar berubah dan validasi kesinambungan waktu.
5. Kirim respons gameplay langsung dengan format canonical. Jangan tampilkan laporan bootstrap atau daftar file yang dibaca sebagai pengganti gameplay.

Jika sumber wajib gagal diakses, sebutkan file yang gagal dan jangan mengaku telah membacanya. Jangan menyelesaikan bagian aksi yang bergantung pada aturan yang tidak tersedia.

## Standar Istilah Kultivasi

- Untuk tingkat kultivasi bernomor 1–9, gunakan **Spirit Realm** secara konsisten. Jangan menyingkatnya menjadi `Realm` atau menyebutnya `Cultivation Realm`.
- Nama tingkat resmi adalah Spirit Initiate, Spirit Adept, Spirit Elder, Spirit Monarch, Spirit King, Spirit Ancestor, Spirit Emperor, Spirit Sovereign, dan Spirit Primordial.
- **Mortal** adalah status dasar sebelum sembilan Spirit Realm, bukan Spirit Realm 0.
- Jangan mengubah nama proper lain yang menggunakan kata *Realm* dengan makna berbeda, seperti Heaven Realm dalam sejarah.

## Sumber Utama dan Batas Tanggung Jawab

- `INDEX.md`: alur dan navigasi.
- `templates/AUTHORITY_ORDER.md`: Authority Order: perilaku GM, prosedur, anti-cheat, dan resolusi aksi tingkat umum.
- `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`: **satu-satunya sumber format visual lengkap setiap respons gameplay**.
- `templates/CHARACTER_PROFILE_TEMPLATE.md`: arti field dan aturan konsistensi state; bukan format output kedua.
- `templates/PLAYER_CONVERSATION_TEMPLATE.md`: prompt pemanggilan singkat; bukan sumber mekanik.
- `world/DYNAMIC_EVENTS.md`: registry canon event dunia persisten; wajib diperiksa setiap giliran gameplay.
- `templates/WORLD_EVENT_UPDATE_TEMPLATE.md`: format usulan perubahan event untuk ditinjau admin; bukan registry dan bukan bukti bahwa perubahan telah disimpan.
- `players.md`: indeks karakter terdaftar.
- `players/<Nama>.md`: snapshot awal karakter individual, bukan save berjalan.
- Modul mekanik: sumber resmi untuk aturan di ruang lingkupnya.
- Modul world: sumber resmi untuk lore, geografi/perjalanan, pemerintahan Golden Dragon Empire, bangsa berakal, faksi, sejarah, katalog artefak, distribusi kekayaan, stratifikasi sosial, serta event dinamis sesuai cakupannya. Untuk perjalanan atau interaksi dengan kelompok masyarakat, baca modul world yang relevan; jangan menganggap `MAP_AND_REGIONS.md` menggantikan aturan transportasi atau lore bangsa berakal.
- Event dinamis: setelah hasil aksi ditetapkan, cek apakah konsekuensinya persisten dan berdampak pada dunia bersama. Jika ya, siapkan proposal melalui `templates/WORLD_EVENT_UPDATE_TEMPLATE.md`. Proposal pemain/GM bukan canon dan tidak boleh dianggap tersimpan sebelum ditinjau, disetujui, dan di-commit oleh owner/admin. Perubahan karakter pribadi tidak dimasukkan ke registry event dunia.
- Profil gameplay terakhir dan kejadian setelahnya: sumber state sesi berjalan.

## Konsistensi yang Wajib Dipertahankan

- Jangan menambah field terpisah untuk Law atau Spirit Rings tanpa persetujuan pemilik. Rincian ring masuk ke Teknik / Kemampuan atau deskripsi Martial Soul.
- HP dan injury adalah dua state berbeda; gunakan modul masing-masing.
- `Satiety: nilai/100` adalah field profil resmi dan hanya dihitung menurut `core/HUNGER_AND_METABOLISM.md`. Waktu tidur malam yang dilindungi mengunci Satiety; pengecualian tidur malam terhadap batas aksi ditetapkan di `gameplay/TIME_AND_ACTION_RULES.md`.
- Sync progress/cap kompatibilitas berbeda dari penguasaan kekuatan ring 100%; ikuti Spirit Ring Rules.
- `Day left` adalah pengecualian hitung-mundur yang hanya berlaku untuk jeda minimum antarpenyerapan Spirit Ring yang berhasil; bukan timer umum breakthrough kultivasi. Ikuti `templates/CHARACTER_PROFILE_TEMPLATE.md` dan interval resmi `bestiary/SPIRIT_BEAST_RULES.md`. `0 Day left` hanya berarti jeda minimum sudah terpenuhi, bukan jaminan breakthrough atau penyerapan ring berhasil. Jika riwayat penyerapan/waktu tidak tersedia, tulis `Belum ditetapkan Day left`.
- Jangan mengubah HP, Qi, Spirit Realm, ring, inventory, equipment, assets, Currency, luka, atau relasi tanpa penyebab yang sah.
- GM wajib mempertahankan ledger uang dan item secara kronologis di riwayat percakapan: catat setiap perubahan ketika benar-benar terjadi, lanjutkan dari entri terakhir, cocokkan saldo Wallet serta jumlah/status item dengan profil, dan silang-rujuk transaksi uang dengan pergerakan item. Ikuti `core/10_ECONOMY_SYSTEM.md` dan `templates/AUTHORITY_ORDER.md`; ledger tidak menambah field profil atau modul terpisah dan tidak boleh diklaim tersimpan permanen di GitHub tanpa commit yang benar-benar diverifikasi. Jika riwayat ledger tidak tersedia, ungkapkan celahnya dan rekonsiliasi dari profil terakhir yang dapat diverifikasi—jangan mengarang sejarah.
- Penggunaan `???` sangat terbatas: hanya untuk karakter yang identitasnya benar-benar tidak dikenal dan nama Martial Soul yang belum diketahui. Jangan gunakan `???` untuk saldo, HP, Qi, Satiety, angka, atau field lain. Field numerik yang belum tercatat diisi `0`; field nonnumerik lain yang belum ditetapkan ditulis `Belum ditetapkan` atau `Tidak ada` sesuai makna. Jangan menciptakan rahasia, kemampuan, transaksi, atau kejadian masa lalu.
- Registry dan file karakter individual tidak boleh diubah selama gameplay tanpa permintaan eksplisit pemilik repository.
- **MODE: NO STEP** berarti tidak ada menu pilihan atau daftar opsi bernomor. Akhiri adegan pada situasi terbuka agar player menentukan tindakan sendiri.

## Daftar File Resmi

- `README.md`
- `INDEX.md`
- `players.md`
- `players/Yuha.md`
- `players/Nafila.md`
- `templates/AUTHORITY_ORDER.md`
- `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`
- `templates/CHARACTER_PROFILE_TEMPLATE.md`
- `templates/PLAYER_CONVERSATION_TEMPLATE.md`
- `core/CULTIVATION_SYSTEM.md`
- `core/CULTIVATOR_ACADEMIES.md`
- `core/MARTIAL_SOUL.md`
- `core/MARTIAL_SOUL_AWAKENING.md`
- `core/SPIRIT_RING_RULES.md`
- `core/HP_SYSTEM.md`
- `core/HUNGER_AND_METABOLISM.md`
- `core/INJURY_SYSTEM.md`
- `core/THINKER_AND_FORMULATION.md`
- `core/10_ECONOMY_SYSTEM.md`
- `bestiary/SPIRIT_BEAST_RULES.md`
- `gameplay/COMBAT_SYSTEM.md`
- `gameplay/TIME_AND_ACTION_RULES.md`
- `world/WORLD.md`
- `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md`
- `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`
- `world/MAP_AND_REGIONS.md`
- `world/GEOGRAPHY_AND_TRAVEL.md`
- `world/WANLUO_SACRED_EXPANSE.md`
- `world/INTELLIGENT_PEOPLES.md`
- `world/FACTIONS.md`
- `world/SPIRIT_HUNTERS_GUILD.md`
- `world/HISTORY.md`
- `world/DYNAMIC_EVENTS.md`
- `templates/WORLD_EVENT_UPDATE_TEMPLATE.md`
- `world/ARTIFACTS_AND_RELICS.md`
- `world/ARTIFICIAL_ARTIFACTS.md`
- `world/WEALTH_DISTRIBUTION.md`
- `world/SOCIAL_STRATIFICATION.md`

Modul yang disebut tetapi belum tersedia tidak otomatis menjadi sumber resmi. Jangan mengklaim membacanya atau menganggap isinya sudah ditetapkan.

## 3. Regional Modules and NPC References

The three canonical repository boundaries are **Golden Dragon Empire, Tianhai Yunzhou, and Beiming Gu**. The subregions listed below are geographic modules inside those powers—not separate repository boundaries. Canonical full NPC profiles have now been relocated into in-repository staging folders under `regions/<power>/npcs/`, with registries for all three powers; the old `world/NPC_*.md` paths are compatibility pointers. These folders are not separate GitHub repositories: destination repository creation/URLs remain unverified. Do not invent missing canon from scaffold headings. For NPC handling, use `world/NPC_MANAGEMENT.md`, the relevant regional module, the regional NPC registry, and `templates/NPC_PROFILE_TEMPLATE.md`.

### Golden Dragon Empire
- Golden Dragon Empire-wide civil and military governance — `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md`
- Named central ministers, seven regional governors, twelve active prefectural offices, and retained former prefects/county magistrates — `world/GOLDEN_DRAGON_EMPIRE_OFFICIALS.md`
- Population-facing services, bank and information-exchange offices, Medicine Hall Society locations, two central dormitory-based academies, and selected Ordo Suci Tianming public libraries — `world/GOLDEN_DRAGON_EMPIRE_POPULATION_SERVICES.md`
- Seven-region, twelve-prefecture, six-county-circuit register and thirteen named rural villages — `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`

**Canon lock — official villages vs. local settlements (Golden Dragon Empire):**
- The empire has exactly **13 officially registered named villages**. The canonical names and regional distribution must be taken from `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`; the seven `world/REGION_*.md` files must agree with that register.
- The atlas also lists **21 named hamlets/local settlements** for exploration and local route continuity. These are not official villages and must never be added to the official village count.
- When counting, use only entries explicitly classified as `Village` in the canonical atlas. Entries classified as `Hamlet` or another local-settlement status are separate categories, even if an older revision or regional table used the word “Village.”
- If a regional file, atlas heading/table, summary, or other document gives a conflicting number or classification, do not average, infer, or silently choose the larger list. Follow the canonical atlas and the owner’s recorded canon decisions; correct the inconsistent newer/secondary material and preserve useful extra locations under their correct local-settlement status.
- Before adding a settlement or editing a regional roster, cross-check the atlas and all seven regional village counts. Do not promote a hamlet to an official village unless the owner explicitly approves a canon change and the atlas plus every affected reference are updated together.

- Longyuan — `world/REGION_LONGYUAN.md`
- Canglan — `world/REGION_CANGLAN.md`
- Jinyue — `world/REGION_JINYUE.md`
- Tianfeng — `world/REGION_TIANFENG.md`
- Yanling — `world/REGION_YANLING.md`
- Baiyue — `world/REGION_BAIYUE.md`
- Xingluo — `world/REGION_XINGLUO.md`

### Tianhai Yunzhou
- Tianhai Yunzhou — `world/REGION_TIANHAI_YUNZHOU.md`
- Tianhai Spirit Hunters Guild offices, independent trade associations, and Medicine Hall Society service points — `world/REGION_TIANHAI_YUNZHOU.md` and `world/FACTIONS.md`
- Four cardinal areas, twelve clan placements, four Cultivator Academies, and the exclusive high-level Thinker Institute — `world/TIANHAI_ACADEMIES_AND_THINKER_INSTITUTE.md`
- Tianhai court, civil/military officials, district administrators, clan heads, dojo masters, Thinker institutions — `regions/tianhai-yunzhou/npcs/POWER_STRUCTURE.md`
- Maharaja Ji Haoyuan — `regions/tianhai-yunzhou/npcs/JI_HAOYUAN.md`
- Bai Xuanyin, revered Tianhai heroine — `regions/tianhai-yunzhou/npcs/BAI_XUANYIN.md`
- Ji Zhaoning, elder twin princess — `regions/tianhai-yunzhou/npcs/JI_ZHAONING.md`
- Ji Ningzhao, younger twin princess — `regions/tianhai-yunzhou/npcs/JI_NINGZHAO.md`

### Beiming Gu
- Beiming Heartland — `world/REGION_BEIMING_HEARTLAND.md`
- Frostveil Range — `world/REGION_FROSTVEIL_RANGE.md`
- Azureflame Basin — `world/REGION_AZUREFLAME_BASIN.md`
- Silverpine Wilds — `world/REGION_SILVERPINE_WILDS.md`
- Stonegate March — `world/REGION_STONEGATE_MARCH.md`
- Hollowmoon Valley — `world/REGION_HOLLOWMOON_VALLEY.md`
- Ironroot Reach — `world/REGION_IRONROOT_REACH.md`
- Beiming Gu NPC profiles — `regions/beiming-gu/npcs/BEIMING_HAN.md`, `regions/beiming-gu/npcs/BEIMING_XENHWA.md`, and `regions/beiming-gu/npcs/BEIMING_JINGHENG.md`

### Lawless Territories
- Ashen Borderlands — `world/REGION_ASHEN_BORDERLANDS.md`
- Black Tide Expanse — `world/REGION_BLACK_TIDE_EXPANSE.md`
- Nine Frost Wastes — `world/REGION_NINE_FROST_WASTES.md`

### NPC modules and templates
- NPC management rules — `world/NPC_MANAGEMENT.md`
- Regional module template — `templates/REGIONAL_MODULE_TEMPLATE.md`
- NPC profile template — `templates/NPC_PROFILE_TEMPLATE.md`

### Established Imperial Family NPC Profiles
- Emperor Jun Haotian — `regions/golden-dragon-empire/npcs/JUN_HAOTIAN.md`
- Empress Shen Yuehua — `regions/golden-dragon-empire/npcs/SHEN_YUEHUA.md`
- Crown Prince Jun Ruiyuan — `regions/golden-dragon-empire/npcs/JUN_RUIYUAN.md`
- Princess Jun Yuejin — `regions/golden-dragon-empire/npcs/JUN_YUEJIN.md`



### Regional structure, NPCs, and route network
- Golden Dragon Empire NPC staging INDEX and registry — `regions/golden-dragon-empire/INDEX.md` and `regions/golden-dragon-empire/npcs/REGISTRY.md`
- Tianhai Yunzhou NPC staging INDEX and registry — `regions/tianhai-yunzhou/INDEX.md` and `regions/tianhai-yunzhou/npcs/REGISTRY.md`
- Beiming Gu NPC staging INDEX and registry — `regions/beiming-gu/INDEX.md` and `regions/beiming-gu/npcs/REGISTRY.md`

- Location and route network rules — `world/LOCATION_AND_ROUTE_NETWORK.md`
- NPC agency, regional placement, and continuity — `world/NPC_MANAGEMENT.md`
- Regional module standard — `templates/REGIONAL_MODULE_TEMPLATE.md`
- Canonical full NPC profile standard — `templates/NPC_PROFILE_TEMPLATE.md`

**Required regional workflow:** when a scene involves a named region, load that region module first. Check the NPC table beside the relevant settlement, institution, or faction heading to establish local context; use the regional NPC registry for a broader roster audit, then consult the one canonical profile only for established recurring/major characters relevant to the scene. When travel is involved, verify the route through `world/LOCATION_AND_ROUTE_NETWORK.md`, the relevant regional modules, and `world/GEOGRAPHY_AND_TRAVEL.md`; resolve duration only through `gameplay/TIME_AND_ACTION_RULES.md`. Do not assume direct connections between all locations.

**Regional data format:** regional modules should keep the same conceptual order: identity → geography → settlements and local life → economy/resources → cultivation/Spirit Beasts/Thinkers → factions/authority → NPC registry → conflicts/events → route network and GM guidance. Existing canon may remain in its established subsection when moving it would risk loss, but new and revised regional content should follow this order and cross-reference rather than duplicate shared records.

**NPC placement:** follow the path: central INDEX → relevant regional/settlement module → NPC table grouped beside the matching location or faction → canonical full profile when needed. Ordinary residents and temporary scene characters may be portrayed situationally under `world/NPC_MANAGEMENT.md`. Recurring and major NPCs belong in the regional registry for discoverability and should link to one canonical full profile. Check official and faction rosters before creating an officeholder or faction member. Separate public knowledge, NPC knowledge, beliefs, and GM-only secrets.

**Route and economy realism:** routes must reflect confirmed geography and transport. Some settlements require an intermediate village, bridge, ferry, pass, port, or gate. Local resources, crafts, labor, demand, and services should create plausible trade relationships, but proposals remain non-canon until owner-approved.



### Mandatory Settlement Canon Load Path — Golden Dragon Empire

Whenever the GM/AI must narrate, count, compare, add, rename, classify, or edit a settlement in the Golden Dragon Empire, load and apply these sources in order before answering or changing files:

1. `INDEX.md` — enter through this routing rule.
2. `world/CANON_DECISIONS_AND_PRECEDENCE.md` — check binding owner decisions and conflict rules.
3. `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md` — authoritative register for the official village names, classifications, counts, and regional distribution.
4. The relevant `world/REGION_<NAME>.md` file for the location/scene. For a **total-count audit, cross-region comparison, or settlement-register edit**, read all seven Golden Dragon Empire regional modules and reconcile each roster against the atlas.
5. `world/MAP_AND_REGIONS.md` and `world/LOCATION_AND_ROUTE_NETWORK.md` when regional context, connections, or travel routes are relevant; read `world/GEOGRAPHY_AND_TRAVEL.md` for travel/transport rules.

**Binding settlement rules:** the Golden Dragon Empire has exactly **13 official named villages** and the atlas separately lists **21 named hamlets/local settlements**. Count only entries classified as official villages in the atlas. Hamlets and other local settlements do not increase the official-village total. Preserve extra settlement details for exploration, but never silently promote, delete, merge, rename, or reclassify a place as canon. Any proposed status change requires explicit owner approval and coordinated updates to the atlas, affected regional modules, and all dependent references.

If a required source cannot be fetched, state which source is unavailable and do not claim that the settlement audit or edit is fully verified. A summary, prior memory, heading, or older cached answer does not substitute for reading the current canonical files.

### Mandatory Territorial Canon Load Path — All Major Powers

This workflow applies to **all three major powers**—Golden Dragon Empire, Tianhai Yunzhou, and Beiming Gu—and to the Lawless Territories whenever they are involved. It applies to gameplay, lore questions, audits, and repository edits. Do not apply the Golden Dragon Empire's administrative counts or settlement classifications to Tianhai Yunzhou or Beiming.

Before narrating a location, describing its government/economy/customs, creating a settlement or NPC, counting local institutions, or changing regional files, follow this path:

1. Read `world/CANON_DECISIONS_AND_PRECEDENCE.md` for binding owner decisions and conflict precedence.
2. Read `world/MAP_AND_REGIONS.md` and `world/WORLD.md` for the established world layout and cross-power context.
3. Read the exact regional module for the location: one of the seven Empire modules, `world/REGION_TIANHAI_YUNZHOU.md`, the matching one of seven Beiming modules, or the relevant Lawless Territory module. The matching regional module is the primary source for local established facts and its own unfilled fields.
4. Follow the INDEX links for the relevant government, faction, institution, service, economy, or established NPC; read those specific sources rather than inferring details from a region's identity.
5. If travel or cross-region movement matters, read `world/LOCATION_AND_ROUTE_NETWORK.md`, the origin and destination regional modules, and `world/GEOGRAPHY_AND_TRAVEL.md`; resolve travel duration only through `gameplay/TIME_AND_ACTION_RULES.md`. A missing route is not proof of a direct connection or of impossibility.
6. For cross-region counts, audits, or edits to a shared register, inspect every affected regional roster and the canonical register governing that category. Do not extrapolate the Golden Dragon Empire's 13-village count to other powers; no count is established unless its authoritative source says so.
7. Reconcile the planned response or edit against the loaded canon. Preserve explicit owner decisions, do not let a newer secondary file silently override established canon, and distinguish confirmed facts from proposals, estimates, rumors, and unknown details.

**Beiming safeguard:** the Beiming regional files are owner-fillable scaffolds where their contents say details are pending. Treat only their confirmed foundations and cross-referenced official sources as established. Do not fill missing settlements, routes, local administration, prices, customs, or NPCs with invented facts and then present them as pre-existing canon. A GM may narrate situational details only within the authority rules and must not silently make them permanent canon.

**Tianhai safeguard:** use `world/REGION_TIANHAI_YUNZHOU.md` and its linked institutional/governance/NPC references for Tianhai-specific facts. Do not transfer the Golden Dragon Empire's bureaucratic tiers, academy count, village register, or local social rules to Tianhai Yunzhou without a source that explicitly establishes them.

If a required file cannot be fetched, name the missing source and limit the answer to what remains supported. A summary, prior memory, or region name is not a substitute for reading current canonical sources.

### Regional/NPC navigation triggers
| Situation | Required source |
|---|---|
| Character is in or traveling to one of the named regions | Fetch the matching `world/REGION_*.md` module, plus `world/MAP_AND_REGIONS.md` / `world/GEOGRAPHY_AND_TRAVEL.md` as needed |
| Character enters a settlement listed in a regional module | Read that region's settlement and NPC registry; do not assume undocumented shops, residents, or authorities exist |
| Character meets an established recurring or major NPC | Read the NPC profile linked from the regional registry and preserve prior continuity |
| Character meets a new minor NPC | Follow `world/NPC_MANAGEMENT.md` and `templates/AUTHORITY_ORDER.md`; do not invent major secrets or present improvised details as permanent canon |
| Faction presence, membership, or authority matters | Read `world/FACTIONS.md` and the matching regional module; regional association alone does not prove current control |
| A character in Tianhai Yunzhou seeks a Guild contract, trade association, healer, or medical service | Read `world/REGION_TIANHAI_YUNZHOU.md`, `world/FACTIONS.md`, and `world/SPIRIT_HUNTERS_GUILD.md` for Guild work; read `world/WORLD.md` for cross-world Medicine Hall Society canon. Check `core/10_ECONOMY_SYSTEM.md` before stating prices or fees |
| Martial Soul Awakening or the Grand Martial Soul Awakening Hall is mentioned in any major power | Read `world/CANON_DECISIONS_AND_PRECEDENCE.md`, `core/MARTIAL_SOUL.md`, `core/MARTIAL_SOUL_AWAKENING.md`, and the relevant power's regional/governance modules. There is exactly one Hall at the principal civilizational center of each major power; do not invent secondary branches or apply Empire-specific fees/subsidies to Tianhai Yunzhou or Beiming |
| A character seeks a first or later Spirit Ring through an academy expedition, a Guild party, or a solo hunt | Read `core/SPIRIT_RING_RULES.md`, `core/CULTIVATION_SYSTEM.md`, and `bestiary/SPIRIT_BEAST_RULES.md`; then load the route-specific source (`core/CULTIVATOR_ACADEMIES.md` for an academy Safe Route or `world/SPIRIT_HUNTERS_GUILD.md` for a Guild party) and relevant combat, HP, injury, time, and metabolism modules. Resolve tracking, combat, ring ownership, and absorption as separate steps. |
| A character seeks any Guild contract, joins a temporary Guild team, accepts escort/cargo/item-search work, seeks a Spirit Beast hunting party, or encounters a Guild bounty notice | Read `world/SPIRIT_HUNTERS_GUILD.md`; also read `core/SPIRIT_RING_RULES.md`, `bestiary/SPIRIT_BEAST_RULES.md`, and relevant combat/HP/injury modules when the contract involves Spirit Beasts or combat |
| Government office, imperial ministry, or civil-versus-military authority matters in the Golden Dragon Empire | Read `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md`, then the matching regional module and any linked NPC profile |
| A character visits or discusses a Golden Dragon Empire prefecture, county, city, or other administrative unit | Read `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md` and the matching `world/REGION_*.md` module; use the atlas as the single source for jurisdiction names and counts |
| A scene, edit, or question involves Golden Dragon Empire villages, hamlets, rural settlement counts, or a regional settlement roster | Follow the mandatory **Settlement Canon Load Path** below; do not rely on INDEX summaries alone |
| A character seeks banking, information brokerage, medical services, foundational education, or a public knowledge library in the Golden Dragon Empire | Read `world/GOLDEN_DRAGON_EMPIRE_POPULATION_SERVICES.md` plus the matching regional module; use its named branch register and access limits |
| NPC action changes the persistent world | Check `world/DYNAMIC_EVENTS.md` and the approved owner workflow; do not claim persistence without a verified repository update |

**Canon boundary:** The regional modules preserve the region identities, named settlements, and faction associations already present in official world files. They intentionally leave detailed geography, routes, settlement-level population and demographics, customs, prices, named NPCs, hidden lore, and current faction control unfilled for the owner to define. Golden Dragon Empire-wide administrative names and planning totals are governed by `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`. Do not infer those details from a module's existence.
