# Merzkava Universe — HP System

Status: Mekanik resmi HP.
Cakupan: HP maksimum berdasarkan Spirit Realm dan Stage, format HP, serta pencatatan HP saat ini.

## 1. Prinsip Dasar

- Mortal memiliki HP maksimum **100**.
- Spirit Primordial/Stage 4 (Peak) memiliki HP maksimum **8.950**.
- HP ditulis sebagai **HP saat ini / HP maksimum**, misalnya `HP: 100/100`.
- HP maksimum ditentukan oleh Realm dan Stage pada tabel resmi di bawah.
- HP saat ini berubah hanya karena kejadian gameplay yang sah, misalnya menerima damage atau pemulihan yang memiliki dasar. Naik Realm atau Stage menaikkan batas maksimum sesuai tabel, tetapi **tidak otomatis memulihkan HP saat ini hingga penuh**.
- **Jika HP saat ini mencapai 0, karakter mati.** Kematian bersifat permanen kecuali mekanik resmi yang sudah ditetapkan secara eksplisit menyatakan sebaliknya. HP 0 bukan sekadar pingsan atau kondisi sekarat; jangan mengubahnya menjadi status lain tanpa dasar mekanik resmi.
- **Modul ini belum menetapkan laju numerik pemulihan HP umum.** Istirahat, tidur, makanan, obat, tabib, teknik, atau artefak tidak boleh diberi angka pemulihan HP tanpa aturan atau efek terdokumentasi. GM boleh mencatat pemulihan naratif yang jelas didukung sumber/kejadian, tetapi tidak boleh mengarang angka atau durasi sebagai aturan resmi.
- Progres pemulihan injury di `core/INJURY_SYSTEM.md` hanya memulihkan cedera yang dicatat; progres tersebut tidak mengisi HP. Sebaliknya, HP yang pulih tidak otomatis mengurangi progres injury.
- Jangan menciptakan damage, pemulihan, bonus HP, atau pengecualian yang tidak didukung mekanik resmi.
- Formula ini menentukan HP maksimum, bukan damage, pertahanan, peluang menang, atau kekuatan tempur secara keseluruhan.

## 2. Tabel HP Maksimum

| Spirit Realm | Stage 1 (Early) | Stage 2 (Middle) | Stage 3 (Late) | Stage 4 (Peak) |
|---|---:|---:|---:|---:|
| Mortal | — | — | — | 100 |
| Spirit Initiate | 150 | 200 | 250 | 300 |
| Spirit Adept | 375 | 450 | 525 | 600 |
| Spirit Elder | 700 | 800 | 900 | 1.000 |
| Spirit Monarch | 1.150 | 1.300 | 1.450 | 1.600 |
| Spirit King | 1.825 | 2.050 | 2.275 | 2.500 |
| Spirit Ancestor | 2.800 | 3.100 | 3.400 | 3.700 |
| Spirit Emperor | 4.075 | 4.450 | 4.825 | 5.200 |
| Spirit Sovereign | 5.650 | 6.100 | 6.550 | 7.000 |
| Spirit Primordial | 7.488 | 7.975 | 8.463 | **8.950** |

Mortal bukan salah satu dari sembilan Spirit Realm. Gunakan `Mortal/0` pada profil untuk menandai status mortal tanpa Stage kultivasi.

## 3. Formula Interpolasi Stage

Untuk setiap Realm, gunakan HP Peak Realm itu sebagai batas maksimum (H_max) dan HP Peak Realm sebelumnya sebagai batas dasar (H_prev). Untuk Spirit Initiate, H_prev = 100 (Mortal). Untuk Realm berikutnya, H_prev adalah HP Peak Realm sebelumnya.

Hitung selisih:

`ΔH = H_max − H_prev`

Kemudian:

- Stage 1 / Early: `H_prev + round(ΔH × 0,25)`
- Stage 2 / Middle: `H_prev + round(ΔH × 0,50)`
- Stage 3 / Late: `H_prev + round(ΔH × 0,75)`
- Stage 4 / Peak: `H_max`

Gunakan pembulatan ke bilangan bulat terdekat. Jika hasil tepat berada di antara dua bilangan bulat, bulatkan ke atas. Tabel pada §2 adalah nilai rujukan final; gunakan angka tabel jika ada perbedaan akibat pembulatan.

Batas HP Peak per Realm:
- Mortal: 100
- Spirit Initiate: 300
- Spirit Adept: 600
- Spirit Elder: 1.000
- Spirit Monarch: 1.600
- Spirit King: 2.500
- Spirit Ancestor: 3.700
- Spirit Emperor: 5.200
- Spirit Sovereign: 7.000
- Spirit Primordial: 8.950

## 4. Format dan Validasi Profil

- Format wajib: `HP: saat_ini/maksimum`.
- Jika Realm/Stage diketahui, isi HP maksimum dari tabel.
- **Inisialisasi sesi baru:** jika snapshot karakter tidak mencatat HP saat ini, tetapkan HP awal sama dengan maksimum yang berlaku pada Realm/Stage tersebut. Contoh: Mortal tanpa HP awal tercatat menjadi `HP: 100/100`, bukan `HP: ???/100`.
- **Sesi berjalan:** pertahankan HP saat ini dari profil gameplay terakhir dan terapkan hanya perubahan yang sah. Jika profil sesi berjalan tidak memuat nilai HP saat ini dan tidak ada riwayat untuk memulihkannya, isi `0` sebagai nilai numerik yang belum tersedia; jangan gunakan `???`.
- Jika Realm/Stage belum diketahui, gunakan `HP: 0/0` sampai Realm/Stage dapat ditetapkan. Jangan gunakan `???` untuk nilai HP.
- Jangan memulihkan HP ke penuh pada sesi berjalan tanpa penyebab sah. Pengecualian hanya inisialisasi sesi baru ketika snapshot tidak mencatat HP saat ini: gunakan maksimum yang berlaku sebagai HP awal.
- Nilai HP saat ini tidak boleh melebihi maksimum. Jika riwayat atau input bertentangan, tandai konflik dan jangan diam-diam mengubah HP.
- Saat Realm/Stage berubah, perbarui angka maksimum sesuai tabel, tetapi pertahankan HP saat ini yang tercatat sampai ada perubahan yang sah.

## 5. Konsistensi

- Gunakan `core/CULTIVATION_SYSTEM.md` untuk memastikan Realm dan Stage yang sah.
- Gunakan modul pertarungan resmi jika tersedia untuk menentukan damage, pertahanan, dan hasil pertarungan. Tabel ini sendiri tidak menetapkan angka damage.
- Gunakan `core/INJURY_SYSTEM.md` untuk progres cedera; jangan memakai laju progres injury sebagai laju pemulihan HP.
- Jangan menafsirkan Mortal sebagai bukti bahwa Martial Soul belum awakening.
- Jangan mengubah angka HP maksimum di tabel tanpa revisi canon oleh pemilik repository.
