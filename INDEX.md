# Xuanling Realm — Official Index

Ini adalah pintu masuk resmi untuk memulai dan menjalankan roleplay Xuanling Realm. INDEX mengatur navigasi dan alur kerja; **aturan rinci harus dibaca dari modul sumbernya**, bukan disalin ulang ke banyak file.

Repository: https://github.com/Antarezka/xuanling-realm

## 1. Sumber Utama per Urusan

| Urusan | Sumber utama | Fungsi |
|---|---|---|
| Perilaku dan prosedur GM | `templates/GM_PROMPT.md` | Alur sesi, hierarki sumber, anti-cheat, format gameplay |
| Format profil | `templates/CHARACTER_PROFILE_TEMPLATE.md` | Urutan field dan aturan pengisian profil |
| Snapshot awal karakter | `players.md` | Data awal karakter terdaftar, bukan save berjalan |
| Lore dan canon dunia | `world/WORLD.md` | Fakta dunia, wilayah, tokoh, dan lore utama |
| Kultivasi, Realm, Stage | `core/CULTIVATION_SYSTEM.md` | Progres, bottleneck, breakthrough |
| Martial Soul | `core/MARTIAL_SOUL.md` | Awakening dan aturan Martial Soul |
| Spirit Ring, Qi, PowerScale | `core/SPIRIT_RING_RULES.md` | Usia, kompatibilitas, penyerapan, Qi, PowerScale |
| HP | `core/HP_SYSTEM.md` | HP maksimum, format dan validasi HP saat ini |
| Thinker dan formulasi | `core/THINKER_AND_FORMULATION.md` | Grade Thinker, formulasi, peluang produksi artefak |
| Spirit Beast | `bestiary/SPIRIT_BEAST_RULES.md` | Kategori Beast, syarat dan jeda penyerapan, deviasi |
| Combat | `gameplay/COMBAT_SYSTEM.md` | Inisiatif, kesiapan, hit, damage, pertahanan, serangan beruntun, combo, konsekuensi |
| Waktu dan durasi aksi | `gameplay/TIME_AND_ACTION_RULES.md` | Timestamp, kalender sesi, durasi, time skip |
| Ekonomi | `core/10_ECONOMY_SYSTEM.md` | Kurs, harga, transaksi, kelangkaan dan kualitas |
| Peta dan wilayah | `world/WORLD.md` | Sumber lore yang tersedia; modul peta khusus belum dibuat |
| Faksi | `world/WORLD.md` | Gunakan detail faksi yang benar-benar tercatat di WORLD |
| Sejarah | `world/WORLD.md` | Gunakan sejarah yang benar-benar tercatat di WORLD |
| Artefak dan relik | `world/WORLD.md` | Gunakan asal-usul dan fungsi yang benar-benar tercatat di WORLD |

## 2. Alur Wajib Setiap Giliran Gameplay

1. Fetch dan baca ulang INDEX ini dari branch resmi.
2. Baca `templates/GM_PROMPT.md`.
3. Tentukan mode: sesi baru terdaftar, sesi berlanjut, atau karakter baru.
4. Fetch hanya modul yang diperlukan untuk aksi dan kondisi saat ini. Pastikan file tersedia dan terbaca.
5. Selesaikan aksi menggunakan modul sumber; jangan membuat aturan pengganti untuk bagian yang belum ditetapkan.
6. Perbarui hanya state yang berubah karena kejadian sah.
7. Gunakan format persis dari `templates/CHARACTER_PROFILE_TEMPLATE.md` dan aturan timestamp dari `gameplay/TIME_AND_ACTION_RULES.md`.

**Jangan mengklaim sudah membaca file yang gagal diakses.** Jika modul penting tidak tersedia, jelaskan keterbatasannya dan lanjutkan hanya bagian yang didukung sumber.

## 3. Pilih Modul Berdasarkan Aksi

