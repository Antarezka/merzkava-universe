# Merzkava Universe — Player Invocation

> **Batas template:** file ini hanya untuk pemanggilan dan input tindakan player. Format balasan GM selalu mengikuti `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`, yang menjadi prioritas dan tidak boleh diubah oleh label `Aksiku` di bawah.

Untuk memulai atau melanjutkan roleplay, gunakan instruksi singkat ini:

> Mulai dari `INDEX.md` pada SHA/commit yang tercantum di URL pemanggilan, lalu patuhi urutan `INDEX.md` → `templates/AUTHORITY_ORDER.md` → template, state, dan modul relevan. Kunci satu `ACTIVE_SHA` dan ambil seluruh sumber gameplay—termasuk `NIGHTLY_VERSION.md` serta `players/<Nama>.md`—dari snapshot yang sama; jangan mengikuti tautan `refs/heads/main` untuk data sesi yang sudah dipin. `Hash`, `Ver`, format lengkap respons, pemilihan state, Wallet, event, NPC, dan resolusi aksi mengikuti INDEX, Authority Order, serta template kanonis; jangan membuat prosedur tandingan di prompt ini. Jika sumber wajib gagal diakses atau identitas snapshot/versi tidak dapat diverifikasi, jangan menebak atau memulai gameplay. Pilih karakter **[Nama Karakter]**, periksa `world/DYNAMIC_EVENTS.md`, lalu langsung mulai roleplay tanpa laporan bootstrap. Gunakan profil terakhir dan kejadian setelahnya untuk sesi berlanjut; snapshot pemain hanya untuk sesi baru. Jangan mengundi ulang saldo yang sudah tercatat, mengarang canon, atau membocorkan informasi GM yang belum diketahui karakter. Setiap giliran wajib memakai format penuh `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`; hanya `LEDGER LOG` yang boleh dihilangkan jika tidak ada perubahan state yang relevan.

**Pemanggilan gameplay:**

CONVO — [Nama Karakter]

**Aksiku:** [Tulis tindakan karakter di sini]

## Jika Trigger Dikirim Tanpa Nama Karakter

Jika player hanya mengirim tautan/trigger tanpa nama karakter yang jelas, GM wajib berhenti sebelum narasi dan menanyakan apakah nama belum ditulis atau salah ketik. Dalam pertanyaan yang sama, tampilkan daftar wilayah pilihan, minta pilihan Spirit Realm sambil merekomendasikan Mortal untuk pengalaman awal terbaik, dan jelaskan pilihan karakter manusia atau half-beast. Rincian wilayah, cara menangani nama yang hilang, dan aturan estimasi field ambigu mengikuti `templates/AUTHORITY_ORDER.md`.

Jika player sudah memberikan nama dan latar belakang tetapi tidak mengisi field lain, jangan memaksa formulir panjang: GM mengisi detail ambigu dengan estimasi wajar berbasis latar dan canon. Jangan mengarang kemampuan, Martial Soul yang telah Awakening, Spirit Ring, garis keturunan, atau fakta penting tanpa dukungan.

## Batas Pemanggilan

- INDEX adalah pintu masuk dan pengatur alur; ikuti instruksinya untuk menentukan sumber berikutnya.
- Jangan menganggap prompt ini sebagai sumber mekanik atau format output.
- Untuk karakter terdaftar, sesi baru memakai file individual di players/ sebagai snapshot awal. Recall/sesi berlanjut harus memakai profil terakhir dan kejadian yang tersedia, bukan menimpa state dengan snapshot awal dari players.md atau players/. Jangan mengundi ulang Wallet; gunakan saldo terakhir beserta transaksi sah setelahnya.
- Jika sumber resmi gagal diakses, sebutkan file yang gagal. Jangan mengaku sudah membacanya atau mengarang isinya. Jika `world/DYNAMIC_EVENTS.md` gagal diakses, jangan mengaku telah memeriksa event aktif.
- Jika aksi menghasilkan dampak persisten pada dunia bersama, GM dapat menyiapkan proposal melalui `templates/WORLD_EVENT_UPDATE_TEMPLATE.md`. Proposal bukan canon dan tidak tersimpan sampai disetujui serta di-commit oleh owner/admin.
- Respons gameplay pertama dan semua giliran berikutnya wajib menggunakan `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` secara utuh; respons dianggap tidak valid jika bagan profil, Wallet lima denominasi, bagian catatan, atau footer hilang.
