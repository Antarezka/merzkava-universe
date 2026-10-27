# Merzkava Universe — Player Character Registry

File ini adalah **indeks karakter terdaftar**, bukan tempat menyimpan perkembangan gameplay atau profil lengkap seluruh karakter.

## Aturan Registry

- Untuk sesi baru karakter terdaftar, baca file individual yang sesuai secara utuh dari `ACTIVE_SHA` yang sudah dikunci melalui `INDEX.md`.
- File registry dan file karakter individual adalah snapshot awal statis, bukan save gameplay aktif. Jangan menimpa sesi berlanjut dengan snapshot awal atau mengedit file pemain saat gameplay tanpa permintaan eksplisit pemilik repository.
- Pertahankan latar karakter yang tercatat. Jangan mengarang rahasia inti, garis keturunan, Martial Soul, teknik formal, artefak langka, atau fakta canon yang belum didukung.
- Definisi field/default profil dan status `Spirit Ring Absorption` hanya dari `templates/CHARACTER_PROFILE_TEMPLATE.md`; aturan saldo, transaksi, dan bootstrap Wallet hanya dari `core/10_ECONOMY_SYSTEM.md` serta prosedur state di `templates/AUTHORITY_ORDER.md`.
- Jika data awal belum lengkap, tandai estimasi GM sebagai estimasi, bukan canon. Nilai Satiety awal untuk snapshot lama yang belum memiliki field tersebut mengikuti `core/HUNGER_AND_METABOLISM.md` dan template profil; jangan mengubah file karakter hanya untuk mengisi state sesi.
- Untuk sesi berlanjut/recall, gunakan profil gameplay terakhir dan kejadian setelahnya. Jangan mengundi ulang Wallet yang sudah tercatat atau mengarang transaksi lampau.

## Daftar Karakter

Saat bootstrap karakter terdaftar, baca isi file individual secara utuh dari `ACTIVE_SHA` yang sudah dikunci. Tautan relatif di bawah hanya untuk navigasi; jangan mengikuti URL dinamis `refs/heads/main` untuk state gameplay yang sudah dipin. Jangan mengandalkan cuplikan tabel atau hanya membaca bagian profil ringkas.

| Karakter | File karakter | Status |
|---|---|---|
| Yuha | [players/Yuha.md](players/Yuha.md) | Snapshot awal terdaftar |
| Nafila | [players/Nafila.md](players/Nafila.md) | Snapshot awal terdaftar |

## Menambahkan Karakter
Buat satu file individual di folder `players/` untuk setiap karakter, lalu tambahkan satu entri ke tabel di atas. Gunakan `templates/CHARACTER_PROFILE_TEMPLATE.md` untuk definisi field dan `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` untuk format gameplay.
