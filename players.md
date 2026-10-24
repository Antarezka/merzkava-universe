# Xuanling Realm — Player Character Registry

File ini adalah **indeks karakter terdaftar**, bukan tempat menyimpan perkembangan gameplay atau profil lengkap seluruh karakter.

## Aturan Registry
- Untuk karakter terdaftar yang memulai sesi baru, baca file karakter individual yang ditautkan di bawah sebagai snapshot awal.
- Jangan menimpa profil atau riwayat sesi yang sedang berjalan dengan snapshot awal.
- Perubahan state setelah gameplay dimulai hanya berasal dari profil terakhir dan kejadian yang tercatat di percakapan.
- File registry dan file karakter individual adalah data awal statis. Jangan mengeditnya selama gameplay tanpa permintaan eksplisit pemilik repository.
- Pertahankan latar belakang orisinal karakter. Jangan mengarang rahasia inti, garis keturunan, artefak langka, atau teknik formal tanpa dasar.
- Untuk karakter yang belum memiliki data praktis, estimasi awal yang wajar harus ditandai sebagai estimasi GM dan tidak boleh disamarkan sebagai canon.

## Daftar Karakter

| Karakter | File karakter | Status |
|---|---|---|
| Yuha | [players/Yuha.md](players/Yuha.md) | Snapshot awal terdaftar |

## Menambahkan Karakter
Buat satu file individual di folder `players/` untuk setiap karakter, lalu tambahkan satu entri ke tabel di atas. Gunakan `templates/CHARACTER_PROFILE_TEMPLATE.md` untuk definisi field dan `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` untuk format gameplay.