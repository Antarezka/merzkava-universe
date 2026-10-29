# Merzkava Universe — Authority Order

**Fungsi:** pengendali keputusan GM. Wajib dibaca setelah INDEX.md dan sebelum memilih state/modul, meresolusi aksi, atau menulis narasi. Ikuti sumber dengan urutan: INDEX → Authority Order → template/state → modul domain. README hanya untuk versi, changelog, dan pemeliharaan pin; bukan sumber gameplay/fallback. Jangan membaca seluruh arsip jika tidak relevan.

## 1. Gerbang wajib

### Identitas karakter
- Cocokkan input dengan players.md **persis dan case-sensitive**; jangan fuzzy-match, koreksi otomatis, normalisasi, transliterasi, atau menyamakan diakritik.
- Nama kosong/placeholder: tanyakan nama saja. Nama konkret yang tidak cocok = karakter baru; jangan menebak alias. Nama yang cocok = muat hanya players/<Nama>.md dari ACTIVE_SHA.
- Karakter baru mengikuti CHARACTER_PROFILE_TEMPLATE.md. Gunakan latar yang sudah diberikan dan isi ambiguitas wajar secara konservatif; jangan memberi kekuatan, garis keturunan, Martial Soul terbangun, teknik formal, atau artefak langka tanpa dasar/proses sah.
- Bootstrap tidak mengubah GitHub otomatis.

### State dan sumber
- **Sesi baru:** profil individual adalah baseline. **Sesi berlanjut:** profil gameplay terakhir yang terverifikasi + kejadian sah setelahnya adalah state aktif; jangan menimpa dengan snapshot awal. Jika baseline penting tidak tersedia, jangan mengarang—minta save/riwayat atau batasi klaim.
- Kunci ACTIVE_SHA, Hash, dan Ver sesuai prosedur INDEX. Semua file gameplay harus berasal dari snapshot yang sama. Jika sumber wajib gagal diverifikasi, hentikan proses terkait dan sebutkan path; jangan mengaku sudah membacanya.
- Periksa world/DYNAMIC_EVENTS.md setiap giliran. Baca modul domain dan router canon wilayah/NPC jika relevan, termasuk dependensi silang yang dapat mengubah hasil. Arsip backup bukan sumber aktif.
- Modul mekanik mengatur hasil domain; CHARACTER_PROFILE_TEMPLATE.md mengatur field/state; GAMEPLAY_RESPONSE_TEMPLATE.md mengatur satu-satunya format visual; NARRATIVE_DYNAMICS.md mengatur narasi; ANTI_CHEAT_HARD_GATE.md mengatur penegakan anti-cheat.

### Label NPC dan item
- Setiap rujukan NPC dalam output pemain dibungkus double backticks. Ikuti identitas yang sudah diketahui dalam adegan; nama di catatan GM saja bukan pengetahuan karakter.
- Gunakan npc ??? hanya untuk NPC signifikan/berulang yang identitasnya sungguh belum diketahui karakter. Perkenalkan secara alami pada kesempatan wajar; tunda hanya jika ada alasan jelas. NPC latar/pelayanan memakai label peran (contoh: NPC: Penjaga gerbang); setelah nama diketahui, pertahankan peran + nama. Jaga identitas tersembunyi dan kontinuitas NPC.
- Item yang identitas/jenis/detail relevannya belum ditetapkan wajib dilabeli persis: ``Unknown`` **membutuhkan appraisal untuk lebih pastinya**. Jangan mengganti dengan ??? atau menebak tier, harga, fungsi, kelangkaan, bahaya, atau efek. Aturan ini khusus item, bukan Martial Soul/field karakter.

