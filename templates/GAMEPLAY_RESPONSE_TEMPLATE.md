# Merzkava Universe — Canonical Gameplay Response Template

Status: **Satu-satunya sumber resmi untuk bentuk, urutan, nama field, dan sekat visual setiap balasan gameplay.**

Semua trigger awal (CONVO), recall, dan giliran lanjutan wajib mengikuti template ini. `INDEX.md` mengatur navigasi/bootstrap; `templates/AUTHORITY_ORDER.md` mengatur perilaku GM; `templates/CHARACTER_PROFILE_TEMPLATE.md` mendefinisikan arti field; modul waktu dan mekanik mengatur perhitungan serta konsekuensi. File ini hanya master **format keluaran gameplay**, bukan tempat menyalin instruksi bootstrap.

## Format Wajib

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
[Narasi imersif sesuai kejadian, suasana, dialog, tindakan NPC, pengetahuan karakter, kondisi dunia, dan konsekuensi yang benar-benar terjadi. Setiap aktivitas terbaru wajib menyebutkan Satiety: jika berubah, nyatakan pengurangan/penambahan dan nilai sebelum → sesudah; jika tetap, nyatakan nilai tetap beserta alasannya. Untuk konsumsi, sebut nama item, tier resmi, jumlah, dan efek Satiety yang terverifikasi; jika tier resmi belum tersedia, ikuti `core/TIER_ASSESSMENT_AND_APPRAISAL.md`: gunakan hasil Kantor Appraisal resmi jika tersedia; jika belum, cantumkan `Prediksi GM` beserta skor hanya bila bukti cukup; jika bukti tidak cukup, tulis “Tier belum ditetapkan — appraisal diperlukan”. Jika Satiety, uang, item, equipment, loot, atau aset benar-benar berubah, tampilkan laporan perubahan natural dan akhiri kalimat terkait dengan `Log tercatat!` sebelum ledger. Jangan gunakan penanda jika tidak ada perubahan atau hasil belum terkonfirmasi.]

[Gunakan **satu LEDGER LOG ringkas** untuk semua perubahan dari satu rangkaian aksi—misalnya membeli makanan, membayar, lalu langsung memakannya. Tampilkan hanya baris yang relevan; jangan membuat log terpisah untuk pembayaran, item, dan konsumsi.]

╭─ LEDGER LOG · #[ID]
│ [Waktu] · [Berhasil/Gagal/Dibatalkan]
│ Item: [nama] · Tier [resmi/belum ditetapkan] ×[jumlah] → [Inventory akhir]
│ Uang: [saldo awal] → [−biaya bersih] → [saldo akhir]
│ Satiety: [awal] → [±delta] → [akhir] · [kategori/durasi jika relevan]
╰─

[Jika perlu, ringkas kembalian dalam satu baris: “Bayar [nominal]; harga [nominal]; kembalian [nominal]”. Untuk konsumsi, sebut nama item, tier kanon/appraisal resmi atau prediksi GM berlabel jelas; jika bukti tidak cukup, “Tier belum ditetapkan — appraisal diperlukan”, jumlah, dan efek Satiety aktual. Jika beberapa item/denominasi berubah, ringkas dalam baris terkait tanpa menghilangkan nilai sebelum → perubahan → sesudah. Tulis persis penanda inline-code `Log tercatat!` sekali setelah laporan perubahan terverifikasi. Jangan tampilkan penanda/ledger untuk perubahan yang tidak terjadi.]

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

Tentukan Aksimu : --
```

## Aturan Penerapan

- **Urutan respons:** timestamp → narasi natural dan laporan perubahan → penanda `Log tercatat!` pada kalimat perubahan yang sudah diverifikasi → satu `LEDGER LOG` untuk perubahan Satiety/uang/item/equipment/loot/aset → `PROFIL KARAKTER` → `INV & KEUANGAN` → `TEKNIK & TUJUAN` → `CATATAN PEMAIN & KONSISTENSI` → catatan kecil → `Aksiku : --`. Jangan menampilkan penanda atau ledger jika tidak ada perubahan state relevan. Setiap aktivitas terbaru tetap harus menyebutkan nilai Satiety, termasuk ketika nilainya tetap.
- **Timestamp dan Era:** ikuti `gameplay/TIME_AND_ACTION_RULES.md`. Pada sesi baru, tentukan era sesuai prosedur dan jangan tinggalkan placeholder setelah bootstrap selesai. Pada sesi berlanjut, teruskan timestamp terakhir yang sah.
- **Ledger gabungan ringkas:** untuk satu rangkaian aksi, gabungkan perubahan uang, item, dan Satiety dalam satu laporan dan satu `LEDGER LOG` sebelum profil. Contoh alur: beli makanan → bayar → konsumsi sambil menikmati pemandangan; catat item/tier/jumlah, harga dan saldo akhir, Inventory akhir, serta Satiety sebelum → perubahan → sesudah. Cukup tampilkan baris yang relevan, tanpa mengulang detail panjang. Gunakan `Log tercatat!` sekali setelah perubahan terverifikasi. Detail audit kronologis tetap dipertahankan di ledger sesi; aturan uang/item mengikuti `core/10_ECONOMY_SYSTEM.md` dan Satiety mengikuti `core/HUNGER_AND_METABOLISM.md`.
- **Profil:** pertahankan nama field dan urutan persis seperti di atas. Empat seksi profil tetap terpisah. Gunakan `templates/CHARACTER_PROFILE_TEMPLATE.md` untuk arti field dan state; file itu bukan format visual alternatif.
- **Spirit Ring Absorption:** `Day left` hanya menghitung jeda minimum antarpenyerapan Spirit Ring yang berhasil, bukan timer breakthrough Kultivasi. Ikuti `templates/CHARACTER_PROFILE_TEMPLATE.md`, `gameplay/TIME_AND_ACTION_RULES.md` §7, dan interval resmi di `bestiary/SPIRIT_BEAST_RULES.md`. `0 Day left` bukan jaminan penyerapan berhasil.
- **HP dan cedera:** gunakan `core/HP_SYSTEM.md` serta `core/INJURY_SYSTEM.md` sebagai dua state terpisah.
- **Satiety:** tampilkan `Satiety: nilai/100` dan hitung hanya menurut `core/HUNGER_AND_METABOLISM.md`. Setiap aktivitas terbaru wajib menyebut nilai Satiety; istirahat terjaga memperlambat pengurangan tanpa menambah Satiety, sedangkan tidur malam yang dilindungi mengunci nilai ini.
- **Currency:** pertahankan format lima denominasi `xc | xs | xg | zj | az` dan saldo yang dapat diverifikasi dari snapshot/profil aktif beserta transaksi sah. Jangan menebak atau mengundi ulang saldo.
- Jangan menambahkan menu pilihan atau opsi bernomor. Akhiri adegan pada situasi terbuka agar player menentukan tindakan.
- **Sumber gagal:** jangan mengaku membaca file yang tidak dapat diakses. Sebutkan keterbatasan secara singkat dan jangan menyelesaikan bagian yang bergantung pada aturan yang hilang.
