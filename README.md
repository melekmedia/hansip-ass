# Hansip — Alat Analisis Risiko Komunitas
Alat penilaian risiko keamanan holistik untuk aktivis dan pembela hak asasi manusia di Indonesia. Dikembangkan bersama komunitas Hansip Bokir yang [MelekMedia](https://melekmedia.org) terlibat di dalamnya.

## Fitur

**5 kategori risiko** (v1 & v2): Kekerasan Fisik, Keselamatan Fisik, Keamanan Digital, Jerat Hukum, Psikis — masing-masing berisi 10 item potensi ancaman yang dinilai dari sisi probabilitas dan dampak (skala 1–5).

**v1** — versi awal:
- **3 skenario kegiatan**: Pra Aksi, Aksi Massa, Paska-Aksi — masing-masing dengan profil probabilitas berbeda, bisa dibandingkan langsung

**v2** — versi terbaru:
- Skenario kegiatan digantikan dengan **Kategori Organisasi** (Pendampingan, Advokasi, Peningkatan Kapasitas, Penelitian, Kampanye) — bisa pilih lebih dari satu. Kuesioner tetap menampilkan semua 10 item per kategori, tapi rata-rata skor risiko hanya dihitung dari item yang relevan dengan kategori organisasi yang dipilih
- Daftar 50 item ancaman diperbarui dengan deskripsi yang lebih konkret dan kontekstual untuk kerja lapangan aktivis
- Tab **Ringkasan**: tabel skor + radar chart yang membandingkan kelima aspek risiko satu sama lain

**Fitur bersama (v1 & v2)**:
- **Auto-save** ke localStorage browser
- **Export / Import JSON** untuk backup dan berbagi data antar perangkat
- **Cetak / Export PDF** via browser
- **Offline-ready** — tidak butuh koneksi internet setelah dibuka
- **Ramah mobile** — card layout di layar kecil, touch target 44px

## Cara Kerja

**1. Identitas Pengisi** — isi nama, organisasi, tanggal, dan catatan konteks kegiatan. Di v2, pilih juga **Kategori Organisasi** kalau ingin rata-rata skor difilter sesuai jenis kerja organisasi Anda (boleh dikosongkan).

**2. Penilaian per kategori** — untuk setiap dari 10 item ancaman di 5 kategori, isi dua angka (skala 1–5):
- **Probabilitas**: 1 Sangat Tidak Mungkin → 5 Hampir Pasti
- **Dampak**: 1 Tidak Signifikan → 5 Kritis

**3. Skor & Level** — skor per item = Probabilitas × Dampak (rentang 1–25), dengan level:

| Skor | Level |
|---|---|
| ≥ 15 | 🔴 Tinggi |
| 5–14 | 🟡 Sedang |
| < 5 | 🟢 Rendah |

Skor rata-rata kategori = rata-rata skor seluruh item di kategori itu (di v2, hanya item yang relevan dengan kategori organisasi terpilih yang dihitung — lihat catatan di bawah header setiap kategori).

**4. Tab Ringkasan** — menampilkan tabel skor rata-rata kelima kategori sekaligus radar chart untuk melihat profil risiko secara keseluruhan: aspek mana yang paling menonjol dan perlu jadi prioritas mitigasi.

**5. Simpan hasil** — data tersimpan otomatis di browser (localStorage). Gunakan **Simpan JSON** untuk backup/berbagi antar perangkat, **Muat JSON** untuk memuatnya kembali, dan **Cetak/PDF** untuk laporan cetak.

> ⚠️ Data hanya tersimpan lokal di browser Anda masing-masing — tidak dikirim ke server manapun.

## Cara Pakai
Buka langsung di browser: **[https://melekmedia.github.io/hansip-ass/](https://melekmedia.github.io/hansip-ass/)** (v1)
Untuk v2 ada di link ini: **[https://melekmedia.github.io/hansip-ass/v2/](https://melekmedia.github.io/hansip-ass/v2)**

Atau unduh `index.html` dan buka sebagai file lokal.

## Update & Kontribusi
Setiap push ke branch `main` akan otomatis ter-deploy ke GitHub Pages dalam ~1 menit.

## Lisensi
[Creative Commons Attribution-ShareAlike 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