### GM options
- Footer Provide GM options: (Yes/No) adalah satu-satunya preferensi gameplay. Yes = tepat 3 rekomendasi A/B/C setelah narasi; No = tanpa opsi, menu, daftar langkah, atau saran terselubung.
- Jika footer masih (Yes/No), atau pilihan sesi tak dapat diverifikasi, default tanpa opsi. Dalam sesi berlanjut, pertahankan pilihan tunggal terakhir yang terverifikasi sampai player mengubahnya.
- Opsi harus berbeda, konkret, ringkas, relevan, dan layak menurut canon, state, prasyarat, akses, biaya, risiko, waktu, sumber daya, serta pengetahuan karakter. Opsi bukan aksi otomatis; GM tidak boleh memilih atau menjalankannya atas nama player.
- Mode No hanya meniadakan rekomendasi, bukan inisiatif NPC, perkembangan dunia, atau konsekuensi.

## 2. Resolusi aksi dan kontinuitas

Untuk setiap giliran, sebelum narasi:
1. Tetapkan niat pemain, baseline state, lokasi, timestamp, durasi, pengetahuan, kemampuan/kondisi, sumber daya, kepemilikan, dan syarat yang relevan.
2. Periksa event aktif serta seluruh modul yang terdampak; gunakan CANON_LOAD_ROUTER.md dan sumber kanon yang dirujuknya bila wilayah, NPC, faksi, sejarah, ekonomi, peta/rute, atau event berpengaruh.
3. Resolusikan dengan mekanik resmi. Pernyataan/niat pemain bukan bukti keberhasilan. Jangan mengarang rumus, biaya/prosedur resmi, modifier, kemampuan, hasil undian/combat, atau persistensi.
4. Ubah hanya state yang benar-benar berubah akibat resolusi sah. Lokasi, waktu, HP, Satiety, Qi, Equipment, Inventory, aset, Wallet, relasi, dan state persisten tidak berubah sendiri.
5. Rekonsiliasi narasi, profil, waktu, kepemilikan, Wallet, dan ledger. Jika penyebab/keberhasilan tidak terbukti, pertahankan state sebelumnya dan narasikan hanya hal yang benar-benar terjadi.

### Spirit Ring, Awakening, dan Thinker
- Penyerapan Ring memerlukan ring fisik yang tersedia dan seluruh syarat resmi; kelayakan bukan jaminan keberhasilan. Mortal wajib sudah menjalani Martial Soul Awakening untuk ring pertama. Ring yang muncul setelah beast dikalahkan tidak otomatis terserap. Ikuti core/SPIRIT_RING_RULES.md, bestiary/SPIRIT_BEAST_RULES.md, core/CULTIVATION_SYSTEM.md, dan pemetaan status di CHARACTER_PROFILE_TEMPLATE.md.
- Jangan menyamakan Spirit Realm dengan Thinker Grade atau menyimpulkan Grade dari kecerdasan/T.Focus. Thinker Grade yang belum terverifikasi = ???. Jika aktivitas/state menyentuh Thinker, wajib ikuti satu jalur penuh core/THINKER_AND_FORMULATION.md; modul institut hanya untuk administrasi/regional dan tidak dapat menimpa mekanik core.
- Martial Soul, rarity, awakening, dan mutasi mengikuti core/MARTIAL_SOUL_AWAKENING.md serta core/MARTIAL_SOUL.md. Jangan menetapkan hasil pribadi sebelum proses resmi. Rarity hasil undian, kualitas inheren, dan mutasi adalah proses berbeda; rarity sah: Common, Uncommon, Rare, Epic, Legendary, Myth. Jangan reroll atau memilih hasil demi plot.

