# Raster Studio Pro

Aplikasi web client-side untuk membuat raster/halftone profesional dari JPG, PNG, WEBP, dan format gambar yang didukung browser.

## Fitur profesional

- AM halftone berbasis DPI/LPI
- CMYK 4-channel dengan preview Composite, C, M, Y, K
- Sudut screen independen C/M/Y/K; preset default C15/M75/Y0/K45
- Dot size dan bentuk dot: Circle, Ellipse, Square, Line
- Grayscale, 1-bit Threshold, Bayer dan Floyd–Steinberg
- Brightness, Contrast, Threshold, Invert
- Ukuran output fisik dalam mm + perhitungan pixel berdasarkan DPI
- Batas maksimum pixel untuk menjaga performa browser
- Background transparan atau warna pilihan
- Warna channel CMYK dapat disesuaikan untuk preview/produksi
- Drag & drop dan multi-file upload
- Undo / Redo hingga 30 perubahan pengaturan
- Zoom preview dan checkerboard transparansi
- Export PNG, JPEG, PDF, dan Vector SVG
- Batch processing ke ZIP PNG
- Tidak mengunggah gambar ke server; pemrosesan dilakukan lokal di browser
- GitHub Actions untuk production build dan GitHub Pages deployment

## Menjalankan lokal

```bash
npm install
npm run dev
```

## Production build

```bash
npm run build
npm run preview
```

## GitHub Pages

Workflow deployment tersedia di `.github/workflows/pages.yml`. Aktifkan **Settings → Pages → Source: GitHub Actions** pada repository bila Pages belum aktif.

## Catatan produksi

SVG menggunakan objek vektor per dot, sehingga file dapat menjadi besar pada gambar beresolusi tinggi atau LPI rendah. Untuk screen printing, gunakan DPI/LPI dan sudut C/M/Y/K sesuai profil mesin, mesh, tinta, dan proses separasi yang digunakan.
