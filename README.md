# Implementasi Tailwind CSS

Proyek sederhana untuk belajar dan mencoba Tailwind CSS v4 pada halaman HTML statis tanpa React atau framework JavaScript lainnya.

Halaman contoh menampilkan pesan **Hello World!**, deskripsi singkat, dan tombol **Get Started** dengan styling dari utility class Tailwind CSS.

## Teknologi

- HTML5
- Tailwind CSS `4.3.5`
- Tailwind CSS CLI
- npm

## Prasyarat

Pastikan perangkat sudah memiliki:

- Node.js dan npm
- Browser modern

## Instalasi

1. Clone repository:

   ```bash
   git clone https://github.com/Ataya24/Implementasi-tailwind.git
   cd Implementasi-tailwind
   ```

2. Install dependency:

   ```bash
   npm install
   ```

## Menjalankan Proyek

### Build CSS

Generate CSS Tailwind dari `src/input.css` ke `dist/output.css` dengan perintah berikut:

```bash
npx @tailwindcss/cli -i ./src/input.css -o ./dist/output.css
```

Setelah proses selesai, buka `index.html` menggunakan browser.

### Mode watch

Gunakan mode watch selama mengembangkan proyek agar CSS dibuat ulang setiap kali file sumber berubah:

```bash
npx @tailwindcss/cli -i ./src/input.css -o ./dist/output.css --watch
```

Biarkan proses tersebut tetap berjalan, lalu refresh `index.html` setelah melakukan perubahan.

## Struktur Proyek

```text
.
├── index.html          # Halaman utama
├── src/
│   ├── input.css       # Entry point Tailwind CSS
│   └── output.css      # File CSS sumber yang tersedia di proyek
├── dist/
│   └── output.css      # CSS hasil build yang digunakan halaman
├── package.json        # Metadata dan dependency npm
└── package-lock.json   # Versi dependency yang terkunci
```

## Cara Mengubah Tampilan

Edit class Tailwind pada `index.html`, kemudian jalankan kembali perintah build atau gunakan mode `--watch`. Contoh:

```html
<h1 class="text-3xl font-bold underline text-blue-500">
  Hello World!
</h1>
```

File `index.html` memuat CSS hasil build melalui:

```html
<link href="./dist/output.css" rel="stylesheet">
```

## Catatan

- `src/input.css` menggunakan `@import "tailwindcss";` sebagai entry point Tailwind CSS.
- `dist/output.css` harus diperbarui setelah utility class pada HTML berubah.
- Proyek ini belum memiliki automated test atau development server.

## Lisensi

Proyek menggunakan lisensi ISC sesuai konfigurasi pada `package.json`.
