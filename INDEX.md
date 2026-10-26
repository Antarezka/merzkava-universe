# Merzkava Universe — Official Index

INDEX ini adalah **pintu masuk tunggal** untuk memulai, melanjutkan, dan menjalankan roleplay Merzkava Universe. Ikuti prosedur bootstrap dan navigasi modul di bawah. Jangan menggandakan aturan mekanik atau format respons lengkap ke file lain.

Repository resmi: https://github.com/Antarezka/merzkava-universe

## Struktur Wilayah di Dalam Repo — WAJIB

**Seluruh dunia Merzkava Universe dikelola di satu repositori resmi ini:** `Antarezka/merzkava-universe`. Nama Golden Dragon Empire, Tianhai Yunzhou, dan Beiming Gu adalah **tiga kekuasaan besar di dalam dunia**, bukan instruksi untuk membuat tiga repositori GitHub terpisah.

**Jangan membuat, meminta, atau mengarahkan migrasi ke repositori regional eksternal.** Struktur kanonis berada di dalam repo yang sama:
- `world/` — canon global, peta, geografi, sejarah, jalur lintas wilayah, pemerintahan, faksi, dan modul dunia sesuai cakupannya.
- `regions/golden-dragon-empire/` — indeks regional dan data khusus Golden Dragon Empire.
- `regions/tianhai-yunzhou/` — indeks regional dan data khusus Tianhai Yunzhou.
- `regions/beiming-gu/` — indeks regional dan data khusus Beiming Gu.
- `regions/<power>/npcs/` — registry serta profil NPC kanonis yang dimiliki/berafiliasi dengan kekuasaan terkait.

Subwilayah, provinsi, kawasan, kota, desa, akademi, institusi, dan faksi tetap menjadi **folder atau modul di dalam repo ini**, bukan repositori terpisah. Jangan membuat repo NPC global keempat. Jangan memindahkan modul canon global ke folder regional hanya karena modul itu menyebut suatu wilayah; tempatkan data menurut cakupan dan otoritas canon-nya.

Nama kekuasaan harus mengikuti `world/WORLD.md` secara persis: **Golden Dragon Empire**, **Tianhai Yunzhou**, dan **Beiming Gu**. Navigasi wajib mengikuti pola: INDEX pusat → indeks/modul kekuasaan di repo yang sama → modul lokasi/permukiman dan registry NPC → profil NPC relevan.

**Status implementasi:** folder regional dan profil NPC berada di repo ini, bukan di repositori eksternal. Beiming Gu memiliki 21 profil kanonis yang dicatat di `regions/beiming-gu/npcs/REGISTRY.md`: Beiming Han, Beiming Xenhwa, Beiming Jingheng, Beiming Nerva, 12 kepala klan, dan 5 master dojo. Beiming Nerva adalah Thinker Grade 9 kedua yang tercatat. Sebelum mengubah atau menghapus path lama `world/NPC_*.md`, periksa isi aktualnya dan sinkronkan seluruh referensi yang terdampak. Tidak ada migrasi lintas-repo yang diwajibkan; pekerjaan struktur harus dilakukan di repo `merzkava-universe` yang sudah ada.

## 0. Prosedur Bootstrap (WAJIB)

Saat pemain memakai trigger awal yang merujuk INDEX.md dan players.md, perlakukan pesan itu sebagai perintah untuk menginisialisasi gameplay — bukan permintaan untuk sekadar menganalisis atau merangkum tautan.

**Aturan canon final:** jika ada keputusan owner yang sudah ditetapkan atau konflik antara file, baca `world/CANON_DECISIONS_AND_PRECEDENCE.md` bersama sumber khusus topik. File yang baru ditambahkan tidak otomatis mengalahkan keputusan final yang lebih lama; selaraskan informasi baru dengan canon yang berlaku kecuali owner secara eksplisit merevisinya.

