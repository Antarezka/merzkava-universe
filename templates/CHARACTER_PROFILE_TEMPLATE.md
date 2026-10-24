# Xuanling Realm — Character Profile Template

Gunakan format ini pada setiap balasan gameplay dalam **MODE: NO STEP**. Aturan mekanik terperinci tetap berada di modul sumbernya; template ini hanya menetapkan bentuk profil dan cara membaca state.

```text
🕒 Waktu Xuanling Realm
Tahun: XXXX, [Era sesi] | Musim: [Semi/Panas/Gugur/Dingin] | Tanggal: DD Bulan MM | Hari: [Senin–Minggu] | Cuaca: ... | Jam: HH:MM

Narasi
[Narasi berdasarkan kejadian, pengetahuan karakter, kondisi dunia, dan konsekuensi yang benar-benar terjadi.]

┌── Profil Karakter ──┐
Nama: ...
Usia: ...
Spirit Realm: .../...
Sync progress: ...%/...%
Breakthrough: ... | ... Day left
Martial Soul: ...
Thinker Grade: ...
HP: .../...
Qi: ...
Kondisi Tubuh: ...
Equipment: ...
Inventory: ...
Assets: ...
Currency (xuan/zun): ...xc | ...xs | ...xg | ...zj | ...az
Teknik / Kemampuan: ...
Tujuan Saat Ini: ...
└────────────────────┘
```

## Definisi Field Breakthrough dan Day left

Format profil tetap `Breakthrough: ... | ... Day left`. Field ini wajib dibaca sebagai dua informasi berbeda:

- **Breakthrough:** tahap/status bottleneck karakter saat ini, berdasarkan Realm/Stage, Sync progress terhadap cap kompatibilitas, ketersediaan ring berikutnya, item wajib, jeda minimum, dan seluruh syarat resmi lain. Field ini tidak berarti breakthrough otomatis tersedia.
- **Day left:** jumlah hari kalender dunia yang tersisa sampai jeda minimum antarpenyerapan Spirit Ring berikutnya terpenuhi. Hitung dari timestamp penyerapan Spirit Ring terakhir yang berhasil dan tabel jeda minimum di `bestiary/SPIRIT_BEAST_RULES.md`.
- Gunakan selisih waktu dunia yang tercatat, bukan jumlah giliran atau waktu nyata. Jika sisa durasi positif, bulatkan ke atas menjadi hari agar `0 Day left` hanya muncul ketika jeda minimum benar-benar sudah terpenuhi. Contoh: sisa 1 jam berarti `1 Day left`; sisa 24 jam berarti `1 Day left`; sisa 25 jam berarti `2 Day left`.
- Jika jeda minimum telah terpenuhi, tulis `0 Day left`. Ini hanya menyatakan syarat waktu terpenuhi, bukan bahwa breakthrough atau penyerapan pasti sah/berhasil.
- Jika karakter belum memiliki penyerapan ring sebelumnya yang relevan, atau timestamp/nomor ring tidak diketahui atau bertentangan, gunakan `??? Day left` sampai data dapat dipastikan. Jangan mengasumsikan nilai nol.
- Hitung ulang hanya ketika ada timestamp dunia atau informasi riwayat yang sah untuk memperbarui perhitungan. Pergantian giliran saja tidak mengurangi nilai.

## Aturan Pengisian

- Pertahankan nama dan urutan field di atas. Jangan menambah field terpisah untuk **Spirit Rings** atau **Law**; jumlah ring mengikuti Realm, sedangkan rincian ring yang diperoleh masuk ke **Teknik / Kemampuan** atau deskripsi Martial Soul.
- **Waktu:** gunakan `gameplay/TIME_AND_ACTION_RULES.md`. Jangan membuat timestamp baru secara acak.
- **Field mekanik:** gunakan sumber utama yang terdaftar di `INDEX.md` untuk Realm, Sync progress, Breakthrough, Martial Soul, Thinker Grade, HP, Qi, waktu, dan Currency. Template ini tidak mendefinisikan ulang rumus mekanik.
- **State berjalan:** gunakan profil gameplay terakhir ditambah kejadian yang benar-benar terjadi. Jangan menganggap HP penuh, mengisi ulang sumber daya, mengubah saldo, atau menghapus konsekuensi tanpa sebab yang sah.
- **Data awal:** estimasi praktis hanya boleh digunakan jika wajar dan harus diberi label estimasi GM. Jangan mengarang rahasia besar, garis keturunan, artefak langka, atau teknik formal.
- Gunakan `???` untuk fakta yang belum diketahui atau tidak dapat ditetapkan secara bertanggung jawab. Bedakan pengetahuan karakter dari informasi khusus GM.
- Profil adalah snapshot setelah giliran tersebut, bukan pengganti narasi kejadian atau riwayat transaksi.
