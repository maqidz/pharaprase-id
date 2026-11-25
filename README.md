# pharaprase-id

Skill agen AI (*agent skill*) khusus **parafrasa, audit, dan tulis ulang naskah akademik berbahasa Indonesia** untuk menghilangkan pola tulisan AI (*AI-isms*), kalke terjemahan Inggris–Indonesia, nominalisasi bertumpuk, dan klaim berlebihan — sambil menjaga makna asli, angka, sitasi, rumus, kaidah **EYD V / KBBI**, dan suara ilmiah penulis.

Menggabungkan disiplin kontrak penyuntingan, sistem *severity tier* (P0–P2), tiga mode operasi, dan guardrail anti-slop dari [conorbronsdon/avoid-ai-writing](https://github.com/conorbronsdon/avoid-ai-writing) yang dirancang khusus untuk **konteks akademik Indonesia**.

> **Prinsip Utama:** Skill ini adalah alat peningkatan kualitas dan kejelasan tulisan akademik, bukan vonis detektor AI dan bukan alat untuk menghindari pengungkapan penggunaan AI maupun plagiarisme.

---

## Fitur Utama

- **Tiga Mode Operasi (`--mode`):**
  - `rewrite` *(default)* — Audit → Parafrasa/Tulis Ulang (maks. 2 putaran) → Ringkasan Perubahan → Verifikasi terstruktur.
  - `detect` — Audit saja tanpa mengubah naskah (dikelompokkan dalam **P0 / P1 / P2** + penilaian *clear problem* vs. *judgment call*).
  - `edit` — Sunting file naskah (`.md`, `.tex`, `.txt`) secara langsung (*in-place*) dengan perubahan minimal sambil melindungi sitasi, rumus, tabel, kode, dan frontmatter.
- **Kontrak Penyuntingan Akademik & Guardrail Anti-Slop:** Menjaga integritas angka, *p-value*, sitasi, dan rumus; menyisipkan `[PENULIS: ...]` jika metrik hilang; aturan *no-op* (0 suntingan jika sudah bersih); dan melarang penyuntikan gaya humanizer palsu.
- **5 Profil Konteks Akademik (`--context`):**
  - `jurnal` *(default — Sinta 1–6 / Scopus)*
  - `skripsi-tesis` *(skripsi, tesis, disertasi)*
  - `prosiding` *(makalah konferensi)*
  - `rebuttal` *(tanggapan reviewer)*
  - `proposal-hibah` *(BIMA Kemdiktisaintek, RIIM BRIN, LPDP Rispro)*
- **5 Profil Suara (`--voice`, berbahasa Inggris):**
  - `formal` — Baku EYD V, objektif, impersonal
  - `concise` — Ringkas, padat, hemat kata
  - `technical` — Presisi istilah teknis & struktur metode
  - `analytical` — Kuat di sintesis literatur & pembahasan kritis
  - `diplomatic` — Sopan, objektif, konstruktif (ideal untuk *rebuttal*)

---

## Struktur Repositori

```text
pharaprase-id/
├── SKILL.md                      # Instruksi utama (kontrak akademik, mode, P0–P2, guardrail, output)
├── README.md                     # Dokumentasi & panduan pemasangan
├── LICENSE                       # Lisensi MIT
└── references/
    └── pola-bahasa-id.md         # Tier kata akademik ID, kalke terjemahan, EYD V, matriks konteks, & voice profiles
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

- *"Parafrasa bagian Pendahuluan skripsi ini dengan skill `pharaprase-id` (`--context skripsi-tesis --voice formal`)."*
- *"Audit saja abstrak artikel jurnal ini (`--mode detect --context jurnal`), jangan ubah teksnya."*
- *"Rapikan `bab3-metode.tex` langsung dengan `--mode edit --context jurnal --voice technical`."*
- *"Tulis ulang tanggapan reviewer ini dengan `--context rebuttal --voice diplomatic`."*
- *"Padatkan paragraf pembahasan ini dengan `--voice concise` atau `--voice analytical`."*