1. **Baca seluruh INDEX.md dan `templates/AUTHORITY_ORDER.md` terlebih dahulu.** INDEX adalah peta navigasi; Authority Order menetapkan perilaku GM dan aturan pelaksanaan.
2. **Pilih mode sesi.** Sesi berlanjut memakai profil gameplay terakhir dan kejadian setelahnya, bukan snapshot awal. Sesi baru memakai snapshot karakter terdaftar setelah template canonical dimuat. Karakter baru mengikuti template dan Authority Order tanpa mengarang rahasia inti atau kemampuan formal.
3. **Ikuti urutan bootstrap terperinci pada bagian “Gerbang format → profil player → ekonomi” di bawah.** Bagian itu adalah sumber langkah operasional lengkap untuk template, profil, Wallet, modul relevan, event, dan validasi.
4. **Gunakan navigasi dinamis selama gameplay.** Periksa `world/DYNAMIC_EVENTS.md` sebelum adegan pertama dan setiap giliran; baca hanya modul yang relevan dengan karakter, lokasi, waktu, dan aksi. Jika sumber wajib gagal diakses, sebutkan sumbernya dan jangan berpura-pura gate selesai. Mulai gameplay langsung tanpa laporan bootstrap.
5. **Perubahan state dan ledger:** ikuti `templates/AUTHORITY_ORDER.md` untuk laporan perubahan, penanda `Log tercatat!`, serta validasi; ikuti `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` untuk urutan dan bentuk visual. `core/10_ECONOMY_SYSTEM.md` mengatur ledger uang/item dan format log gabungan; `core/HUNGER_AND_METABOLISM.md` adalah satu-satunya sumber rumus Satiety. Setiap aktivitas terbaru wajib menyebut nilai Satiety. Penanda berarti ledger sesi telah dicatat, bukan klaim bahwa data ditulis ke GitHub.

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

