# Merzkava Universe — Official Index

INDEX ini adalah **pintu masuk tunggal** untuk memulai, melanjutkan, dan menjalankan roleplay Merzkava Universe. Ikuti prosedur bootstrap dan navigasi modul di bawah. Jangan menggandakan aturan mekanik atau format respons lengkap ke file lain.

Repository resmi: https://github.com/Antarezka/merzkava-universe

## 0. Prosedur Bootstrap (WAJIB)

Saat pemain memakai trigger awal yang merujuk INDEX.md dan players.md, perlakukan pesan itu sebagai perintah untuk menginisialisasi gameplay — bukan permintaan untuk sekadar menganalisis atau merangkum tautan.

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
| Nama dan jumlah regional, prefektur, county, kota, kota kecil, distrik, serta desa Kekaisaran Naga Emas | `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md` |
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

Regional modules are divided according to the established geography in `world/MAP_AND_REGIONS.md`. They are **owner-fillable scaffolds**, not a license for the GM to invent missing canon. Fetch the module matching the character's current location or intended destination; fetch `world/NPC_MANAGEMENT.md` when creating, meeting, or continuing an important NPC. Use `templates/NPC_PROFILE_TEMPLATE.md` for a full NPC profile and link it from the regional registry.

### Golden Dragon Empire
- Empire-wide civil and military governance — `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md`
- Named central ministers, regional governors, all prefects and county magistrates — `world/GOLDEN_DRAGON_EMPIRE_OFFICIALS.md`
- Population-facing services, bank and information-exchange offices, Medicine Hall Society locations, two central dormitory-based academies, and selected Ordo Suci Tianming public libraries — `world/GOLDEN_DRAGON_EMPIRE_POPULATION_SERVICES.md`
- Prefecture/county register, broad territorial-area estimates, centralization gradient, and four named rural villages per region — `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`
- Longyuan — `world/REGION_LONGYUAN.md`
- Canglan — `world/REGION_CANGLAN.md`
- Jinyue — `world/REGION_JINYUE.md`
- Tianfeng — `world/REGION_TIANFENG.md`
- Yanling — `world/REGION_YANLING.md`
- Baiyue — `world/REGION_BAIYUE.md`
- Xingluo — `world/REGION_XINGLUO.md`

### Tianhai Yunzhou
- Tianhai Yunzhou — `world/REGION_TIANHAI_YUNZHOU.md`

### Beiming Gu
- Beiming Heartland — `world/REGION_BEIMING_HEARTLAND.md`
- Frostveil Range — `world/REGION_FROSTVEIL_RANGE.md`
- Azureflame Basin — `world/REGION_AZUREFLAME_BASIN.md`
- Silverpine Wilds — `world/REGION_SILVERPINE_WILDS.md`
- Stonegate March — `world/REGION_STONEGATE_MARCH.md`
- Hollowmoon Valley — `world/REGION_HOLLOWMOON_VALLEY.md`
- Ironroot Reach — `world/REGION_IRONROOT_REACH.md`

### Lawless Territories
- Ashen Borderlands — `world/REGION_ASHEN_BORDERLANDS.md`
- Black Tide Expanse — `world/REGION_BLACK_TIDE_EXPANSE.md`
- Nine Frost Wastes — `world/REGION_NINE_FROST_WASTES.md`

### NPC modules and templates
- NPC management rules — `world/NPC_MANAGEMENT.md`
- Regional module template — `templates/REGIONAL_MODULE_TEMPLATE.md`
- NPC profile template — `templates/NPC_PROFILE_TEMPLATE.md`

### Established Imperial Family NPC Profiles
- Emperor Jun Haotian — `world/NPC_JUN_HAOTIAN.md`
- Empress Shen Yuehua — `world/NPC_SHEN_YUEHUA.md`
- Crown Prince Jun Ruiyuan — `world/NPC_JUN_RUIYUAN.md`
- Princess Jun Yuejin — `world/NPC_JUN_YUEJIN.md`

### Regional/NPC navigation triggers
| Situation | Required source |
|---|---|
| Character is in or traveling to one of the named regions | Fetch the matching `world/REGION_*.md` module, plus `world/MAP_AND_REGIONS.md` / `world/GEOGRAPHY_AND_TRAVEL.md` as needed |
| Character enters a settlement listed in a regional module | Read that region's settlement and NPC registry; do not assume undocumented shops, residents, or authorities exist |
| Character meets an established recurring or major NPC | Read the NPC profile linked from the regional registry and preserve prior continuity |
| Character meets a new minor NPC | Follow `world/NPC_MANAGEMENT.md` and `templates/AUTHORITY_ORDER.md`; do not invent major secrets or present improvised details as permanent canon |
| Faction presence, membership, or authority matters | Read `world/FACTIONS.md` and the matching regional module; regional association alone does not prove current control |
| A character seeks a first or later Spirit Ring through an academy expedition, a Guild party, or a solo hunt | Read `core/SPIRIT_RING_RULES.md`, `core/CULTIVATION_SYSTEM.md`, and `bestiary/SPIRIT_BEAST_RULES.md`; then load the route-specific source (`core/CULTIVATOR_ACADEMIES.md` for an academy Safe Route or `world/SPIRIT_HUNTERS_GUILD.md` for a Guild party) and relevant combat, HP, injury, time, and metabolism modules. Resolve tracking, combat, ring ownership, and absorption as separate steps. |
| A character seeks any Guild contract, joins a temporary Guild team, accepts escort/cargo/item-search work, seeks a Spirit Beast hunting party, or encounters a Guild bounty notice | Read `world/SPIRIT_HUNTERS_GUILD.md`; also read `core/SPIRIT_RING_RULES.md`, `bestiary/SPIRIT_BEAST_RULES.md`, and relevant combat/HP/injury modules when the contract involves Spirit Beasts or combat |
| Government office, imperial ministry, or civil-versus-military authority matters in the Golden Dragon Empire | Read `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md`, then the matching regional module and any linked NPC profile |
| A character visits or discusses a Golden Dragon Empire prefecture, county, city, or other administrative unit | Read `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md` and the matching `world/REGION_*.md` module; use the atlas as the single source for jurisdiction names and counts |
| A character seeks banking, information brokerage, medical services, foundational education, or a public knowledge library in the Golden Dragon Empire | Read `world/GOLDEN_DRAGON_EMPIRE_POPULATION_SERVICES.md` plus the matching regional module; use its named branch register and access limits |
| NPC action changes the persistent world | Check `world/DYNAMIC_EVENTS.md` and the approved owner workflow; do not claim persistence without a verified repository update |

**Canon boundary:** The regional modules preserve the region identities, named settlements, and faction associations already present in official world files. They intentionally leave detailed geography, routes, settlement-level population and demographics, customs, prices, named NPCs, hidden lore, and current faction control unfilled for the owner to define. Empire-wide administrative names and planning totals are governed by `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`. Do not infer those details from a module's existence.
