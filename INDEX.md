# Xuanling Realm — Official Index

INDEX ini adalah **pintu masuk tunggal** untuk memulai, melanjutkan, dan menjalankan roleplay Xuanling Realm. Ikuti alur di bawah; jangan menggandakan isi modul mekanik ke file lain.

Repository resmi: https://github.com/Antarezka/xuanling-realm

## Alur Utama Roleplay

### 1. Baca sumber inti
Setiap kali memulai CONVO, melakukan recall, atau menerima giliran gameplay:
1. Fetch versi terbaru file ini (INDEX.md) dari repository resmi.
2. Baca `templates/GM_PROMPT.md` untuk prosedur dan batas perilaku Game Master.
3. Baca `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` untuk format respons gameplay yang wajib dipakai.

### 2. Tentukan jenis sesi dan sumber karakter
- **Karakter terdaftar, sesi baru:** baca `players.md` untuk menemukan file individual karakter, lalu baca file karakter tersebut sebagai snapshot awal. Jangan menciptakan riwayat sebelum sesi.
- **Sesi berlanjut / recall:** gunakan profil gameplay terakhir dan kejadian setelahnya yang tersedia. Jangan menimpa state berjalan dengan snapshot awal dari `players.md` atau `players/`.
- **Karakter baru:** gunakan `templates/CHARACTER_PROFILE_TEMPLATE.md` untuk field profil; tanyakan hanya informasi penting yang tidak tersedia dan tidak dapat disimpulkan secara wajar.
- **Riwayat atau profil terakhir tidak tersedia:** jangan berpura-pura mengingatnya. Minta player memberikan profil terakhir atau catatan save yang dibutuhkan.

### 3. Baca modul sesuai kebutuhan
Pilih modul berdasarkan aksi, kondisi, dan lokasi saat ini. Jangan membaca atau mengarang modul yang tidak tersedia hanya karena jalurnya tercantum di peta.

| Kebutuhan | Sumber resmi |
|---|---|
| Definisi field profil dan konsistensi state | `templates/CHARACTER_PROFILE_TEMPLATE.md` |
| Kalender, timestamp, durasi aksi, time skip | `gameplay/TIME_AND_ACTION_RULES.md` |
| Realm, Stage, Sync, bottleneck, breakthrough | `core/CULTIVATION_SYSTEM.md` |
| Awakening dan Martial Soul | `core/MARTIAL_SOUL.md` |
| Spirit Ring, kompatibilitas, penyerapan, Qi, PowerScale | `core/SPIRIT_RING_RULES.md` |
| Spirit Beast, syarat ring, jeda minimum, deviasi | `bestiary/SPIRIT_BEAST_RULES.md` |
| Combat, serangan beruntun, multi-hit, combo, damage, pertahanan | `gameplay/COMBAT_SYSTEM.md` |
| HP | `core/HP_SYSTEM.md` |
| Cedera dan pemulihan injury | `core/INJURY_SYSTEM.md` |
| Thinker Grade, formulasi, produksi Artificial Artifact | `core/THINKER_AND_FORMULATION.md` |
| Harga, transaksi, kurs, aset, Currency | `core/10_ECONOMY_SYSTEM.md` |
| Dunia, tokoh, tiga kekuasaan utama, fondasi lore | `world/WORLD.md` |
| Peta, wilayah, permukiman, rute yang diketahui | `world/MAP_AND_REGIONS.md` |
| Klan, dojo, sekte, organisasi, Medicine Hall Society | `world/FACTIONS.md` |
| Kronologi, bukti sejarah, peristiwa historis | `world/HISTORY.md` |
| Kategori Relic/Ancient Artifact dan katalog | `world/ARTIFACTS_AND_RELICS.md` |
| Katalog dan lore Artificial Artifact | `world/ARTIFICIAL_ARTIFACTS.md` |
| Lapar dan metabolisme | `core/HUNGER_AND_METABOLISM.md` — belum tersedia |

