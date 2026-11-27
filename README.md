# Dokumentasi CBT Indolat

Sumber situs dokumentasi CBT Indolat (Mintlify). Setiap push ke branch `main` diterbitkan otomatis.

## Struktur

| Lokasi | Isi |
| --- | --- |
| `docs.json` | Navigasi, bahasa (ID default, EN), warna, dan redirect |
| `*.mdx`, `<folder>/*.mdx` | Halaman bahasa Indonesia |
| `en/` | Terjemahan bahasa Inggris dengan path yang sama |
| `images/<folder>/<halaman>/NN-deskripsi.png` | Screenshot per halaman, diberi nomor sesuai urutan tampil |
| `api/`, `en/api/` | Dokumentasi API |

Folder halaman panduan mengikuti modul di aplikasi:

- `memulai/`: Portal, modul, dan akun admin
- `paket-soal/`, `data-ujian/`, `cbt/`: modul **Platform Ujian (CBT)**
- `data-akun/`, `lainnya/login-peserta`: akun dan login peserta
- `administrasi/`, `lainnya/manajemen-akses-admin`, `lainnya/transaksi-dan-penarikan-saldo`,
  `lainnya/kustomisasi-tampilan-website`: modul **Administrasi Aplikasi**
- `lms/`, `web-builder/`: modul **LMS** dan **Pembuat Website**
- `peserta/`: tab **Panduan Peserta**, panduan untuk peserta ujian di aplikasi peserta

## Pratinjau lokal

```bash
npm i -g mint
mint dev
```

Buka `http://localhost:3000`. Jalankan `mint broken-links` sebelum push.

## Aturan penulisan

- Bahasa Indonesia baku (EYD V dan KBBI), sapaan "Anda", tanpa emoji.
- Nama menu, tombol, dan kolom ditulis **tebal** persis seperti di aplikasi. Jalur menu ditulis lengkap, misalnya
  **Portal** → **Platform Ujian (CBT)** → **Manajemen Ujian** → **Data Ujian**.
- Setiap halaman panduan dibuka dengan paragraf tujuan dan blok `<Info>` berisi lokasi menu.
- Langkah memakai `<Steps>`/`<Step>`, setiap gambar berada di dalam `<Frame>` dengan teks alt yang deskriptif.
- `<Warning>` hanya untuk tindakan yang tidak bisa dibatalkan atau berisiko kehilangan data.
- Setiap perubahan halaman ID wajib diikuti perubahan halaman `en/` yang setara. Tautan internal di halaman EN memakai
  awalan `/en/`.

## Aturan screenshot

- Ambil dari tampilan aplikasi terbaru dengan lebar jendela 1440 px, lalu potong ke area yang relevan.
- Penanda berwarna merah (`#E11D27`): kotak dan panah untuk tombol atau menu yang diklik, lingkaran bernomor bila teks
  berisi daftar bernomor (nomor di gambar sama dengan nomor di teks).
- Gunakan data contoh fiktif (nama Indonesia, email `@contoh.id`), jangan data pelanggan atau orang sungguhan.
- Simpan di `images/<folder>/<halaman>/` dan hapus gambar lama yang tidak dirujuk lagi.
