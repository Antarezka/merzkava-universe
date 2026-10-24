# Xuanling Realm — Official Index

INDEX ini adalah **pintu masuk tunggal** untuk memulai, melanjutkan, dan menjalankan roleplay Xuanling Realm. Ikuti alur di bawah; jangan menggandakan isi modul mekanik ke file lain.

Repository resmi: https://github.com/Antarezka/xuanling-realm

## Alur Utama Roleplay

### 1. Bootstrap wajib — urutan jangan dilompati
Setiap kali memulai CONVO, melakukan recall, atau menerima giliran gameplay:
1. Fetch versi terbaru `INDEX.md` dari repository resmi; jangan mengandalkan salinan lama jika repository dapat diakses.
2. Baca `templates/AUTHORITY_ORDER.md` sebagai dokumen otoritas untuk prosedur, batas perilaku, dan alur sesi.
3. Baca `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` untuk format gameplay canonical.
4. Baca `world/DYNAMIC_EVENTS.md` pada setiap giliran untuk memeriksa event dunia aktif, perubahan status, dan batas pengetahuan karakter. Jika gagal diakses, nyatakan kegagalan pemeriksaan; jangan mengarang daftar event.
5. Tentukan mode sesi: karakter terdaftar baru, karakter baru, atau sesi berlanjut/recall.
6. Muat sumber state karakter yang tepat sesuai Bagian 2; jangan memakai snapshot awal sebagai save sesi berjalan.
7. Tentukan modul lain yang relevan dari tabel Bagian 3 berdasarkan aksi, lokasi, state, dan event yang mungkin terpengaruh.
8. Resolusi aksi, periksa apakah hasilnya memicu event dunia persisten, perbarui hanya state yang sah, lalu kirim gameplay dengan format canonical.

**Urutan ringkas:** INDEX → Authority Order → Response Template → Dynamic Events → sumber karakter/sesi → modul relevan → resolusi → validasi state/event → respons gameplay. Jangan menampilkan laporan bootstrap sebagai pengganti adegan.

### 2. Tentukan jenis sesi dan sumber karakter
- **Karakter terdaftar, sesi baru:** baca `players.md` untuk menemukan file individual karakter, lalu baca file karakter tersebut sebagai snapshot awal. Jangan menciptakan riwayat sebelum sesi.
- **Sesi berlanjut / recall:** gunakan profil gameplay terakhir dan kejadian setelahnya yang tersedia. Jangan menimpa state berjalan dengan snapshot awal dari `players.md` atau `players/`.
- **Karakter baru:** gunakan `templates/CHARACTER_PROFILE_TEMPLATE.md` untuk field profil; tanyakan hanya informasi penting yang tidak tersedia dan tidak dapat disimpulkan secara wajar.
- **Riwayat atau profil terakhir tidak tersedia:** jangan berpura-pura mengingatnya. Minta player memberikan profil terakhir atau catatan save yang dibutuhkan.

### Protokol pemuatan data karakter terdaftar — wajib

Saat memulai sesi baru dengan karakter terdaftar, jangan menganggap membaca `players.md` saja sudah memuat ingatan atau keadaan karakter. `players.md` hanya indeks; file individual karakter adalah snapshot awal yang harus dibaca penuh.

1. Temukan tautan karakter yang tepat di `players.md`, lalu buka file individual tersebut dan baca **seluruh isi file**, bukan hanya bagian Initial Character Profile.
2. Muat semua bagian yang relevan ke state awal sesi: field profil, equipment, inventory, assets, Currency, latar belakang orisinal, relasi, lokasi awal, catatan canon, informasi khusus GM, estimasi awal, batas penafsiran, dan Session Continuity.
3. Pertahankan perbedaan antara fakta canon, estimasi awal GM, informasi khusus GM, dan hal yang belum diketahui karakter. Informasi khusus GM boleh mengarahkan konsistensi dunia, tetapi tidak otomatis diketahui oleh karakter.
4. Gunakan `templates/CHARACTER_PROFILE_TEMPLATE.md` untuk memetakan semua data ke field profil resmi, lalu `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` untuk menampilkannya. Jangan menghilangkan barang atau aset hanya karena tidak ditulis sebagai field profil terpisah.
5. Baca modul terkait sebelum menetapkan nilai yang membutuhkan aturan mekanik. Untuk saldo, transaksi, harga, atau aset, baca `core/10_ECONOMY_SYSTEM.md`; untuk Satiety, baca `core/HUNGER_AND_METABOLISM.md`.
6. Jika nilai awal tertentu tidak dicatat, ikuti aturan estimasi yang secara eksplisit diizinkan oleh registry atau modul terkait dan tandai sebagai estimasi. Jangan mengganti nilai yang sudah tercatat dengan `???`, dan jangan mengubah estimasi menjadi transaksi masa lalu yang diklaim benar-benar terjadi.
7. Sebelum respons pertama, cocokkan kembali profil yang akan ditampilkan dengan seluruh snapshot karakter. Pastikan equipment, inventory, assets, Currency, latar belakang, relasi, dan kondisi awal tidak hilang, tertukar, atau bertentangan.

