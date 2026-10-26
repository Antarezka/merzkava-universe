# Merzkava Universe — Canonical Gameplay Response Template

Status: **Satu-satunya sumber resmi untuk bentuk, urutan, nama field, dan sekat visual setiap balasan gameplay.**

Semua trigger awal (CONVO), recall, dan giliran lanjutan wajib mengikuti template ini. `INDEX.md` mengatur navigasi/bootstrap; `templates/AUTHORITY_ORDER.md` mengatur perilaku GM; `templates/CHARACTER_PROFILE_TEMPLATE.md` mendefinisikan arti field; modul waktu dan mekanik mengatur perhitungan serta konsekuensi. File ini hanya master **format keluaran gameplay**, bukan tempat menyalin instruksi bootstrap.

## Format Wajib — MODE: NO STEP

Gunakan susunan vertikal dan plakat ringkas yang nyaman dibaca di ponsel. Pertahankan empat seksi profil yang terpisah. Jangan menambah field, mengganti urutan, membuat format alternatif, atau menyalin instruksi dalam tanda kurung siku ke respons akhir. Ganti semua placeholder dengan state konkret yang sudah diverifikasi.

Field `Spirit Ring Absorption` selalu memuat tepat satu status lengkap dengan format `status | Day left`, sesuai `templates/CHARACTER_PROFILE_TEMPLATE.md`. Jangan membuat field terpisah bernama `Breakthrough` atau `Day left`.

```text
🕒 Waktu Merzkava Universe
Tahun: XXXX
Era: ...
Musim: ... | Tanggal: ...
Hari: ... | Cuaca: ... | Jam: HH:MM

━━━━━━━━━━━━━━━━━━

NARASI
[Narasi imersif sesuai kejadian, suasana, dialog, tindakan NPC, pengetahuan karakter, kondisi dunia, dan konsekuensi yang benar-benar terjadi. Narasi harus mendahului ledger.]

[LEDGER LOG hanya tampil jika transaksi atau perubahan uang, item, atau aset benar-benar terjadi. Jika tidak ada perubahan, lewati seluruh bagian ledger.]

╭─ LEDGER LOG · #[ID]
│ Waktu: ...
│ Jenis: ...
│ Pihak terkait: ...
│ Status: Berhasil / Gagal / Dibatalkan
│
│ Rincian:
│ • Pengeluaran/pemasukan: ...
│ • Harga, konversi, atau kembalian: ...
│ • Item/aset masuk atau keluar: ...
│
│ Saldo sebelum: ...
│ Perubahan bersih: ...
│ Saldo sesudah: ...
│
│ Inventory sebelum: ...
│ Perubahan item: ...
│ Inventory sesudah: ...
╰─

✓ PENEGASAN LEDGER
[Nyatakan hasil pencatatan hanya setelah transaksi dan perhitungannya diverifikasi. Jika transaksi gagal atau batal, nyatakan status sebenarnya.]

━━━━━━━━━━━━━━━━━━

   ╱━━━━━━━━━━━━━━╲
◈━━┫ PROFIL KARAKTER ┣━━◈
   ╲━━━━━━━━━━━━━━╱

Nama: ...
Usia: ...
Spirit Realm: ...
Sync progress: ...%/...%
Spirit Ring Absorption: ... | ... Day left
Martial Soul: ...
Thinker Grade: ...
HP: .../...
Satiety: .../100
Qi: ...
Kondisi Tubuh: ...
Equipment: ...

━━━━━━━━━━━━━━━━━━

   ╱━━━━━━━━━━━━━━╲
◈━━┫ INV & KEUANGAN ┣━━◈
   ╲━━━━━━━━━━━━━━╱

Inventory: ...
Assets Bangunan: ...
Wallet (wealth): ... xc | ... xs | ... xg | ... zj | ... az

━━━━━━━━━━━━━━━━━━

   ╱━━━━━━━━━━━━━━━━━━━━╲
◈━━┫ TEKNIK & TUJUAN ┣━━◈
   ╲━━━━━━━━━━━━━━━━━━━━╱

Teknik / Kemampuan: ...
Tujuan Saat Ini: ...

━━━━━━━━━━━━━━━━━━

   ╱━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╲
◈━━┫ CATATAN PEMAIN & KONSISTENSI ┣━━◈
   ╲━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╱

• Jangan memaksakan survival, kerapuhan, cedera, atau konsekuensi ekstrem tanpa dasar mekanik maupun kejadian yang jelas.
• Profil harus konsisten dengan profil gameplay terakhir dan kejadian setelahnya.
• Setiap perubahan status harus memiliki penyebab yang dapat ditelusuri.
• Jangan mengarang fakta, formula, kemampuan, saldo, kurs, transaksi, atau informasi tersembunyi.
• Ikuti modul resmi sesuai cakupannya dan gunakan prosedur konflik jika ditemukan ketidaksesuaian.
• Jangan mengedit registry atau snapshot karakter selama gameplay tanpa permintaan eksplisit pemilik repository.
• Jangan mengklaim perubahan data telah tersimpan ke repository jika proses penulisan gagal atau tidak dilakukan.

✦ Enjoy your convo, player! ✦

Aksiku : --
```

