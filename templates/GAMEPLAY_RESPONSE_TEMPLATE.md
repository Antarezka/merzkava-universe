# Merzkava Universe — Canonical Gameplay Response Template

Status: **Satu-satunya sumber resmi untuk bentuk, urutan, nama field, dan sekat visual setiap balasan gameplay.**

Semua trigger awal (`CONVO`), recall, dan giliran lanjutan wajib mengikuti template ini. `INDEX.md` mengarahkan GM ke file ini; `AUTHORITY_ORDER.md` mengatur perilaku GM; modul waktu dan mekanik mengatur perhitungan serta konsekuensi. Jangan menyalin format lengkap ini ke file lain atau membuat format alternatif.

## Format Wajib — MODE: NO STEP

Gunakan susunan vertikal dan sekat pendek agar nyaman dibaca pada layar ponsel. Pertahankan urutan field profil, nama field, dan penutup kanonis. Timestamp boleh dipecah menjadi beberapa baris pendek, tetapi seluruh nilainya wajib ada. Untuk tingkat kultivasi, gunakan field `Spirit Realm`; jangan menyingkatnya menjadi `Realm` atau menulis `Cultivation Realm`. Status awal ditulis `Mortal/0`. `???` hanya untuk identitas karakter yang benar-benar tidak dikenal atau nama Martial Soul yang belum diketahui. Field numerik yang belum tercatat diisi `0`, kecuali HP awal mengikuti inisialisasi resmi dan `Day left` hanya berlaku untuk jeda minimum penyerapan Spirit Ring; bila tidak dapat dihitung, tulis `Belum ditetapkan Day left`. Jika belum ada Spirit Ring yang sedang diproses, Sync progress ditulis `0%/0%`. Field nonnumerik lain yang belum ditetapkan ditulis `Belum ditetapkan`. Jangan pernah mengirim placeholder contoh seperti `...` sebagai nilai akhir field.

```text
🕒 Waktu Merzkava Universe
Tahun: XXXX, Era ???
Musim: [Semi/Panas/Gugur/Dingin] | Tanggal: DD Bulan MM
Hari: [Senin–Minggu] | Cuaca: ... | Jam: HH:MM

Narasi
[Narasi imersif sesuai kejadian, pengetahuan karakter, kondisi dunia, dan konsekuensi yang benar-benar terjadi.]

[LEDGER LOG — hanya tampilkan jika transaksi/perubahan uang, item, atau aset benar-benar terjadi. Letakkan setelah narasi dan sebelum profil. Jika tidak ada perubahan, lewati bagian ini.]

╭─ LEDGER LOG · #[ID]
│ Waktu: ...
│ Jenis: ...
│ Pihak terkait: ...
│ Status: Berhasil / Gagal / Dibatalkan
│ Rincian:
│ • Uang keluar/masuk: ...
│ • Harga, konversi, atau kembalian: ...
│ • Item/aset masuk/keluar: ...
│ Saldo sebelum: ...
│ Perubahan bersih: ...
│ Saldo sesudah: ...
│ Item sebelum → sesudah: ...
╰─

✓ PENEGASAN LEDGER
[Nyatakan transaksi tercatat setelah hasil dan perhitungan diverifikasi. Tegaskan saldo/inventaris diperbarui hanya jika benar-benar sudah diselaraskan.]

╭─〔 PROFIL KARAKTER 〕
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
├─〔 ✉ INV & KEUANGAN 〕
Inventory: ...
Assets Bangunan: ...
Wallet (wealth): ... xc | ... xs | ... xg | ... zj | ... az
├────────────────────
Teknik / Kemampuan: ...
Tujuan Saat Ini: ...
╰────────────────────

【 CATATAN PEMAIN & KONSISTENSI 】

- GM dilarang melakukan overclaim yang memaksakan karakter ke kondisi survival, kerapuhan, atau konsekuensi tidak masuk akal tanpa dasar mekanik maupun kejadian yang jelas.
- Profil harus konsisten dengan profil terakhir. Perubahan status wajib memiliki penyebab yang tercatat.
- Pada sesi baru, cocokkan nama karakter di `players.md`, lalu ambil Wallet dari file `players/<Nama>.md` yang sesuai. `Assets Bangunan` hanya berisi bangunan/properti tercatat; jangan memindahkan tabungan atau penghasilan ke field itu. Jika Authority secara eksplisit menetapkan saldo, gunakan sumber Authority tersebut. Jika saldo tidak tercatat pada sumber yang berlaku, tetapkan satu saldo bootstrap konkret sesuai `core/10_ECONOMY_SYSTEM.md`. Jangan menebak dari Assets atau pekerjaan dan jangan mengundi ulang. Pada sesi berlanjut, gunakan Wallet dari profil gameplay terakhir beserta transaksi sah setelahnya.
- Setiap teknik atau kemampuan wajib disertai deskripsi fungsi yang jelas dan sesuai modul resmi.
- Jangan mengarang informasi yang belum ditetapkan. Gunakan `???` hanya untuk identitas karakter yang benar-benar tidak dikenal atau nama Martial Soul yang belum diketahui. Field numerik yang belum tercatat gunakan `0`; field nonnumerik lain gunakan `Belum ditetapkan` atau `Tidak ada` jika ketiadaan memang diketahui.

catatan kecil:

- Yang terpenting, enjoy your convo, player!

Aksiku : --
```

