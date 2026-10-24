# Merzkava Universe — Player Character Registry

File ini adalah **indeks karakter terdaftar**, bukan tempat menyimpan perkembangan gameplay atau profil lengkap seluruh karakter.

## Aturan Registry
- Untuk karakter terdaftar yang memulai sesi baru, baca file karakter individual yang ditautkan di bawah sebagai snapshot awal.
- Jangan menimpa profil atau riwayat sesi yang sedang berjalan dengan snapshot awal.
- Perubahan state setelah gameplay dimulai hanya berasal dari profil terakhir dan kejadian yang tercatat di percakapan.
- File registry dan file karakter individual adalah data awal statis. Jangan mengeditnya selama gameplay tanpa permintaan eksplisit pemilik repository.
- Pertahankan latar belakang orisinal karakter. Jangan mengarang rahasia inti, garis keturunan, artefak langka, atau teknik formal tanpa dasar.
- Untuk karakter yang belum memiliki data praktis, estimasi awal yang wajar harus ditandai sebagai estimasi GM dan tidak boleh disamarkan sebagai canon.
- **Saldo awal bootstrap:** jika karakter terdaftar belum memiliki saldo eksplisit, GM menetapkan satu saldo awal melalui undian bootstrap satu kali, lalu menuliskannya secara konkret di profil sesi pertama dan memperlakukannya sebagai saldo awal tetap. Undian tidak boleh didasarkan pada pekerjaan, Assets, atau penghasilan masa lalu; jangan mengarang transaksi lampau dan jangan mengundi ulang pada giliran berikutnya. Jika snapshot sudah mencatat saldo, gunakan nilai tersebut tanpa mengubahnya.
- Aturan placeholder profil: `???` hanya untuk identitas karakter yang benar-benar tidak dikenal atau nama Martial Soul yang belum diketahui. Field numerik yang belum tercatat diisi `0`, kecuali HP sesi baru mengikuti maksimum pada `core/HP_SYSTEM.md`; `Day left` hanya digunakan untuk jeda minimum antarpenyerapan Spirit Ring; jika riwayat/waktu penyerapan tidak tersedia, tulis `Belum ditetapkan`. Ini pengecualian hitung-mundur dan bukan timer umum breakthrough kultivasi. Field nonnumerik lain yang belum ditetapkan ditulis `Belum ditetapkan` atau `Tidak ada` jika memang diketahui tidak ada.
- Jika snapshot karakter dibuat sebelum field Satiety ditambahkan, jangan menganggap nilainya otomatis 100. Tetapkan nilai awal secara wajar sebagai estimasi GM pada sesi baru, lalu gunakan `core/HUNGER_AND_METABOLISM.md`; jangan mengubah file karakter individual hanya untuk mengisi state sesi.

## Daftar Karakter

Saat bootstrap karakter terdaftar, gunakan tautan **RAW** untuk mengambil isi file individual secara langsung dan utuh. Jangan mengandalkan cuplikan tabel atau hanya membaca bagian profil ringkas.

| Karakter | File karakter | Status |
|---|---|---|
| Yuha | [players/Yuha.md](players/Yuha.md) · [RAW](https://raw.githubusercontent.com/Antarezka/merzkava-universe/refs/heads/main/players/Yuha.md?v=1) | Snapshot awal terdaftar |

## Menambahkan Karakter
Buat satu file individual di folder `players/` untuk setiap karakter, lalu tambahkan satu entri ke tabel di atas. Gunakan `templates/CHARACTER_PROFILE_TEMPLATE.md` untuk definisi field dan `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` untuk format gameplay.