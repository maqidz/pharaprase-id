# pharaprase-id

Skill agen AI (*agent skill*) berbahasa Indonesia untuk **mengaudit, memparafrasa, dan menulis ulang teks** agar bebas dari pola tulisan AI (*AI-isms*), kalke terjemahan Inggris–Indonesia, nominalisasi bertumpuk, dan frasa klise — tanpa mengorbankan makna asli, fakta, maupun suara penulis.

Diadaptasi dari filosofi, kontrak penyuntingan, sistem *severity tier*, profil konteks, dan profil suara [conorbronsdon/avoid-ai-writing](https://github.com/conorbronsdon/avoid-ai-writing), lalu dirancang khusus untuk struktur dan kaidah **Bahasa Indonesia**.

> **Prinsip Utama:** Ini adalah alat peningkatan kualitas tulisan, bukan alat vonis detektor AI dan bukan alat untuk menghindari kebijakan pengungkapan penggunaan AI.

---

## Fitur Utama

- **Tiga Mode Operasi:**
  - `rewrite` *(default)* — Audit → Parafrasa/Tulis Ulang (maks. 2 putaran) → Ringkasan Perubahan → Verifikasi terstruktur.
  - `detect` — Audit saja tanpa mengubah teks (dikelompokkan dalam **P0 / P1 / P2** + penilaian *clear problem* vs. *judgment call*).
  - `edit` — Sunting file prosa/Markdown secara langsung (*in-place*) dengan perubahan minimal sambil melindungi kode, tabel, kutipan, dan frontmatter.
- **Katalog Pola Khusus Bahasa Indonesia:** Tier kata 1A/1B/2/3, kalke terjemahan Inggris–Indonesia (*"adalah penting untuk dicatat"*, *"memainkan peran kunci"*, *"...yang mana..."*), nominalisasi bertumpuk, paralelisme negatif, dan ekor partisipial.
- **Kontrak Penyuntingan & Guardrail Anti-Slop:** Menjaga kesetiaan fakta (*source fidelity*), konten terlindungi (*protected content*), aturan *no-op* (0 suntingan bila teks sudah bersih), dan melarang penyuntikan "gaya humanizer palsu" (*staccato* paksaan, *"Jujur saja,"*, pengalaman fiktif).
- **7 Profil Konteks (`--context`):** `linkedin`, `blog`, `technical-blog`, `email-bisnis`, `docs`, `casual`, dan `akademik` lengkap dengan matriks toleransi.
- **5 Profil Suara (`--voice`):** `santai`, `profesional`, `teknis`, `hangat`, dan `lugas`, plus kalibrasi dari contoh tulisan penulis.

---

## Struktur Repositori

```text
pharaprase-id/
├── SKILL.md                      # Instruksi utama (kontrak penyuntingan, mode, P0–P2, guardrail, output)
├── README.md                     # Dokumentasi & panduan pemasangan
├── LICENSE                       # Lisensi MIT
└── references/
    └── pola-bahasa-id.md         # Tier kata ID, kalke terjemahan, matriks toleransi konteks, & profil suara
```

---

## Cara Memasang

### Antigravity (Global Skill)
```bash
git clone https://github.com/maqidz/pharaprase-id.git ~/.gemini/config/skills/pharaprase-id
```

### Claude Code / Cursor / Codex
```bash
git clone https://github.com/maqidz/pharaprase-id.git ~/.claude/skills/pharaprase-id
```

---

## Contoh Penggunaan

- *"Parafrasa teks ini dengan skill `pharaprase-id` supaya lebih alami untuk blog."*
- *"Audit saja pola AI di artikel ini (`--mode detect --context linkedin`), jangan ubah teksnya."*
- *"Rapikan file `draft-artikel.md` langsung dengan gaya `--voice lugas --context technical-blog`."*
- *"Tulis ulang email ini dengan `--context email-bisnis --voice profesional`."*
