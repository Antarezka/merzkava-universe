# Xuanling Realm — Canonical Gameplay Response Template

Status: **Satu-satunya sumber resmi untuk bentuk, urutan, nama field, dan sekat visual setiap balasan gameplay.**

Semua trigger awal (`CONVO`), recall, dan giliran lanjutan wajib mengikuti template ini. `INDEX.md` mengarahkan GM ke file ini; `AUTHORITY_ORDER.md` mengatur perilaku GM; modul waktu dan mekanik mengatur perhitungan serta konsekuensi. Jangan menyalin format lengkap ini ke file lain atau membuat format alternatif.

## Format Wajib — MODE: NO STEP

Pertahankan struktur, urutan field, nama field, ornamen visual, dan penutup berikut. Isi berdasarkan state serta kejadian yang benar-benar tercatat. `???` hanya untuk identitas karakter yang benar-benar tidak dikenal atau nama Martial Soul yang belum diketahui. Field numerik yang belum tercatat diisi `0`, kecuali HP awal mengikuti inisialisasi resmi dan Day left yang belum dapat dihitung ditulis `Belum ditetapkan`. Jika belum ada Spirit Ring yang sedang diproses, Sync progress ditulis `0%/0%`. Field nonnumerik lain yang belum ditetapkan ditulis `Belum ditetapkan`. Jangan pernah mengirim placeholder contoh seperti `...` sebagai nilai akhir field.

```text
🕒 Waktu Xuanling Realm
Tahun: XXXX, [Era sesi] | Musim: [Semi/Panas/Gugur/Dingin] | Tanggal: DD Bulan MM | Hari: [Senin–Minggu] | Cuaca: ... | Jam: HH:MM

Narasi
[Narasi imersif sesuai kejadian, pengetahuan karakter, kondisi dunia, dan konsekuensi yang benar-benar terjadi.]

╔═══════════════〔 PROFIL KARAKTER 〕═══════════════╗
Nama: ...
Usia: ...
Spirit Realm: .../...
Sync progress: ...%/...%
Breakthrough: ... | ... Day left
Martial Soul: ...
Thinker Grade: ...
HP: .../...
Satiety: .../100
Qi: ...
Kondisi Tubuh: ...
Equipment: ...
╟────────────〔 ✉ INV & KEUANGAN ✉ 〕────────────╢
Inventory: ...
Assets Bangunan: ...
Wallet (wealth): 0 xc | 0 xs | 0 xg | 0 zj | 0 az
╟────────────────────────────────────────────────╢
Teknik / Kemampuan: ...
Tujuan Saat Ini: ...
╚══════════════════════════════════════════════════╝
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
【 CATATAN PEMAIN & KONSISTENSI 】
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

- GM dilarang melakukan overclaim yang memaksakan karakter ke kondisi survival, kerapuhan, atau konsekuensi tidak masuk akal tanpa dasar mekanik maupun kejadian yang jelas.
- Profil harus konsisten dengan profil terakhir. Perubahan status wajib memiliki penyebab yang tercatat.
- Pada sesi baru, cocokkan nama karakter di `players.md`, lalu ambil Wallet dari file `players/<Nama>.md` yang sesuai. Jika Authority secara eksplisit menetapkan saldo, gunakan sumber Authority tersebut. Jika saldo tidak tercatat pada sumber yang berlaku, tetapkan satu saldo bootstrap konkret sesuai `core/10_ECONOMY_SYSTEM.md`. Jangan menebak dari Assets atau pekerjaan dan jangan mengundi ulang. Pada sesi berlanjut, gunakan Wallet dari profil gameplay terakhir beserta transaksi sah setelahnya.
- Setiap teknik atau kemampuan wajib disertai deskripsi fungsi yang jelas dan sesuai modul resmi.
- Jangan mengarang informasi yang belum ditetapkan. Gunakan `???` hanya untuk identitas karakter yang benar-benar tidak dikenal atau nama Martial Soul yang belum diketahui. Field numerik yang belum tercatat gunakan `0`; field nonnumerik lain gunakan `Belum ditetapkan` atau `Tidak ada` jika ketiadaan memang diketahui.

catatan kecil:

- Yang terpenting, enjoy your convo, player!

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Aksiku : --
```

## Aturan Penerapan

- **Timestamp:** ikuti `gameplay/TIME_AND_ACTION_RULES.md`. Pada sesi baru tanpa timestamp, tetapkan kalender sesi yang konsisten; pada sesi lanjutan, lanjutkan timestamp terakhir yang sah.
- **Profil:** jangan mengganti, mengurutkan ulang, menghilangkan, atau menambah field tanpa persetujuan pemilik repository. Nilai state harus berasal dari profil terakhir dan kejadian sah. Pertahankan ornamen kotak profil di atas.
- **Definisi field:** gunakan `templates/CHARACTER_PROFILE_TEMPLATE.md`. File tersebut mendefinisikan arti field dan konsistensi state; file ini menentukan bentuk visual serta urutannya.
- **Breakthrough / Day left:** isi sesuai definisi di bagian terkait `templates/CHARACTER_PROFILE_TEMPLATE.md` dan interval resmi di `bestiary/SPIRIT_BEAST_RULES.md`. `0 Day left` bukan jaminan breakthrough.
- **HP dan cedera:** gunakan `core/HP_SYSTEM.md` serta `core/INJURY_SYSTEM.md` sebagai dua state terpisah.
- **Satiety:** tampilkan `Satiety: nilai/100` dan hitung hanya menurut `core/HUNGER_AND_METABOLISM.md`; tidur malam yang dilindungi mengunci nilai ini.
- **Combat:** satu aksi dapat memuat beberapa hit atau combo jika diizinkan `gameplay/COMBAT_SYSTEM.md`; jangan menyamakan satu aksi dengan satu hit.
- **NO STEP:** jangan menambahkan menu pilihan atau opsi bernomor. Akhiri adegan pada situasi terbuka agar player menentukan tindakan.
- **Sumber gagal:** jangan mengaku membaca file yang tidak dapat diakses. Sebutkan keterbatasan secara singkat dan jangan menyelesaikan bagian yang bergantung pada aturan yang hilang.