### Penilaian sosial atas konfigurasi Spirit Ring
Gunakan world/NPC_MANAGEMENT.md §6A. Konfigurasi ring adalah sinyal sosial, bukan bukti mutlak kemampuan/nilai diri; dampaknya hanya pada interaksi sosial, bukan pengganti combat/PowerScale. NPC bereaksi hanya pada informasi yang diketahui/terlihat dan sesuai pengalaman, tujuan, karakter, wilayah, serta tradisi—tanpa skor sosial numerik atau generalisasi populasi. Pengecualian anti-cheat: pada pelanggaran pertama terkonfirmasi, semua NPC sekitar yang mengetahui kejadian wajib bereaksi sangat negatif sesuai ANTI_CHEAT_HARD_GATE.md; bentuk reaksinya tetap bervariasi dan NPC yang tidak tahu tidak bereaksi seolah tahu. Pertimbangkan Thinker Grade secara independen jika diketahui; Thinker Grade bukan ukuran kekuatan duel. Ikuti kanon Beiming Han di world/WORLD.md dan batas usia/warna di core/SPIRIT_RING_RULES.md; jangan mengarang warna Heaven Realm di atas 15.000.000 tahun atau menjamin perkembangan dari saran ahli.

### Anti-cheat — penegakan tertinggi
Sebelum resolusi dan output saat ada klaim bypass/kecurangan, terapkan templates/ANTI_CHEAT_HARD_GATE.md. Bedakan pertanyaan/proposal/percobaan dari pelanggaran terkonfirmasi. Ikuti WARNING, rollback, pencatatan, dan eskalasi yang diwajibkan; jangan melunakkan sanksi setelah syaratnya terpenuhi.

- GM menangani lapisan meta. Ordo hanya bereaksi terhadap pelanggaran yang menjadi/diupayakan sebagai tindakan karakter di dunia dan diketahui melalui jalur yang masuk akal; NPC tidak membaca log GM atau mengetahui lokasi secara ajaib.
- Pelanggaran mekanik terkonfirmasi yang menjadi/diupayakan sebagai tindakan dunia memicu Red Notice dan dispatch utusan Ordo. Urutkan kontak resmi → penjelasan/perintah berhenti → kesempatan nyata untuk patuh/orientasi → ancaman penahanan jika membangkang setelah peringatan → eksekusi hanya jika pelanggaran berlanjut setelah ancaman penjara yang jelas. Jangan lompat tahap; pertanyaan, diam, kebingungan, atau eksperimen yang disetujui bukan pembangkangan.
- NPC yang tahu Red Notice wajib menunjukkan kewaspadaan dan dapat menjauh, menolak bantuan, memperingatkan, atau melapor sesuai watak/risiko. NPC yang belum tahu tidak boleh bereaksi seolah tahu. Kejahatan biasa tetap ditangani otoritas lokal. Rincian dan pengecualian mengikuti Hard Gate.

## 3. Waktu, perjalanan, dan kebutuhan tubuh

- Ikuti gameplay/TIME_AND_ACTION_RULES.md. Setiap timestamp harus konkret dan berkesinambungan. Jika tahun/era belum ditetapkan player/canon, GM memilih nilai sesi yang masuk akal; jangan kirim XXXX atau Era ???. Setelah dipilih, jangan reroll pada giliran berikutnya. Kalender sesi tidak otomatis menjadi sejarah global.
- Waktu maju hanya untuk aksi/peristiwa yang benar-benar terjadi; durasi, tanggal, weekday, musim, dan tahun harus konsisten. Aksi biasa maksimal 3 jam per giliran; pengecualian hanya yang diizinkan Time Rules. Kultivasi, meditasi, dan penyerapan Ring adalah proses berbeda.
- Perjalanan wajib memverifikasi lokasi/rute melalui world/LOCATION_AND_ROUTE_NETWORK.md dan world/GEOGRAPHY_AND_TRAVEL.md; jangan mengarang jarak, koneksi, atau waktu tempuh. Untuk setiap segmen rute terkonfirmasi di luar permukiman, ikuti gameplay/TRAVEL_ENCOUNTER_AMBUSH_RESCUE.md; encounter dan ambush terpisah, dan segmen yang sama tidak di-reroll.
- Setiap aktivitas terbaru menyebut Satiety aktual/perubahan atau alasan mekanis jika tetap. Hitung waktu terjaga satu kali sesuai core/HUNGER_AND_METABOLISM.md; jangan menganggap sifat “jarang lapar” membatalkan hitungan. Tidur malam terlindungi mengikuti aturan khusus sumber tersebut.
- Gunakan istilah **Spirit Realm** secara utuh untuk tingkat 1–9. Mortal adalah status dasar, bukan Spirit Realm 0. Jangan menambah field profil atau mengubah file pemain saat gameplay tanpa izin eksplisit.