**Hard gate bagan profil — validasi bentuk, bukan sekadar isi:** sebelum mengirim setiap respons gameplay, cocokkan hasil akhir langsung dengan `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` dari judul `PROFIL KARAKTER` sampai `TEKNIK & TUJUAN`. Salin kerangka visual canonical, bukan membuat ulang dengan kotak ASCII, tabel, daftar ringkas, atau format alternatif. Pertahankan persis urutan seksi, judul seksi, garis pemisah, nama field, urutan field, format satu baris Wallet, dan penutup. Profil harus berupa empat blok visual yang terpisah: (1) `PROFIL KARAKTER`, (2) `INV & KEUANGAN`, (3) `TEKNIK & TUJUAN`, dan (4) `CATATAN PEMAIN & KONSISTENSI`; jangan melebur isi antarblok atau memindahkan Inventory/Assets/Wallet ke blok lain. Field inti dalam urutan canonical: Nama, Usia, Spirit Realm, Sync progress, Spirit Ring Absorption, Martial Soul, Thinker Grade, HP, Satiety, Qi, Kondisi Tubuh, Equipment. Lanjutkan dengan Inventory, Assets Bangunan, Wallet (wealth) dalam format lima denominasi; kemudian Teknik / Kemampuan dan Tujuan Saat Ini. Jangan menambahkan field seperti Breakthrough, Law, atau Spirit Rings, dan jangan menghilangkan field hanya karena nilainya belum diketahui. Ganti placeholder dengan nilai yang sesuai aturan field; jangan menyalin instruksi placeholder ke output. Setelah selesai, lakukan perbandingan visual baris demi baris terhadap template canonical. Jika susunan/ornamen/field berbeda, perbaiki sebelum mengirim. Template canonical tetap satu-satunya sumber lengkap untuk karakter visual; paragraf ini adalah pemeriksaan kepatuhan, bukan format pengganti.

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
| Encounter perjalanan, ambush terpisah, dan pertolongan darurat tabib pengembara Medicine Hall Society | `gameplay/TRAVEL_ENCOUNTER_AMBUSH_RESCUE.md` |
| Spirit Realm, Stage, Sync, bottleneck, breakthrough | `core/CULTIVATION_SYSTEM.md` |
| Akademi kultivator dan pendidikan dasar | `core/CULTIVATOR_ACADEMIES.md` |
| Keputusan canon final, prioritas sumber, dan aturan sinkronisasi file lama/baru | `world/CANON_DECISIONS_AND_PRECEDENCE.md` |
| Prosedur awakening, chance rarity, formulasi penilaian Martial Soul, undian dan keputusan mutasi | `core/MARTIAL_SOUL_AWAKENING.md` |
| Lore, bentuk, karakteristik, dan interpretasi Martial Soul | `core/MARTIAL_SOUL.md` |
| Spirit Ring, kompatibilitas, penyerapan, kombinasi kemampuan, Qi, PowerScale, jalur perolehan ring | `core/SPIRIT_RING_RULES.md` |
| Spirit Beast, syarat ring, jeda minimum, deviasi | `bestiary/SPIRIT_BEAST_RULES.md` |
| Penilaian tier universal dan Kantor Appraisal dunia | `core/TIER_ASSESSMENT_AND_APPRAISAL.md` |
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
| Ruined Archiver: cabang Ordo untuk registrasi ekspedisi Ruined, verifikasi peta, kompensasi, kerahasiaan, dan deteksi dini anomali | `world/RUINED_ARCHIVER.md` |
| Lore, hierarki, Martial Soul, filosofi, dan batas pengetahuan dua klan/sekte tersembunyi di puncak lautan awan | `world/ANCIENT_SHAMANISM_AND_BUDDHIST_CLANS.md` |
| Bangsa berakal, ciri kelompok, dan konteks perlakuan sosial | `world/INTELLIGENT_PEOPLES.md` |
| Klan, dojo, sekte, organisasi, Medicine Hall Society, Ordo Suci Tianming | `world/FACTIONS.md` |
| Ancient Shamanism dan klan Buddhis tersembunyi | `world/ANCIENT_SHAMANISM_AND_BUDDHIST_CLANS.md` |
| Serikat Guild: kontrak lintas jenis pekerjaan, enam tingkat kesulitan, party sementara, perburuan Spirit Beast, blacklist, dan kontrak buruan Deadpool | `world/SPIRIT_HUNTERS_GUILD.md` |
| Geografi dan lore kawasan suci Wanluo, World Knowledge Tower, distrik, jalur ziarah, serta kompleks Ordo Suci Tianming | `world/WANLUO_SACRED_EXPANSE.md` |
| Kronologi, bukti sejarah, bencana dunia masa lampau, dan peristiwa historis yang sudah mapan | `world/HISTORY.md` |
| Registry event dunia persisten dan event berulang canon, termasuk Festival Tiga Kekuasaan setiap enam bulan, status, dampak lintas sesi, dan sumber konfirmasi | `world/DYNAMIC_EVENTS.md` |
| Form proposal untuk menambah/memperbarui event dunia; bukan canon sampai disetujui admin | `templates/WORLD_EVENT_UPDATE_TEMPLATE.md` |
| Kategori Relic/Ancient Artifact dan katalog | `world/ARTIFACTS_AND_RELICS.md` |
| Katalog dan lore Artificial Artifact | `world/ARTIFICIAL_ARTIFACTS.md` |
| Satiety, kategori aktivitas dan pengali, jadwal/jendela makan terlewat, metabolisme Spirit Realm, tidur malam, konsumsi makanan, dan pengubah kondisi tubuh | `core/HUNGER_AND_METABOLISM.md` |

Untuk aksi yang menyentuh beberapa sistem, baca semua modul yang relevan. Contoh: combat yang mengubah HP dan menimbulkan luka memerlukan Combat, HP, Injury, Time, dan Hunger/Metabolism bila waktu aktif berlalu. Produksi Artificial Artifact menggunakan mekanik di `core/THINKER_AND_FORMULATION.md`; file lore artefak tidak menggantikan aturan produksi.

### 2. Jalankan giliran
1. Pahami niat player dan periksa lokasi, waktu, kemampuan, kondisi, sumber daya, serta pengetahuan karakter.
2. Resolusi aksi menggunakan modul resmi yang relevan. Satu aksi tidak otomatis berarti satu hit; ikuti Combat System untuk multi-hit dan combo.
3. Terapkan hanya konsekuensi yang didukung mekanik dan kejadian.
4. Perbarui state yang benar-benar berubah dan validasi kesinambungan waktu.
5. Kirim respons gameplay langsung dengan format canonical. Jangan tampilkan laporan bootstrap atau daftar file yang dibaca sebagai pengganti gameplay.

