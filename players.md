# Xuanling Realm — Player Character Registry

File ini adalah **indeks karakter terdaftar**, bukan tempat menyimpan perkembangan gameplay atau profil lengkap seluruh karakter.

## Aturan Registry
- Untuk karakter terdaftar yang memulai sesi baru, baca file karakter individual yang ditautkan di bawah sebagai snapshot awal.
- Jangan menimpa profil atau riwayat sesi yang sedang berjalan dengan snapshot awal.
- Perubahan state setelah gameplay dimulai hanya berasal dari profil terakhir dan kejadian yang tercatat di percakapan.
- File registry dan file karakter individual adalah data awal statis. Jangan mengeditnya selama gameplay tanpa permintaan eksplisit pemilik repository.
- Pertahankan latar belakang orisinal karakter. Jangan mengarang rahasia inti, garis keturunan, artefak langka, atau teknik formal tanpa dasar.
- Untuk karakter yang belum memiliki data praktis, estimasi awal yang wajar harus ditandai sebagai estimasi GM dan tidak boleh disamarkan sebagai canon.
- Jika snapshot karakter dibuat sebelum field Satiety ditambahkan, jangan menganggap nilainya otomatis 100. Tetapkan nilai awal secara wajar sebagai estimasi GM pada sesi baru, lalu gunakan `core/HUNGER_AND_METABOLISM.md`; jangan mengubah file karakter individual hanya untuk mengisi state sesi.

## Daftar Karakter

| Karakter | File karakter | Status |
|---|---|---|
| Yuha | [players/Yuha.md](players/Yuha.md) | Snapshot awal terdaftar |

## Menambahkan Karakter
Buat satu file individual di folder `players/` untuk setiap karakter, lalu tambahkan satu entri ke tabel di atas. Gunakan `templates/CHARACTER_PROFILE_TEMPLATE.md` untuk definisi field dan `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` untuk format gameplay.