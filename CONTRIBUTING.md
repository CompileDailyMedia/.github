# Panduan Kontribusi

Terima kasih sudah tertarik membantu CompileDaily. Panduan ini berlaku untuk semua repository di
organisasi CompileDailyMedia, kecuali repo tersebut punya `CONTRIBUTING.md` sendiri.

## Sebelum Mulai

- Baca [Kode Etik](CODE_OF_CONDUCT.md).
- Cek issue yang sudah ada supaya tidak dobel.
- Untuk perubahan besar, buka issue dulu untuk diskusi sebelum menulis kode.
- Jangan laporkan celah keamanan lewat issue publik — ikuti [SECURITY.md](SECURITY.md).

## Melaporkan Kesalahan Artikel

Kesalahan faktual di artikel compiledaily.net **bukan** bug kode. Kirim lewat email ke
[support@compiledaily.net](mailto:support@compiledaily.net) dengan menyertakan tautan artikel dan
detail kesalahannya, atau gunakan template issue "Koreksi Artikel".

## Alur Kontribusi Kode

1. Fork repository, lalu buat branch dari `main`:
   ```bash
   git checkout -b fix/komentar-tidak-tersimpan
   ```
2. Kerjakan perubahan dan sertakan test bila menyentuh logic.
3. Pastikan test dan code style lolos (untuk repo Laravel):
   ```bash
   php artisan test
   ./vendor/bin/pint
   ```
4. Commit dengan pesan yang jelas dan spesifik.
5. Buka pull request ke `main` dan isi template yang tersedia.

## Konvensi

- PHP mengikuti **PSR-12**, dirapikan dengan Laravel Pint.
- Validasi input lewat **Form Request**, otorisasi lewat **Policy**.
- Logic bisnis di **Service class** atau **Model**, controller tetap tipis.
- Nama branch: `feat/...`, `fix/...`, `docs/...`, `refactor/...`.
- Jangan commit `.env`, kredensial, kunci OAuth, atau data pengguna.

### Antarmuka

Tampilan CompileDaily memakai gaya editorial minimalis:

- Font: sans-serif geometris untuk body, serif editorial untuk judul, monospace untuk metadata.
- Palet warm monochrome dengan aksen pastel untuk badge kategori.
- Tanpa gradient, tanpa shadow tebal, tanpa emoji di markup maupun teks.
- Animasi hanya lewat `transform` dan `opacity`.

## Pull Request

- Satu PR untuk satu perubahan yang fokus.
- Jelaskan apa yang berubah dan alasannya.
- Lampirkan screenshot untuk perubahan tampilan.
- PR akan ditinjau maintainer sebelum digabung.