Jika sumber wajib gagal diakses, sebutkan file yang gagal dan jangan mengaku telah membacanya. Jangan menyelesaikan bagian aksi yang bergantung pada aturan yang tidak tersedia.

## Rujukan Status Spirit Ring Absorption

Pemetaan tunggal status dan format `status | Day left` berada di `templates/CHARACTER_PROFILE_TEMPLATE.md`. Rumus serta akumulasi waktu `Day left` hanya mengikuti `gameplay/TIME_AND_ACTION_RULES.md` §7; interval minimum mengikuti `bestiary/SPIRIT_BEAST_RULES.md`. Sebelum setiap percobaan penyerapan, verifikasi semua syarat resmi dan terapkan hard gate di `core/SPIRIT_RING_RULES.md`. Jangan menyalin atau membuat pemetaan status alternatif di indeks ini.

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
- `core/TIER_ASSESSMENT_AND_APPRAISAL.md`: metode fallback Tier 1–9 untuk barang/artefak/Beast serta otoritas Kantor Appraisal (MAA). Martial Soul tidak memakai Tier 1–9 generik: undian rarity dan penilaian kualitas inherennya mengikuti formulasi khusus `core/MARTIAL_SOUL_AWAKENING.md`; appraisal kualitas inheren tidak menimpa rarity hasil undian yang sah.
- Modul mekanik: sumber resmi untuk aturan di ruang lingkupnya.
- Modul world: sumber resmi untuk lore, geografi/perjalanan, pemerintahan Golden Dragon Empire, bangsa berakal, faksi, sejarah, katalog artefak, distribusi kekayaan, stratifikasi sosial, serta event dinamis sesuai cakupannya. Untuk perjalanan atau interaksi dengan kelompok masyarakat, baca modul world yang relevan; jangan menganggap `MAP_AND_REGIONS.md` menggantikan aturan transportasi atau lore bangsa berakal.
- Event dinamis: setelah hasil aksi ditetapkan, cek apakah konsekuensinya persisten dan berdampak pada dunia bersama. Jika ya, siapkan proposal melalui `templates/WORLD_EVENT_UPDATE_TEMPLATE.md`. Proposal pemain/GM bukan canon dan tidak boleh dianggap tersimpan sebelum ditinjau, disetujui, dan di-commit oleh owner/admin. Perubahan karakter pribadi tidak dimasukkan ke registry event dunia.
- Profil gameplay terakhir dan kejadian setelahnya: sumber state sesi berjalan.

## Konsistensi yang Wajib Dipertahankan

