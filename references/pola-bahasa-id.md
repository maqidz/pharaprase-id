# Katalog Pola Bahasa Indonesia, Profil Konteks & Profil Suara

Referensi lengkap untuk skill `pharaprase-id`. Baca dan terapkan aturan serta
pengecualiannya sesuai profil konteks dan profil suara yang aktif.

---

## 1. Tier Kata & Frasa Bahasa Indonesia

### Tier 1A — Penanda Frekuensi AI (Ganti Secara Default)
Kecuali dipakai dalam makna teknis yang ketat, ganti kata-kata berikut:

| Ganti | Alternatif Alami |
| :--- | :--- |
| *menyelami / mendalami secara mendalam* | *membahas, memeriksa, meninjau* |
| *menggarisbawahi / menyoroti* (berlebihan) | *menunjukkan, menegaskan, memperlihatkan* |
| *lanskap* (metaforis: *lanskap digital/bisnis*) | *pasar, industri, ekosistem, bidang* |
| *permadani / jalinan kompleks* (*tapestry*) | *gabungan, rangkaian, struktur* |
| *bukti nyata* (*testament to*) | *menunjukkan bahwa, membuktikan* |
| *ranah* (berlebihan) | *bidang, sektor, area* |
| *sinergi* (klise korporat/AI) | *kerja sama, kolaborasi, keterpaduan* |
| *holistik* (tanpa definisi) | *menyeluruh* (sebutkan cakupannya) |
| *komprehensif* (tanpa ruang lingkup) | sebutkan jumlah/cakupan spesifik |
| *mulus* (*seamless*) | *lancar, otomatis, tanpa hambatan [spesifik]* |
| *krusial / vital / pivotal* (berlebihan) | *penting, utama, menentukan* (atau tunjukkan dampaknya) |
| *transformatif / revolusioner / game-changer* | sebutkan perubahan konkretnya |
| *bernuansa* (*nuanced*) | *rinci, berlapis, tidak hitam-putih* |
| *multifaset / intrikat* | *beragam, rumit, memiliki beberapa sisi* |

### Tier 1B — Perbaikan Kejelasan (Saran Gaya, Bukan Bukti Kepenulisan AI)
- *memanfaatkan* (berulang) → *menggunakan, memakai*
- *melakukan implementasi / pelaksanaan pengujian* → *menerapkan / menguji*
- *dalam rangka untuk / guna untuk* → *untuk*
- *dikarenakan oleh fakta bahwa* → *karena*
- *memberikan kontribusi terhadap peningkatan* → *meningkatkan*

### Tier 2 — Tandai Jika Muncul ≥2 Kali dalam Satu Paragraf
*optimal/mengoptimalkan, efektif/efektivitas, inovatif, strategis, dinamis,
berkelanjutan, adaptif, kolaboratif, terintegrasi, akselerasi, ekosistem,
momentum, katalisator, pilar, fondasi*.

*(Satu kemunculan wajar tidak perlu ditandai; tumpukan ≥2 kata dalam satu
paragraf membuat prosa terdengar seperti brosur AI.)*

### Tier 3 — Frasa Klise (Tandai Jika Berulang ≥2× atau Mengelompok ≥3 Frasa)
- *"Di era digitalisasi / globalisasi / AI saat ini..."*
- *"Dalam dunia yang terus berubah dengan cepat..."*
- *"Tidak dapat dipungkiri bahwa..."*
- *"Pada akhirnya, keberhasilan bergantung pada..."*
- *"Satu hal yang jelas..."*
- *"Di sinilah [X] hadir sebagai solusi..."*
- *"Menjembatani kesenjangan antara teori dan praktik..."*
- *"Membuka pintu menuju peluang baru..."*

---

## 2. Kalke Terjemahan Inggris → Indonesia

Pola sintaksis terjemahan kaku yang paling sering muncul di teks AI Indonesia:

| Kalke (Hindari) | Bahasa Indonesia Alami |
| :--- | :--- |
| *Adalah penting untuk dicatat bahwa...* | *Perlu dicatat bahwa...* atau langsung tulis intinya |
| *Memainkan peran kunci / penting dalam...* | *Berperan dalam...* / *Memengaruhi...* |
| *...yang mana...* (kalke *which*) | *...yang...* atau pecah menjadi dua kalimat |
| *...di mana...* (bukan penunjuk tempat, kalke *where*) | *...ketika...*, *...pada kondisi...*, *...yang menunjukkan...* |
| *Berdasarkan fakta bahwa...* | *Karena...* / *Mengingat...* |
| *Ketika datang ke [X]...* (*when it comes to*) | *Terkait [X]...* / *Untuk urusan [X]...* |
| *Tidak hanya X, tetapi juga Y* / *Bukan sekadar X, melainkan Y* | Nyatakan langsung kedua poin tanpa bingkai dramatis |
| *..., yang menyoroti pentingnya...* (ekor partisipial `-ing`) | Potong ekornya atau jadikan kalimat tersendiri |
| *Memiliki potensi untuk dapat...* | *Berpotensi...* / *Dapat...* |

---

## 3. Pola Struktural & Retorika AI