## Aturan Penerapan

- **Urutan respons:** timestamp → Narasi → LEDGER LOG dan penegasan hanya jika ada perubahan uang/item/aset → profil lengkap → CATATAN PEMAIN & KONSISTENSI → catatan kecil → `Aksiku : --`.
- **Timestamp dan Era:** ikuti `gameplay/TIME_AND_ACTION_RULES.md`. Pada sesi baru, tentukan era sesuai prosedur di sana dan jangan tinggalkan `Era ???` dalam respons gameplay setelah bootstrap selesai. Pada sesi lanjutan, lanjutkan timestamp dan era terakhir yang sah.
- **Ledger terlihat:** setiap transaksi atau perubahan uang, item, maupun aset yang benar-benar terjadi harus memiliki LEDGER LOG setelah narasi dan sebelum profil. Jangan tampilkan log transaksi jika tidak ada perubahan; jangan menyatakan berhasil sebelum transaksi selesai dan hasilnya diverifikasi. Detail wajib mengikuti `core/10_ECONOMY_SYSTEM.md`.
- **Profil:** jangan mengganti, mengurutkan ulang, menghilangkan, atau menambah field profil tanpa persetujuan pemilik repository. Gunakan `templates/CHARACTER_PROFILE_TEMPLATE.md` untuk definisi field. Sekat profil ringkas di atas adalah format visual mobile; seluruh field kanonis harus tetap ada dan urutannya tidak boleh berubah.
- **Breakthrough / Day left:** `Day left` hanya menghitung jeda minimum antarpenyerapan Spirit Ring yang berhasil, bukan timer breakthrough kultivasi umum. Ikuti `templates/CHARACTER_PROFILE_TEMPLATE.md` dan interval resmi di `bestiary/SPIRIT_BEAST_RULES.md`. `0 Day left` bukan jaminan breakthrough atau penyerapan ring berhasil.
- **HP dan cedera:** gunakan `core/HP_SYSTEM.md` serta `core/INJURY_SYSTEM.md` sebagai dua state terpisah.
- **Satiety:** tampilkan `Satiety: nilai/100` dan hitung hanya menurut `core/HUNGER_AND_METABOLISM.md`; tidur malam yang dilindungi mengunci nilai ini.
- **Combat:** satu aksi dapat memuat beberapa hit atau combo jika diizinkan `gameplay/COMBAT_SYSTEM.md`; jangan menyamakan satu aksi dengan satu hit.
- **NO STEP:** jangan menambahkan menu pilihan atau opsi bernomor. Akhiri adegan pada situasi terbuka agar player menentukan tindakan.
- **Sumber gagal:** jangan mengaku membaca file yang tidak dapat diakses. Sebutkan keterbatasan secara singkat dan jangan menyelesaikan bagian yang bergantung pada aturan yang hilang.