- Jangan menambah field terpisah untuk Law atau Spirit Rings tanpa persetujuan pemilik. Rincian ring masuk ke Teknik / Kemampuan atau deskripsi Martial Soul.
- HP dan injury adalah dua state berbeda; gunakan modul masing-masing.
- `Satiety: nilai/100` adalah field profil resmi dan hanya dihitung menurut `core/HUNGER_AND_METABOLISM.md`. Setiap aktivitas terbaru wajib menyebut Satiety, dengan nilai sebelum → perubahan → sesudah bila berubah, atau nilai tetap dan alasannya bila tidak berubah. Istirahat tidak menambah Satiety; hanya memperlambat pengurangan. Konsumsi harus menyebut nama item, tier resmi, jumlah, dan efek aktual; jika tier belum tercatat secara resmi, ikuti `core/TIER_ASSESSMENT_AND_APPRAISAL.md`: gunakan hasil appraisal resmi bila tersedia; jika belum, gunakan prediksi GM berskor hanya bila bukti cukup dan beri label prediksi; jika bukti tidak cukup, tulis “Tier belum ditetapkan — appraisal diperlukan”. Jika snapshot lama dibuat sebelum field Satiety ditambahkan, tetapkan estimasi awal GM yang wajar saat bootstrap sesi baru; jangan otomatis menetapkan 0 atau 100 dan jangan mengubah snapshot hanya untuk mengisi state sesi. Waktu tidur malam yang dilindungi mengunci Satiety; pengecualian tidur malam terhadap batas aksi ditetapkan di `gameplay/TIME_AND_ACTION_RULES.md`.
- Sync progress/cap kompatibilitas berbeda dari penguasaan kekuatan ring 100%; ikuti Spirit Ring Rules.
- Status dan format field `Spirit Ring Absorption` mengikuti `templates/CHARACTER_PROFILE_TEMPLATE.md`; rumus `Day left` mengikuti `gameplay/TIME_AND_ACTION_RULES.md` §7; interval minimum mengikuti `bestiary/SPIRIT_BEAST_RULES.md`. Terapkan hard gate dari `core/SPIRIT_RING_RULES.md` sebelum percobaan penyerapan.
- Jangan mengubah HP, Qi, Spirit Realm, ring, inventory, equipment, assets, Currency, luka, atau relasi tanpa penyebab yang sah.
- GM wajib mempertahankan ledger Satiety, uang, dan item secara kronologis di riwayat percakapan: catat setiap perubahan ketika benar-benar terjadi, lanjutkan dari entri terakhir, cocokkan Satiety/Wallet/jumlah/status item dengan profil, dan silang-rujuk perubahan yang berasal dari tindakan yang sama. Ikuti `core/HUNGER_AND_METABOLISM.md`, `core/10_ECONOMY_SYSTEM.md`, dan `templates/AUTHORITY_ORDER.md`; gunakan satu laporan perubahan dan satu LEDGER LOG untuk semua field yang terdampak oleh satu tindakan. Ledger tidak menambah field profil atau modul terpisah dan tidak boleh diklaim tersimpan permanen di GitHub tanpa commit yang benar-benar diverifikasi. Jika riwayat ledger tidak tersedia, ungkapkan celahnya dan rekonsiliasi dari profil terakhir yang dapat diverifikasi—jangan mengarang sejarah.
- Penggunaan `???` sangat terbatas: identitas karakter yang benar-benar tidak dikenal, nama Martial Soul yang belum diketahui, dan `Day left` sebelum penyerapan Spirit Ring pertama yang berhasil. Semua status serta format `status | Day left` mengikuti `templates/CHARACTER_PROFILE_TEMPLATE.md`. Jangan gunakan `???` untuk saldo, HP, Qi, Satiety, atau field lain. Field numerik lain yang belum tercatat diisi `0`; field nonnumerik lain yang belum ditetapkan ditulis `Belum ditetapkan` atau `Tidak ada` sesuai makna. `Belum ditetapkan Day left` hanya untuk state lama yang diketahui pernah menyerap ring tetapi riwayatnya tidak cukup untuk menghitung cooldown. Jangan menciptakan rahasia, kemampuan, transaksi, atau kejadian masa lalu.
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
- `gameplay/TRAVEL_ENCOUNTER_AMBUSH_RESCUE.md`
- `world/WORLD.md`
- `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md`
- `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`
- `world/MAP_AND_REGIONS.md`
- `world/LAWLESS_TERRITORIES.md`
- `world/GEOGRAPHY_AND_TRAVEL.md`
- `world/WANLUO_SACRED_EXPANSE.md`
- `world/INTELLIGENT_PEOPLES.md`
- `world/FACTIONS.md`
- `world/SPIRIT_HUNTERS_GUILD.md`
- `world/HISTORY.md`
- `world/RUINED_ARCHIVER.md`
- `world/DYNAMIC_EVENTS.md`
- `templates/WORLD_EVENT_UPDATE_TEMPLATE.md`
- `world/ARTIFACTS_AND_RELICS.md`
- `world/ARTIFICIAL_ARTIFACTS.md`
- `world/WEALTH_DISTRIBUTION.md`
- `world/SOCIAL_STRATIFICATION.md`

Modul yang disebut tetapi belum tersedia tidak otomatis menjadi sumber resmi. Jangan mengklaim membacanya atau menganggap isinya sudah ditetapkan.