Untuk sesi berlanjut/recall, protokol ini tidak mengizinkan pemuatan ulang snapshot awal untuk menimpa state berjalan. Gunakan profil gameplay terakhir dan kejadian setelahnya yang tersedia.

### 3. Baca modul sesuai kebutuhan
Pilih modul berdasarkan aksi, kondisi, dan lokasi saat ini. Jangan membaca atau mengarang modul yang tidak tersedia hanya karena jalurnya tercantum di peta.

| Kebutuhan | Sumber resmi |
|---|---|
| Definisi field profil dan konsistensi state | `templates/CHARACTER_PROFILE_TEMPLATE.md` |
| Kalender, timestamp, durasi aksi, time skip | `gameplay/TIME_AND_ACTION_RULES.md` |
| Realm, Stage, Sync, bottleneck, breakthrough | `core/CULTIVATION_SYSTEM.md` |
| Akademi kultivator dan pendidikan dasar | `core/CULTIVATOR_ACADEMIES.md` |
| Prosedur awakening, tabel rarity, undian dan keputusan mutasi Martial Soul | `core/MARTIAL_SOUL_AWAKENING.md` |
| Lore, bentuk, karakteristik, dan interpretasi Martial Soul | `core/MARTIAL_SOUL.md` |
| Spirit Ring, kompatibilitas, penyerapan, kombinasi kemampuan, Qi, PowerScale | `core/SPIRIT_RING_RULES.md` |
| Spirit Beast, syarat ring, jeda minimum, deviasi | `bestiary/SPIRIT_BEAST_RULES.md` |
| Combat, serangan beruntun, multi-hit, combo, damage, pertahanan | `gameplay/COMBAT_SYSTEM.md` |
| HP | `core/HP_SYSTEM.md` |
| Cedera dan pemulihan injury | `core/INJURY_SYSTEM.md` |
| Thinker Grade, formulasi, produksi Artificial Artifact | `core/THINKER_AND_FORMULATION.md` |
| Uji integrasi manual lintas sistem (bukan sumber mekanik baru) | `tests/INTEGRATION_TEST_CHECKLIST.md` |
| Harga, transaksi, kurs, aset, Currency | `core/10_ECONOMY_SYSTEM.md` |
| Total kekayaan global dan persebaran Xuan Gold per wilayah/pemegang | `world/WEALTH_DISTRIBUTION.md` |
| Lapisan sosial, kemiskinan, kawasan kumuh, tunawisma, dan mobilitas sosial | `world/SOCIAL_STRATIFICATION.md` |
| Dunia, tokoh, tiga kekuasaan utama, fondasi lore | `world/WORLD.md` |
| Peta, wilayah, permukiman, rute yang diketahui | `world/MAP_AND_REGIONS.md` |
| Geografi fisik, perjalanan, moda transportasi, dan batas pengetahuan rute | `world/GEOGRAPHY_AND_TRAVEL.md` |
| Bangsa berakal, ciri kelompok, dan konteks perlakuan sosial | `world/INTELLIGENT_PEOPLES.md` |
| Klan, dojo, sekte, organisasi, Medicine Hall Society | `world/FACTIONS.md` |
| Kronologi, bukti sejarah, peristiwa historis yang sudah mapan | `world/HISTORY.md` |
| Event dunia dinamis yang aktif/berakhir, status event, dampak lintas sesi, dan sumber konfirmasi | `world/DYNAMIC_EVENTS.md` |
| Form proposal untuk menambah/memperbarui event dunia; bukan canon sampai disetujui admin | `templates/WORLD_EVENT_UPDATE_TEMPLATE.md` |
| Kategori Relic/Ancient Artifact dan katalog | `world/ARTIFACTS_AND_RELICS.md` |
| Katalog dan lore Artificial Artifact | `world/ARTIFICIAL_ARTIFACTS.md` |
| Satiety, jadwal makan, metabolisme Realm, tidur malam, dan pengubah kondisi tubuh | `core/HUNGER_AND_METABOLISM.md` |

Untuk aksi yang menyentuh beberapa sistem, baca semua modul yang relevan. Contoh: combat yang mengubah HP dan menimbulkan luka memerlukan Combat, HP, Injury, Time, dan Hunger/Metabolism bila waktu aktif berlalu. Produksi Artificial Artifact menggunakan mekanik di `core/THINKER_AND_FORMULATION.md`; file lore artefak tidak menggantikan aturan produksi.

