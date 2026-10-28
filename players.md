# Merzkava Universe — Player Character Registry

File ini adalah **indeks karakter terdaftar**, bukan tempat menyimpan perkembangan gameplay atau profil lengkap seluruh karakter.

## Aturan Registry

- Untuk sesi baru karakter terdaftar, baca file individual yang sesuai secara utuh dari `ACTIVE_SHA` yang sudah dikunci melalui `INDEX.md`.
- File registry dan file karakter individual adalah snapshot awal statis, bukan save gameplay aktif. Jangan menimpa sesi berlanjut dengan snapshot awal atau mengedit file pemain saat gameplay tanpa permintaan eksplisit pemilik repository.
- Pertahankan latar karakter yang tercatat. Jangan mengarang rahasia inti, garis keturunan, Martial Soul, teknik formal, artefak langka, atau fakta canon yang belum didukung.
- Definisi field/default profil, estimasi data ambigu, dan satu-satunya jalur bootstrap/save karakter baru berada di `templates/CHARACTER_PROFILE_TEMPLATE.md`; aturan kurs, harga, dan transaksi berada di `core/10_ECONOMY_SYSTEM.md`. Wallet awal adalah bagian dari proses profil yang sama, bukan jalur save terpisah.
- Untuk karakter baru, pertahankan semua fakta eksplisit; estimasikan field ambigu secara wajar berdasarkan latar. Usia 8–19 tahun adalah rentang acuan fleksibel, bukan batas mutlak. Tentukan Wallet awal dari latar dan kondisi ekonomi, bukan undian acak, lalu simpan dalam file karakter yang sama. Tandai estimasi sebagai estimasi GM, bukan canon pasti.
- Jangan menerapkan bootstrap baru secara retroaktif pada snapshot terdaftar atau fixture pengujian seperti Nafila. Snapshot yang ada tetap tidak berubah kecuali pemilik meminta perubahan eksplisit. Nilai Satiety awal untuk snapshot lama yang belum memiliki field tersebut mengikuti `core/HUNGER_AND_METABOLISM.md` dan template profil; jangan mengubah file karakter hanya untuk mengisi state sesi.
- Untuk sesi berlanjut/recall, gunakan profil gameplay terakhir dan kejadian setelahnya. Jangan mengundi ulang Wallet yang sudah tercatat atau mengarang transaksi lampau.

## Daftar Karakter

Saat bootstrap karakter terdaftar, baca isi file individual secara utuh dari `ACTIVE_SHA` yang sudah dikunci. Tautan relatif di bawah hanya untuk navigasi; jangan mengikuti URL dinamis `refs/heads/main` untuk state gameplay yang sudah dipin. Jangan mengandalkan cuplikan tabel atau hanya membaca bagian profil ringkas.

| Karakter | File karakter | Status |
|---|---|---|
| Yuha | [players/Yuha.md](players/Yuha.md) | Snapshot awal terdaftar |
| Nafila | [players/Nafila.md](players/Nafila.md) | Snapshot awal terdaftar |

## Menambahkan dan Menyimpan Karakter Baru
Ikuti satu jalur saja: gunakan `templates/CHARACTER_PROFILE_TEMPLATE.md` untuk membangun seluruh snapshot karakter, termasuk estimasi field ambigu dan Wallet berbasis latar; gunakan `core/10_ECONOMY_SYSTEM.md` hanya untuk kurs serta aturan ekonomi, bukan untuk bootstrap Wallet terpisah. Pertahankan latar dan fakta eksplisit, tandai estimasi GM, dan jangan mengarang hasil awakening atau kemampuan yang belum diperoleh. Simpan profil lengkap dan Wallet dalam satu file `players/<Nama>.md`, kemudian tambahkan satu entri ke tabel ini. Jangan mengedit snapshot karakter lama atau fixture pengujian saat membuat standar baru. Gunakan `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` untuk format gameplay.