## 3. Regional Modules and NPC References

The three major powers are **Golden Dragon Empire, Tianhai Yunzhou, and Beiming Gu**. They are represented by regional folders/modules inside this one repository, not separate GitHub repositories. Canonical full NPC profiles and registries are maintained under `regions/<power>/npcs/`; the regional INDEX and registry guide NPC lookup, while the relevant `world/REGION_*.md` module remains the source for established regional/location context unless another canonical source is explicitly linked. Legacy `world/NPC_*.md` files must be inspected individually: treat each as a legacy source until its actual contents confirm that it is a compatibility pointer. Do not invent missing canon from scaffold headings. For NPC handling, use `world/NPC_MANAGEMENT.md`, the relevant regional module, the regional NPC registry, and `templates/NPC_PROFILE_TEMPLATE.md`.

### Golden Dragon Empire
- civil and military governance across the Golden Dragon Empire — `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md`
- Named central ministers, seven regional governors, twelve active prefectural offices, and retained former prefects/county magistrates — `world/GOLDEN_DRAGON_EMPIRE_OFFICIALS.md`
- Population-facing services, bank and information-exchange offices, Medicine Hall Society locations, two central dormitory-based academies, and selected Ordo Suci Tianming public libraries — `world/GOLDEN_DRAGON_EMPIRE_POPULATION_SERVICES.md`
- Seven-region, twelve-prefecture, six-county-circuit register and thirteen named rural villages — `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`

**Canon lock — official villages vs. local settlements (Golden Dragon Empire):**
- The Golden Dragon Empire has exactly **13 officially registered named villages**. The canonical names and regional distribution must be taken from `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`; the seven `world/REGION_*.md` files must agree with that register.
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
- Tianhai Yunzhou Spirit Hunters Guild offices, independent trade associations, and Medicine Hall Society service points — `world/REGION_TIANHAI_YUNZHOU.md` and `world/FACTIONS.md`
- Four cardinal areas, twelve clan placements, four Cultivator Academies, and the exclusive high-level Thinker Institute — `world/TIANHAI_ACADEMIES_AND_THINKER_INSTITUTE.md`
- Tianhai Yunzhou court, civil/military officials, district administrators, clan heads, dojo masters, Thinker institutions — `regions/tianhai-yunzhou/npcs/POWER_STRUCTURE.md`
- Maharaja Ji Haoyuan — `regions/tianhai-yunzhou/npcs/JI_HAOYUAN.md`
- Bai Xuanyin, revered Tianhai Yunzhou heroine — `regions/tianhai-yunzhou/npcs/BAI_XUANYIN.md`
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
- Beiming Gu NPC registry and full roster — `regions/beiming-gu/npcs/REGISTRY.md`; established profiles: `regions/beiming-gu/npcs/BEIMING_HAN.md`, `regions/beiming-gu/npcs/BEIMING_XENHWA.md`, `regions/beiming-gu/npcs/BEIMING_JINGHENG.md`, `regions/beiming-gu/npcs/BEIMING_NERVA.md`; clan/dojo roster profiles are linked from the registry.

