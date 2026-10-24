# Xuanling Realm

**Eastern Fantasy roleplay world and game mechanics.**

## Mulai di sini

- **[INDEX.md](INDEX.md)** — satu-satunya entry point yang perlu diberikan pemain kepada AI Game Master. Berisi bootstrap, direktori modul, pemicu pemuatan file, dan aturan anti-cheat.
- **[world/WORLD.md](world/WORLD.md)** — sumber utama lore dunia, wilayah, faksi, dan fakta yang sudah ditetapkan. Detail yang ditandai sebagai usulan/rancangan awal masih provisional.
- **[templates/GM_PROMPT.md](templates/GM_PROMPT.md)** — instruksi operasional untuk AI Game Master.
- **[core/CULTIVATION_SYSTEM.md](core/CULTIVATION_SYSTEM.md)** — Realm, Stage, progres, bottleneck, breakthrough, dan slot Spirit Ring.
- **[core/MARTIAL_SOUL.md](core/MARTIAL_SOUL.md)** — aturan dasar Martial Soul dan awakening.
- **[core/SPIRIT_RING_RULES.md](core/SPIRIT_RING_RULES.md)** — usia dan warna ring, penyerapan, sinkronisasi, serta hubungan dengan breakthrough.

## Alur Memulai Roleplay

1. Gunakan [`templates/PLAYER_CONVERSATION_TEMPLATE.md`](templates/PLAYER_CONVERSATION_TEMPLATE.md) sebagai prompt player, lalu jalankan trigger `CONVO` bersama nama karakter. `INDEX.md` tetap menjadi entry point navigasi resmi.
2. Untuk karakter terdaftar, GM membaca `players.md` sebagai **state awal**, lalu memuat template profil dan modul yang relevan.
3. Untuk melanjutkan permainan di percakapan yang sama, GM memakai profil karakter terakhir dan kejadian sesudahnya. Data awal di `players.md` tidak boleh menimpa progres sesi berjalan.
4. Untuk karakter baru yang belum terdaftar, GM memakai template profil dan informasi yang diberikan pemain; detail praktis yang masuk akal boleh ditandai sebagai estimasi GM.
5. Field `Breakthrough` dan `Day left` mengikuti definisi di `templates/CHARACTER_PROFILE_TEMPLATE.md`; `Day left` adalah sisa hari dunia menuju terpenuhinya jeda minimum penyerapan berikutnya, bukan jaminan breakthrough.
6. Respons gameplay pertama langsung dimulai dengan timestamp lengkap, narasi pembuka, dan profil karakter lengkap. MODE: NO STEP berarti tidak ada menu pilihan.
6. Pada setiap giliran gameplay, GM memeriksa ulang INDEX dan instruksi GM, lalu memuat modul yang relevan. Jika file gagal diakses, GM harus menyatakannya dan tidak boleh berpura-pura telah membaca isinya.

Untuk transaksi, kurs, penilaian harga, atau perubahan saldo, GM wajib menggunakan `core/10_ECONOMY_SYSTEM.md` dan mencatat transaksi di narasi/riwayat. Profil karakter mencerminkan saldo setelah transaksi; bootstrap tidak boleh mengubah saldo dengan sendirinya.

## Prinsip proyek

- Jangan mengarang aturan atau mengklaim membaca file yang tidak tersedia.
- Pertahankan konsekuensi, keadaan karakter, dan riwayat permainan.
- Tidak ada plot armor; kematian permanen kecuali pengecualian resmi ditetapkan.
- Bedakan fakta canon, usulan provisional, rumor, dan informasi yang belum diketahui.
- Gunakan modul khusus untuk aturan rinci setelah modul tersebut benar-benar tersedia.

File yang belum ada tetapi disebut di INDEX adalah rencana pengembangan, bukan sumber aturan yang sudah aktif.
