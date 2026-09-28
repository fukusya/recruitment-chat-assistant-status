# Recruitment Chat Assistant — Status Progres

Halaman status non-teknis untuk [Recruitment Chat Assistant](https://github.com/fukusya/recruitment-chat-assistant).
Situs statis, tanpa build step, tanpa koneksi ke database bisnis — hanya baca
`status.json` yang disalin dari repo aplikasi tiap checkpoint.

**Isi:** peta modul (V1 s/d V2-3), status tiap hasil (belum/sedang
dikerjakan/kode+test lokal/terbukti live/dipakai sehari-hari), keputusan yang
masih terbuka, dan langkah berikutnya. Tidak ada data kandidat, token, atau
kredensial.

## Cara update

1. Dari repo `recruitment-assistant`: edit `status.json`, lalu jalankan
   `node scripts/render-status-block.mjs` (ini juga memperbarui blok status di
   `HANDOFF_CONTEXT.md`).
2. Salin `status.json` yang sudah diperbarui ke repo ini (folder ini).
3. `git add status.json && git commit -m "..." && git push`.

Situs otomatis ter-update lewat GitHub Pages beberapa saat setelah push.

## Kenapa terpisah dari repo aplikasi

Supaya publikasi status tidak pernah butuh akses ke kode/data aplikasi utama,
dan supaya update rutin halaman ini tidak ikut ter-gate oleh proses approval
push kode aplikasi (lihat `AGENTS.md` di repo aplikasi).