### Lawless Territories
- Ashen Borderlands — `world/REGION_ASHEN_BORDERLANDS.md`
- Black Tide Expanse — `world/REGION_BLACK_TIDE_EXPANSE.md`
- Nine Frost Wastes — `world/REGION_NINE_FROST_WASTES.md`
- **Lawless Territories master reference** (underground economy, organizations' service roles, neutral refuge, Azerion Forest, Dead Zone as the deepest core only, central lake and Mega Colossal Labyrinth, unexplored-ruin map/hidden-treasure rules, hidden Inner Azerion city and half-beast economy, illusion fog, human access risks, slave market, food scarcity, elite auctions) — `world/LAWLESS_TERRITORIES.md`

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

**Required regional workflow:** when a scene involves a named region, first perform the applicable global canon/precedence checks in the `Mandatory Territorial Canon Load Path — All Major Powers` below, then load the exact regional module from `world/REGION_*.md` for local context. Check the NPC table beside the relevant settlement, institution, or faction heading; use the regional NPC registry for broader roster audits, then consult only the canonical profile of an established recurring/major NPC relevant to the scene. When travel is involved, verify the route through `world/LOCATION_AND_ROUTE_NETWORK.md`, the relevant origin/destination regional modules, and `world/GEOGRAPHY_AND_TRAVEL.md`; resolve duration only through `gameplay/TIME_AND_ACTION_RULES.md`. Do not assume direct connections between all locations.

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

This workflow applies to **all three major powers**—Golden Dragon Empire, Tianhai Yunzhou, and Beiming Gu—and to the Lawless Territories whenever they are involved. It applies to gameplay, lore questions, audits, and repository edits. Do not apply the Golden Dragon Empire's administrative counts or settlement classifications to Tianhai Yunzhou or Beiming Gu.

Before narrating a location, describing its government/economy/customs, creating a settlement or NPC, counting local institutions, or changing regional files, follow this path:

1. Read `world/CANON_DECISIONS_AND_PRECEDENCE.md` for binding owner decisions and conflict precedence.
2. Read `world/MAP_AND_REGIONS.md` and `world/WORLD.md` for the established world layout and cross-power context.
3. Read the exact regional module for the location from `world/REGION_*.md` or the explicitly linked canonical Lawless Territories module. This regional module is the primary source for local established facts and its own unfilled fields. Use `regions/<power>/INDEX.md` and `regions/<power>/npcs/REGISTRY.md` only for NPC navigation and roster checks; do not assume these folders contain settlement modules.
4. Follow the INDEX links for the relevant government, faction, institution, service, economy, or established NPC; read those specific sources rather than inferring details from a region's identity.
5. If travel or cross-region movement matters, read `world/LOCATION_AND_ROUTE_NETWORK.md`, the origin and destination regional modules, and `world/GEOGRAPHY_AND_TRAVEL.md`; resolve travel duration only through `gameplay/TIME_AND_ACTION_RULES.md`. A missing route is not proof of a direct connection or of impossibility.
6. For cross-region counts, audits, or edits to a shared register, inspect every affected regional roster and the canonical register governing that category. Do not extrapolate the Golden Dragon Empire's 13-village count to other powers; no count is established unless its authoritative source says so.
7. Reconcile the planned response or edit against the loaded canon. Preserve explicit owner decisions, do not let a newer secondary file silently override established canon, and distinguish confirmed facts from proposals, estimates, rumors, and unknown details.

**Beiming Gu safeguard:** the Beiming Gu regional files are owner-fillable scaffolds where their contents say details are pending. Treat only their confirmed foundations and cross-referenced official sources as established. Do not fill missing settlements, routes, local administration, prices, customs, or NPCs with invented facts and then present them as pre-existing canon. A GM may narrate situational details only within the authority rules and must not silently make them permanent canon.

**Tianhai Yunzhou safeguard:** use `world/REGION_TIANHAI_YUNZHOU.md` and its linked institutional/governance/NPC references for Tianhai Yunzhou-specific facts. Do not transfer the Golden Dragon Empire's bureaucratic tiers, academy count, village register, or local social rules to Tianhai Yunzhou without a source that explicitly establishes them.

If a required file cannot be fetched, name the missing source and limit the answer to what remains supported. A summary, prior memory, or region name is not a substitute for reading current canonical sources.

### Regional/NPC navigation triggers
| Situation | Required source |
|---|---|
| Character is in or traveling to one of the named regions | Fetch the matching `world/REGION_*.md` module, plus `world/MAP_AND_REGIONS.md` / `world/GEOGRAPHY_AND_TRAVEL.md` as needed; for any Lawless Territories scene, also fetch `world/LAWLESS_TERRITORIES.md` |
| Character enters a settlement listed in a regional module | Read that region's settlement and NPC registry; do not assume undocumented shops, residents, or authorities exist |
| Character meets an established recurring or major NPC | Read the NPC profile linked from the regional registry and preserve prior continuity |
| Character meets a new minor NPC | Follow `world/NPC_MANAGEMENT.md` and `templates/AUTHORITY_ORDER.md`; do not invent major secrets or present improvised details as permanent canon |
| Ruined expedition, map submission, official exploration credit, payment, or suspected anomaly | Read `world/RUINED_ARCHIVER.md`, `world/GEOGRAPHY_AND_TRAVEL.md`, and `world/HISTORY.md`; also load the relevant regional module and `world/LAWLESS_TERRITORIES.md` when applicable |
| Faction presence, membership, or authority matters | Read `world/FACTIONS.md` and the matching regional module; regional association alone does not prove current control |
| A character in Tianhai Yunzhou seeks a Guild contract, trade association, healer, or medical service | Read `world/REGION_TIANHAI_YUNZHOU.md`, `world/FACTIONS.md`, and `world/SPIRIT_HUNTERS_GUILD.md` for Guild work; read `world/WORLD.md` for cross-world Medicine Hall Society canon. Check `core/10_ECONOMY_SYSTEM.md` before stating prices or fees |
| Martial Soul Awakening or the Grand Martial Soul Awakening Hall is mentioned in any major power | Read `world/CANON_DECISIONS_AND_PRECEDENCE.md`, `core/MARTIAL_SOUL.md`, `core/MARTIAL_SOUL_AWAKENING.md`, and the relevant power's regional/governance modules. There is exactly one Hall at the principal civilizational center of each major power; do not invent secondary branches or apply Golden Dragon Empire-specific fees/subsidies to Tianhai Yunzhou or Beiming Gu |
| A character seeks a first or later Spirit Ring through an academy expedition, a Guild party, or a solo hunt | Read `core/SPIRIT_RING_RULES.md`, `core/CULTIVATION_SYSTEM.md`, and `bestiary/SPIRIT_BEAST_RULES.md`; then load the route-specific source (`core/CULTIVATOR_ACADEMIES.md` for an academy Safe Route or `world/SPIRIT_HUNTERS_GUILD.md` for a Guild party) and relevant combat, HP, injury, time, and metabolism modules. Before every absorption attempt, calculate the `Spirit Ring Absorption` profile status from current state and enforce the hard gate; player insistence never bypasses eligibility. Resolve tracking, combat, ring ownership, eligibility, and absorption as separate steps. If ineligible and the character forces the attempt, apply only the existing deviation/HP and injury rules; do not invent damage or automatic permanent disability. |
| A character seeks any Guild contract, joins a temporary Guild team, accepts escort/cargo/item-search work, seeks a Spirit Beast hunting party, or encounters a Guild bounty notice | Read `world/SPIRIT_HUNTERS_GUILD.md`; also read `core/SPIRIT_RING_RULES.md`, `bestiary/SPIRIT_BEAST_RULES.md`, and relevant combat/HP/injury modules when the contract involves Spirit Beasts or combat |
| Government office, imperial ministry, or civil-versus-military authority matters in the Golden Dragon Empire | Read `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md`, then the matching regional module and any linked NPC profile |
| A character visits or discusses a Golden Dragon Empire prefecture, county, city, or other administrative unit | Read `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md` and the matching `world/REGION_*.md` module; use the atlas as the single source for jurisdiction names and counts |
| A scene, edit, or question involves Golden Dragon Empire villages, hamlets, rural settlement counts, or a regional settlement roster | Follow the mandatory **Settlement Canon Load Path** below; do not rely on INDEX summaries alone |
| A character seeks banking, information brokerage, medical services, foundational education, or a public knowledge library in the Golden Dragon Empire | Read `world/GOLDEN_DRAGON_EMPIRE_POPULATION_SERVICES.md` plus the matching regional module; use its named branch register and access limits |
| NPC action changes the persistent world | Check `world/DYNAMIC_EVENTS.md` and the approved owner workflow; do not claim persistence without a verified repository update |

**Canon boundary:** The regional modules preserve the region identities, named settlements, and faction associations already present in official world files. They intentionally leave detailed geography, routes, settlement-level population and demographics, customs, prices, named NPCs, hidden lore, and current faction control unfilled for the owner to define. administrative names across the Golden Dragon Empire and planning totals are governed by `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`. Do not infer those details from a module's existence.