## Aturan Penerapan

- **Urutan respons:** timestamp → narasi → LEDGER LOG dan penegasan hanya jika ada perubahan uang/item/aset → `PROFIL KARAKTER` → `INV & KEUANGAN` → `TEKNIK & TUJUAN` → `CATATAN PEMAIN & KONSISTENSI` → catatan kecil → `Aksiku : --`.
- **Timestamp dan Era:** ikuti `gameplay/TIME_AND_ACTION_RULES.md`. Pada sesi baru, tentukan era sesuai prosedur dan jangan tinggalkan placeholder setelah bootstrap selesai. Pada sesi berlanjut, teruskan timestamp terakhir yang sah.
- **Ledger:** setiap transaksi atau perubahan uang, item, atau aset yang benar-benar terjadi harus dicatat setelah narasi dan sebelum profil. Jangan tampilkan ledger jika tidak ada perubahan; jangan menyatakan berhasil sebelum hasil diverifikasi. Detail mengikuti `core/10_ECONOMY_SYSTEM.md`.
- **Profil:** pertahankan nama field dan urutan persis seperti di atas. Empat seksi profil tetap terpisah. Gunakan `templates/CHARACTER_PROFILE_TEMPLATE.md` untuk arti field dan state; file itu bukan format visual alternatif.
- **Spirit Ring Absorption:** `Day left` hanya menghitung jeda minimum antarpenyerapan Spirit Ring yang berhasil, bukan timer breakthrough Kultivasi. Ikuti `templates/CHARACTER_PROFILE_TEMPLATE.md`, `gameplay/TIME_AND_ACTION_RULES.md` §7, dan interval resmi di `bestiary/SPIRIT_BEAST_RULES.md`. `0 Day left` bukan jaminan penyerapan berhasil.
- **HP dan cedera:** gunakan `core/HP_SYSTEM.md` serta `core/INJURY_SYSTEM.md` sebagai dua state terpisah.
- **Satiety:** tampilkan `Satiety: nilai/100` dan hitung hanya menurut `core/HUNGER_AND_METABOLISM.md`; tidur malam yang dilindungi mengunci nilai ini.
- **Currency:** pertahankan format lima denominasi `xc | xs | xg | zj | az` dan saldo yang dapat diverifikasi dari snapshot/profil aktif beserta transaksi sah. Jangan menebak atau mengundi ulang saldo.
- **NO STEP:** jangan menambahkan menu pilihan atau opsi bernomor. Akhiri adegan pada situasi terbuka agar player menentukan tindakan.
- **Sumber gagal:** jangan mengaku membaca file yang tidak dapat diakses. Sebutkan keterbatasan secara singkat dan jangan menyelesaikan bagian yang bergantung pada aturan yang hilang.