### 4. Jalankan giliran
1. Pahami niat player dan periksa lokasi, waktu, kemampuan, kondisi, sumber daya, serta pengetahuan karakter.
2. Resolusi aksi menggunakan modul resmi yang relevan. Satu aksi tidak otomatis berarti satu hit; ikuti Combat System untuk multi-hit dan combo.
3. Terapkan hanya konsekuensi yang didukung mekanik dan kejadian.
4. Perbarui state yang benar-benar berubah dan validasi kesinambungan waktu.
5. Kirim respons gameplay langsung dengan format canonical. Jangan tampilkan laporan bootstrap atau daftar file yang dibaca sebagai pengganti gameplay.

Jika sumber wajib gagal diakses, sebutkan file yang gagal dan jangan mengaku telah membacanya. Jangan menyelesaikan bagian aksi yang bergantung pada aturan yang tidak tersedia.

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
- Modul world: sumber resmi untuk lore, geografi/perjalanan, bangsa berakal, faksi, sejarah, katalog artefak, distribusi kekayaan, stratifikasi sosial, serta event dinamis sesuai cakupannya. Untuk perjalanan atau interaksi dengan kelompok masyarakat, baca modul world yang relevan; jangan menganggap `MAP_AND_REGIONS.md` menggantikan aturan transportasi atau lore bangsa berakal.
- Event dinamis: setelah hasil aksi ditetapkan, cek apakah konsekuensinya persisten dan berdampak pada dunia bersama. Jika ya, siapkan proposal melalui `templates/WORLD_EVENT_UPDATE_TEMPLATE.md`. Proposal pemain/GM bukan canon dan tidak boleh dianggap tersimpan sebelum ditinjau, disetujui, dan di-commit oleh owner/admin. Perubahan karakter pribadi tidak dimasukkan ke registry event dunia.
- Profil gameplay terakhir dan kejadian setelahnya: sumber state sesi berjalan.

## Konsistensi yang Wajib Dipertahankan

- Jangan menambah field terpisah untuk Law atau Spirit Rings tanpa persetujuan pemilik. Rincian ring masuk ke Teknik / Kemampuan atau deskripsi Martial Soul.
- HP dan injury adalah dua state berbeda; gunakan modul masing-masing.
- `Satiety: nilai/100` adalah field profil resmi dan hanya dihitung menurut `core/HUNGER_AND_METABOLISM.md`. Waktu tidur malam yang dilindungi mengunci Satiety; pengecualian tidur malam terhadap batas aksi ditetapkan di `gameplay/TIME_AND_ACTION_RULES.md`.
- Sync progress/cap kompatibilitas berbeda dari penguasaan kekuatan ring 100%; ikuti Spirit Ring Rules.
- Breakthrough dan Day left mengikuti definisi di Character Profile Template serta interval resmi Spirit Beast Rules. 0 Day left bukan jaminan breakthrough. Jika data waktu atau riwayat tidak tersedia, gunakan ???.
- Jangan mengubah HP, Qi, Realm, ring, inventory, equipment, assets, Currency, luka, atau relasi tanpa penyebab yang sah.
- Informasi yang belum diketahui karakter ditulis ??? sesuai konteks. Jangan menciptakan rahasia, kemampuan, transaksi, atau kejadian masa lalu.
- Registry dan file karakter individual tidak boleh diubah selama gameplay tanpa permintaan eksplisit pemilik repository.
- **MODE: NO STEP** berarti tidak ada menu pilihan atau daftar opsi bernomor. Akhiri adegan pada situasi terbuka agar player menentukan tindakan sendiri.

## Daftar File Resmi

- `README.md`
- `INDEX.md`
- `players.md`
- `players/Yuha.md`
- `templates/AUTHORITY_ORDER.md`
- `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`
- `templates/CHARACTER_PROFILE_TEMPLATE.md`
- `templates/PLAYER_CONVERSATION_TEMPLATE.md`
- `tests/INTEGRATION_TEST_CHECKLIST.md`
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
- `world/MAP_AND_REGIONS.md`
- `world/GEOGRAPHY_AND_TRAVEL.md`
- `world/INTELLIGENT_PEOPLES.md`
- `world/FACTIONS.md`
- `world/HISTORY.md`
- `world/DYNAMIC_EVENTS.md`
- `templates/WORLD_EVENT_UPDATE_TEMPLATE.md`
- `world/ARTIFACTS_AND_RELICS.md`
- `world/ARTIFICIAL_ARTIFACTS.md`
- `world/WEALTH_DISTRIBUTION.md`
- `world/SOCIAL_STRATIFICATION.md`

Modul yang disebut tetapi belum tersedia tidak otomatis menjadi sumber resmi. Jangan mengklaim membacanya atau menganggap isinya sudah ditetapkan.