- Realm, Stage, Sync progress, bottleneck, breakthrough: `core/CULTIVATION_SYSTEM.md` dan `core/SPIRIT_RING_RULES.md`.
- Awakening atau Martial Soul: `core/MARTIAL_SOUL.md`.
- Spirit Beast, perburuan, syarat ring, jeda minimum, deviasi: `bestiary/SPIRIT_BEAST_RULES.md`; tambahkan `core/SPIRIT_RING_RULES.md` untuk formula deviasi lengkap (§5: persentase deviasi 1–100%, skala kehilangan HP menurut nomor ring, pengali, kategori risiko, dan alur GM).
- Combat, serangan beruntun, atau combo: `gameplay/COMBAT_SYSTEM.md`; satu aksi dapat berisi beberapa hit dan aturan combo default berlaku dari modul ini. Tambahkan `core/HP_SYSTEM.md` bila HP berubah atau perlu divalidasi.
- Waktu, perjalanan berdurasi, kultivasi panjang, atau time skip: `gameplay/TIME_AND_ACTION_RULES.md` serta modul mekanik terkait.
- HP atau pembuatan/pembaruan profil: `core/HP_SYSTEM.md` dan template profil.
- Makan, lapar, metabolisme: gunakan `core/HUNGER_AND_METABOLISM.md` **hanya jika file tersebut tersedia**; saat ini belum ada di repository.
- Thinker atau pembuatan Artificial Artifact: `core/THINKER_AND_FORMULATION.md`; penggunaan artefak dalam pertarungan juga mengikuti Combat.
- Pembelian, penjualan, appraisal, tawar-menawar, pembayaran, atau perubahan saldo: `core/10_ECONOMY_SYSTEM.md`.
- Lokasi, perjalanan, faksi, sejarah, atau lore: `world/WORLD.md`.
- Karakter terdaftar yang memulai sesi baru: `players.md`. Jangan gunakan registry untuk menimpa state berjalan.
- Pemain meminta bantuan tentang proyek atau struktur repository: `README.md`.

## 4. Format Profil dan Konsistensi State

Template profil adalah satu-satunya sumber untuk urutan dan nama field profil. Jangan menyalin ulang format profil penuh ke INDEX, GM Prompt, atau registry.

- Jangan menambah field terpisah untuk Law atau Spirit Rings tanpa persetujuan pemilik. Realm menentukan jumlah slot; detail ring yang dimiliki masuk ke Teknik / Kemampuan atau deskripsi Martial Soul.
- HP saat ini harus berasal dari profil terakhir atau kejadian yang tercatat; jangan otomatis menganggap HP penuh.
- Perubahan Qi, ring, Realm, inventory, equipment, assets, Currency, luka, dan hubungan harus memiliki penyebab yang sah.
- `players.md` adalah snapshot awal. Profil terakhir dan kejadian setelahnya adalah state sesi berjalan.
- Informasi yang belum diketahui karakter ditulis `???` sesuai konteks. Jangan menciptakan rahasia besar, kemampuan, transaksi, atau kejadian masa lalu tanpa dasar.
- MODE: NO STEP berarti tidak ada menu pilihan atau daftar opsi bernomor; akhiri adegan pada situasi terbuka.

## 5. File Resmi yang Tersedia

- `README.md`
- `templates/GM_PROMPT.md`
- `templates/CHARACTER_PROFILE_TEMPLATE.md`
- `players.md`
- `core/CULTIVATION_SYSTEM.md`
- `core/MARTIAL_SOUL.md`
- `core/SPIRIT_RING_RULES.md`
- `core/HP_SYSTEM.md`
- `core/THINKER_AND_FORMULATION.md`
- `core/10_ECONOMY_SYSTEM.md`
- `bestiary/SPIRIT_BEAST_RULES.md`
- `gameplay/COMBAT_SYSTEM.md`
- `gameplay/TIME_AND_ACTION_RULES.md`
- `world/WORLD.md`

## 6. Modul yang Belum Dibuat

Jalur berikut belum tersedia dan tidak boleh dianggap sudah dibaca atau menjadi sumber resmi:

- `core/HUNGER_AND_METABOLISM.md`
- `world/MAP_AND_REGIONS.md`
- `world/FACTIONS.md`
- `world/HISTORY.md`
- `world/ARTIFACTS_AND_RELICS.md`
- `world/CUSTOM_EVENTS.md`

Sampai modul khusus dibuat, gunakan hanya informasi yang benar-benar ada di `world/WORLD.md`. Jangan mengarang jalur, isi, atau status file.

## 7. Prinsip Integrasi

- INDEX adalah peta dan alur; bukan tempat menyimpan ulang semua mekanik.
- GM Prompt adalah prosedur GM; bukan sumber angka combat, HP, ekonomi, atau waktu.
- Template profil adalah bentuk state; bukan buku aturan mekanik.
- Registry adalah snapshot awal; bukan save otomatis.
- Setiap modul mekanik menjadi sumber utama untuk ruang lingkupnya.
- Jika aturan belum ditetapkan atau dua sumber bertentangan, tandai masalahnya. Jangan menyelesaikan konflik secara diam-diam.