Untuk aksi yang menyentuh beberapa sistem, baca semua modul yang relevan. Contoh: combat yang mengubah HP dan menimbulkan luka memerlukan Combat, HP, dan Injury. Produksi Artificial Artifact menggunakan mekanik di `core/THINKER_AND_FORMULATION.md`; file lore artefak tidak menggantikan aturan produksi.

### 4. Jalankan giliran
1. Pahami niat player dan periksa lokasi, waktu, kemampuan, kondisi, sumber daya, serta pengetahuan karakter.
2. Resolusi aksi menggunakan modul resmi yang relevan. Satu aksi tidak otomatis berarti satu hit; ikuti Combat System untuk multi-hit dan combo.
3. Terapkan hanya konsekuensi yang didukung mekanik dan kejadian.
4. Perbarui state yang benar-benar berubah dan validasi kesinambungan waktu.
5. Kirim respons gameplay langsung dengan format canonical. Jangan tampilkan laporan bootstrap atau daftar file yang dibaca sebagai pengganti gameplay.

Jika sumber wajib gagal diakses, sebutkan file yang gagal dan jangan mengaku telah membacanya. Jangan menyelesaikan bagian aksi yang bergantung pada aturan yang tidak tersedia.

## Sumber Utama dan Batas Tanggung Jawab

- `INDEX.md`: alur dan navigasi.
- `templates/GM_PROMPT.md`: perilaku GM, prosedur, anti-cheat, dan resolusi aksi tingkat umum.
- `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`: **satu-satunya sumber format visual lengkap setiap respons gameplay**.
- `templates/CHARACTER_PROFILE_TEMPLATE.md`: arti field dan aturan konsistensi state; bukan format output kedua.
- `templates/PLAYER_CONVERSATION_TEMPLATE.md`: prompt pemanggilan singkat; bukan sumber mekanik.
- `players.md`: indeks karakter terdaftar.
- `players/<Nama>.md`: snapshot awal karakter individual, bukan save berjalan.
- Modul mekanik: sumber resmi untuk aturan di ruang lingkupnya.
- Modul world: sumber resmi untuk lore, geografi, faksi, sejarah, dan katalog artefak sesuai cakupannya.
- Profil gameplay terakhir dan kejadian setelahnya: sumber state sesi berjalan.

## Konsistensi yang Wajib Dipertahankan

- Jangan menambah field terpisah untuk Law atau Spirit Rings tanpa persetujuan pemilik. Rincian ring masuk ke Teknik / Kemampuan atau deskripsi Martial Soul.
- HP dan injury adalah dua state berbeda; gunakan modul masing-masing.
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
- `templates/GM_PROMPT.md`
- `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`
- `templates/CHARACTER_PROFILE_TEMPLATE.md`
- `templates/PLAYER_CONVERSATION_TEMPLATE.md`
- `core/CULTIVATION_SYSTEM.md`
- `core/MARTIAL_SOUL.md`
- `core/SPIRIT_RING_RULES.md`
- `core/HP_SYSTEM.md`
- `core/INJURY_SYSTEM.md`
- `core/THINKER_AND_FORMULATION.md`
- `core/10_ECONOMY_SYSTEM.md`
- `bestiary/SPIRIT_BEAST_RULES.md`
- `gameplay/COMBAT_SYSTEM.md`
- `gameplay/TIME_AND_ACTION_RULES.md`
- `world/WORLD.md`
- `world/MAP_AND_REGIONS.md`
- `world/FACTIONS.md`
- `world/HISTORY.md`
- `world/ARTIFACTS_AND_RELICS.md`
- `world/ARTIFICIAL_ARTIFACTS.md`

Modul yang disebut tetapi belum tersedia tidak otomatis menjadi sumber resmi. Jangan mengklaim membacanya atau menganggap isinya sudah ditetapkan.
