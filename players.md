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
- Status `Spirit Ring Absorption` dan format tunggal `status | Day left` wajib mengikuti pemetaan di `templates/CHARACTER_PROFILE_TEMPLATE.md`. Sebelum penyerapan pertama berhasil, gunakan `??? Day left` dengan status sesuai tahap: Mortal tanpa Awakening aktif = `not eligible yet | ??? Day left`; Awakening aktif = `pending | ??? Day left`; setelah Awakening selesai = `eligible | ??? Day left` hanya jika syarat ring pertama terpenuhi, selain itu `not eligible yet | ??? Day left`. Untuk Spirit Realm 1–8, syarat yang belum lengkap memakai `not eligible yet | N Day left`; seluruh syarat karakter/proses terpenuhi memakai `eligible | 0 Day left`. Spirit Realm 9 selalu `max | ∞ Day left`. Setelah penyerapan berhasil, langsung mulai cooldown menuju ring berikutnya. `Belum ditetapkan Day left` hanya untuk state lama yang diketahui pernah menyerap ring tetapi data waktu/riwayatnya tidak cukup untuk menghitung cooldown. Ini pengecualian hitung-mundur dan bukan timer umum breakthrough kultivasi. Field numerik lain yang belum tercatat diisi `0`, kecuali HP sesi baru mengikuti maksimum pada `core/HP_SYSTEM.md`. Field nonnumerik lain yang belum ditetapkan ditulis `Belum ditetapkan` atau `Tidak ada` jika memang diketahui tidak ada.
- Jika snapshot karakter dibuat sebelum field Satiety ditambahkan, tetapkan estimasi awal GM yang wajar pada bootstrap sesi baru berdasarkan `core/HUNGER_AND_METABOLISM.md`. Jangan otomatis memakai 0 atau 100, jangan mengarang sifat tubuh untuk membenarkan angka, dan jangan mengubah file karakter individual hanya untuk mengisi state sesi. Setelah nilai awal ditetapkan di profil sesi, semua perubahan berikutnya harus mengikuti modul mekanik tersebut.

## Daftar Karakter

Saat bootstrap karakter terdaftar, gunakan tautan **RAW** untuk mengambil isi file individual secara langsung dan utuh. Jangan mengandalkan cuplikan tabel atau hanya membaca bagian profil ringkas.

| Karakter | File karakter | Status |
|---|---|---|
| Yuha | [players/Yuha.md](players/Yuha.md) · [RAW](https://raw.githubusercontent.com/Antarezka/merzkava-universe/refs/heads/main/players/Yuha.md?v=2) | Snapshot awal terdaftar |
| Nafila | [players/Nafila.md](players/Nafila.md) · [RAW](https://raw.githubusercontent.com/Antarezka/merzkava-universe/refs/heads/main/players/Nafila.md?v=2) | Snapshot awal terdaftar |

## Menambahkan Karakter
Buat satu file individual di folder `players/` untuk setiap karakter, lalu tambahkan satu entri ke tabel di atas. Gunakan `templates/CHARACTER_PROFILE_TEMPLATE.md` untuk definisi field dan `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` untuk format gameplay.
