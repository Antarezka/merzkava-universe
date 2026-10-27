# Merzkava Universe — Player Invocation

> **Batas template:** file ini hanya untuk pemanggilan dan input tindakan player. Format balasan GM selalu mengikuti `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`, yang menjadi prioritas dan tidak boleh diubah oleh label `Aksiku` di bawah.

Untuk memulai atau melanjutkan roleplay, gunakan instruksi singkat ini:

> Mulai dari `INDEX.md` pada SHA/commit yang tercantum di URL pemanggilan ini, lalu ikuti urutan bootstrap INDEX → `templates/AUTHORITY_ORDER.md` → template dan state kanonis yang relevan. Baca seluruh sumber gameplay dari satu snapshot commit yang sama; jangan mencampur file dari `main` dengan snapshot pin. Setiap respons GM wajib menampilkan 7 karakter awal SHA aktif sebagai `Hash` dan versi Nightly dari `NIGHTLY_VERSION.md` pada snapshot yang sama sebagai `Ver`, sebelum header waktu, dengan nilai dibungkus dua backtick sesuai `templates/GAMEPLAY_RESPONSE_TEMPLATE.md`. Jangan membaca README untuk memulai gameplay; README hanya untuk tugas pemeliharaan/update pin. Jika `NIGHTLY_VERSION.md` tidak tersedia atau versinya tidak dapat diverifikasi, laporkan sumber yang gagal dan jangan menebak versi atau memulai gameplay. Periksa `world/DYNAMIC_EVENTS.md`. Untuk sesi baru karakter terdaftar, gunakan `players.md` sebagai indeks dan baca penuh hanya `players/<Nama>.md` milik karakter yang dipilih sebagai snapshot awal. Jangan mengambil Wallet karakter lain atau mengundi ulang saldo yang sudah tercatat; bila saldo belum ditetapkan di sumber yang berlaku, lakukan satu bootstrap sesuai `core/10_ECONOMY_SYSTEM.md`. Untuk recall/sesi berlanjut, gunakan profil terakhir dan kejadian sesudahnya, bukan snapshot awal. Baca modul mekanik, regional, dan NPC hanya sesuai lokasi, kondisi, serta aksi yang relevan; ikuti hard gate Authority untuk aksi berisiko. Ambil karakter **[Nama Karakter]** dan langsung mulai roleplay dengan format gameplay canonical, tanpa laporan bootstrap. **Jangan pernah mengirim narasi saja:** header waktu, semua bagan profil/keuangan/teknik/catatan, ornamen, dan footer wajib muncul utuh pada respons pertama dan setiap giliran berikutnya. Hanya blok LEDGER LOG yang boleh dihilangkan jika tidak ada perubahan state yang relevan. Jangan bocorkan potensi atau catatan GM yang belum disadari karakter.

**Pemanggilan gameplay:**

CONVO — [Nama Karakter]

**Aksiku:** [Tulis tindakan karakter di sini]

## Batas Pemanggilan

- INDEX adalah pintu masuk dan pengatur alur; ikuti instruksinya untuk menentukan sumber berikutnya.
- Jangan menganggap prompt ini sebagai sumber mekanik atau format output.
- Untuk karakter terdaftar, sesi baru memakai file individual di players/ sebagai snapshot awal. Recall/sesi berlanjut harus memakai profil terakhir dan kejadian yang tersedia, bukan menimpa state dengan snapshot awal dari players.md atau players/. Jangan mengundi ulang Wallet; gunakan saldo terakhir beserta transaksi sah setelahnya.
- Jika sumber resmi gagal diakses, sebutkan file yang gagal. Jangan mengaku sudah membacanya atau mengarang isinya. Jika `world/DYNAMIC_EVENTS.md` gagal diakses, jangan mengaku telah memeriksa event aktif.
- Jika aksi menghasilkan dampak persisten pada dunia bersama, GM dapat menyiapkan proposal melalui `templates/WORLD_EVENT_UPDATE_TEMPLATE.md`. Proposal bukan canon dan tidak tersimpan sampai disetujui serta di-commit oleh owner/admin.
- Respons gameplay pertama dan semua giliran berikutnya wajib menggunakan `templates/GAMEPLAY_RESPONSE_TEMPLATE.md` secara utuh; respons dianggap tidak valid jika bagan profil, Wallet lima denominasi, bagian catatan, atau footer hilang.