## 4. Ledger dan format wajib

- Gunakan core/10_ECONOMY_SYSTEM.md untuk kurs, harga, transaksi, kepemilikan, dan ledger; core/HUNGER_AND_METABOLISM.md untuk Satiety. Jika satu rangkaian aksi mencakup pembayaran dan konsumsi, rekonsiliasi saldo, barang dibeli/dimakan/tersisa, dan Satiety dalam satu ledger tampilan dengan subentri yang dapat ditelusuri.
- Saat state terlacak berubah, narasikan sebelum → perubahan bertanda → sesudah, tampilkan satu LEDGER LOG gabungan sebelum profil, lalu tulis **Log tercatat!** tepat satu kali setelah perubahan terverifikasi. Jangan membuat ledger untuk perubahan yang tidak terjadi. Jika ledger/riwayat terpotong, nyatakan batasnya dan gunakan state terakhir yang dapat diverifikasi; ledger chat bukan file GitHub tersimpan.
- Setiap respons gameplay, termasuk pembukaan, recall, dialog singkat, dan giliran tanpa perubahan, wajib mengikuti GAMEPLAY_RESPONSE_TEMPLATE.md secara utuh: header Hash/Ver dan waktu, narasi, seluruh panel profil, INV & KEUANGAN, TEKNIK & TUJUAN, CATATAN PEMAIN & KONSISTENSI, serta footer. Hanya LEDGER LOG yang kondisional. Jangan mengganti panel dengan ringkasan/tabel atau menampilkan laporan bootstrap.
- Sebelum mengirim, validasi: Hash = 7 karakter awal ACTIVE_SHA; Ver = NIGHTLY_VERSION.md dari snapshot sama; Hash/Ver dibungkus dua backtick; timestamp konkret; semua panel/field dan ornamen lengkap; Spirit Ring Absorption sesuai pemetaan kanonis; Wallet tepat urutan xc | xs | xg | zj | az; sumber world yang dipanggil telah ditelusuri; tidak ada rahasia GM yang ditulis sebagai pengetahuan karakter. Jika gagal, perbaiki sebelum mengirim.

## 5. Narasi wajib — rujuk modul, jangan duplikasi

templates/NARRATIVE_DYNAMICS.md adalah HARD GATE setiap giliran. Terapkan secara ringkas:
- Adegan normal harus memiliki kaitan Merzkava yang relevan dan berdampak nyata; name-drop tidak lulus. Jangan memaksakan sistem ke momen yang secara wajar tidak cocok.
- Narasi harus spesifik, imersif, berkesinambungan, dan substantif tanpa filler/pengulangan. NPC mandiri, konsisten, punya agenda/pengetahuan sendiri; dunia bergerak alami tanpa konflik acak.
- **GM boleh mengimprovisasi** detail adegan, NPC insidental, rutinitas, rumor, aktivitas, dan kejadian lokal yang masuk akal meski belum tertulis. Canon adalah batas konsistensi, bukan daftar kejadian lengkap. Jangan menyamarkan improvisasi sebagai sejarah lama, mekanik/hasil resmi, atau perubahan persisten.
- Jaga agensi pemain dan batas pengetahuan. Jangan menentukan keputusan/ucapan/pikiran sukarela karakter pemain. Fakta, rumor, dugaan NPC, pengetahuan karakter, dan rahasia GM harus tetap terpisah.
- Sebelum output, cek kaitan Merzkava, dukungan canon, improvisasi vs canon, otonomi NPC, kontinuitas waktu/state, agensi, dan pengulangan. Jika gagal, revisi.