- **Nominalisasi bertumpuk:** Mengubah terlalu banyak kata kerja menjadi kata benda berimbuhan *pe-...-an* (*"Pelaksanaan pengoptimalan pengelolaan..."* → *"Pengelolaan dioptimalkan..."*).
- **Penghindaran kopula:** Memakai *berfungsi sebagai, bertindak sebagai, hadir sebagai* ketika cukup menulis *adalah* atau kata kerja langsung.
- **Synonym cycling:** Menyebut objek yang sama dengan 4 nama berbeda dalam satu paragraf (*"sistem ini... platform tersebut... solusi inovatif ini... ekosistem digital tersebut"*). Gunakan istilah konsisten.
- **Treadmill effect (kepadatan informasi rendah):** Paragraf panjang yang hanya mengulang kalimat pertama dengan kata berbeda tanpa menambah fakta baru.
- **Uji acak paragraf (*paragraph-reshuffle test*):** Jika urutan paragraf bisa ditukar tanpa merusak alur logika, artinya teks masih terlalu generik dan kurang transisi argumen yang nyata.
- **Pengecualian *self-reference*:** Jika teks memang sedang membahas contoh tulisan AI (misal artikel edukasi atau dokumentasi skill), kutipan contoh tidak boleh ditandai.

---

## 4. Profil Konteks (`--context`)

Jika pengguna tidak menyebut konteks, simpulkan dari sinyal teks (panjang,
sapaan, blok kode, sitasi, tagar).

| Profil | Deskripsi Singkat |
| :--- | :--- |
| `linkedin` | Unggahan media sosial profesional; ringkas, visual rapi, *hook* jelas. |
| `blog` | Default. Artikel panjang atau esai umum; seluruh aturan berlaku penuh. |
| `technical-blog` | Artikel teknis dengan kode, arsitektur, API; istilah teknis dilindungi. |
| `email-bisnis` | Email eksekutif, klien, atau investor; sangat ketat terhadap bahasa promosi & inflasi. |
| `docs` | Dokumentasi, README, panduan; utamakan kejelasan & langkah konkret. |
| `casual` | Pesan Slack/WhatsApp kerja, catatan internal; hanya tangkap P0/masalah berat. |
| `akademik` | Makalah, skripsi/tesis, jurnal; jaga EYD V/KBBI, *hedging* berbasis bukti, dan sitasi. |

### Matriks Toleransi

| Aturan | linkedin | blog | technical-blog | email-bisnis | docs | casual | akademik |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Em-dash (`—`) | longgar (≤2) | ketat | ketat | ketat | longgar | skip | ketat |
| Bold berlebihan | longgar | ketat | ketat | ketat | longgar | skip | ketat |
| Daftar poin | skip | ketat | longgar | ketat | skip | skip | ketat |
| Hedging | ketat | ketat | longgar | ketat | longgar | skip | longgar* |
| Daftar kata Tier 1A | ketat | ketat | parsial** | ketat | longgar | P0 saja | ketat |
| Bahasa promosi | longgar | ketat | ketat | **ekstra ketat** | ketat | skip | **ekstra ketat** |
| Inflasi signifikansi | ketat | ketat | ketat | **ekstra ketat** | longgar | skip | **ekstra ketat** |
| Transisi mekanis | skip | ketat | ketat | ketat | longgar | skip | ketat |
| Tagar berlebih | ketat | ketat | ketat | **ekstra ketat** | skip | skip | skip |

*\*Pada `akademik`, hedging berbasis bukti (`mengindikasikan`, `sejalan dengan`) dipertahankan; tumpukan hedging kosong (`mungkin berpotensi dapat`) tetap dihapus.*
*\*\*Pada `technical-blog`/`docs`, istilah teknis bermakna spesifik (`robust`, `ekosistem`, `seamless failover`, `test harness`) tidak ditandai.*

---

## 5. Profil Suara (`--voice`)

Profil suara bersifat **opsional** dan independen dari profil konteks (misal:
`--context blog --voice lugas`). Jika tidak disebutkan, pertahankan register
asli teks. Seluruh profil suara tetap tunduk pada guardrail *Jangan Pernah
Menyuntikkan Ini*.

- **`santai` (`casual`):** Kalimat mengalir, kosakata sehari-hari yang wajar tanpa memaksa slang berlebihan, tetap mempertahankan istilah yang dibutuhkan pembaca. Hapus basa-basi korporat (*"perlu digarisbawahi bahwa"*).
- **`profesional` (`professional`):** Kalimat aktif saat pelaku penting, klaim konkret sesuai sumber, permintaan/tindakan (*call to action*) jelas, buang *hedging* kosong sambil menjaga ketidakpastian yang nyata.
- **`teknis` (`technical`):** Kopula lugas (*"X adalah Y"*), pisahkan ide kompleks agar mudah dipindai, kalimat imperatif untuk langkah panduan, jaga presisi istilah teknis dan tabel/daftar.
- **`hangat` (`warm`):** Sapaan langsung yang wajar (*Anda* jika sumber sudah menyapa pembaca), tempo tenang, hapus empati artifisial (*"Saya sepenuhnya memahami betapa menantangnya..."*) dan penguat kosong.
- **`lugas` (`blunt`):** Langsung ke inti klaim di kalimat pertama, buang pembuka bertele-tele, hindari *em-dash* dan *rule of three* kosong, tetap jaga batas kepastian/syarat dari sumber.

**Kalibrasi dari contoh tulisan penulis:** Jika pengguna memberikan contoh
tulisan sendiri (*"sesuaikan dengan gaya tulisan saya ini"*), tiru rata-rata
panjang kalimat, pilihan kata ganti (*saya / kami / kita / penulis*), dan cara
membuka paragrafnya — tanpa "menaikkan" level kosakata secara paksa.
