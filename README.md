# M. Ilham Ramadani — SEO Content Portfolio

Website portofolio statis yang siap dipublikasikan melalui GitHub Pages.

## Isi paket

- `index.html` — halaman utama, styling, navigasi, studi kasus, filter, pencarian, dan tampilan artikel.
- `articles.js` — database artikel publik dan data 11 studi kasus pilihan.
- `assets/` — foto profil, thumbnail artikel yang tersedia, dan screenshot bukti studi kasus.

## Data yang saat ini ditampilkan

- 99 URL artikel publik unik: 47 CatchPlay dan 52 Seva.id.
- 11 studi kasus pilihan berdasarkan PDF portofolio terbaru.
- 20 catatan keyword tercatat pada posisi #1–#3 di workbook tracking. Tanggal pengukuran tidak dicantumkan, jadi angka ini ditampilkan sebagai catatan historis, bukan ranking real-time.
- Hanya tautan artikel publik yang masuk Article Library. Link dokumen internal, baris tanpa URL publik, tautan duplikat, dan halaman video non-artikel tidak ditampilkan.

Sebagian artikel sudah memiliki thumbnail yang diambil dari materi portofolio. Kartu artikel lainnya memakai cover grafis berdasarkan brand dan kategori sampai thumbnail spesifik tersedia.

## Cara memperbarui daftar artikel

1. Buka `articles.js`.
2. Cari bagian `window.PORTFOLIO_ARTICLES = [`.
3. Tambahkan objek artikel baru di dalam array. Contoh:

```js
{
  "brand": "Seva.id",
  "industry": "Finance & Automotive",
  "category": "Financial Guide",
  "title": "Judul artikel yang sudah terbit",
  "keyword": "keyword utama",
  "publicUrl": "https://www.seva.id/blog/contoh-artikel",
  "status": "Published",
  "thumbnail": "assets/thumbnails/seva/contoh-artikel.jpg",
  "id": "seva-contoh-artikel"
}
```

4. Pastikan `publicUrl` mengarah ke halaman artikel publik, bukan Google Docs atau dokumen internal.
5. Gunakan brand persis `CatchPlay` atau `Seva.id` agar filter bekerja.
6. Jika menambahkan thumbnail, simpan gambarnya di folder brand yang sesuai, lalu samakan path di properti `thumbnail`. Jika tidak ada thumbnail, hapus properti `thumbnail`; website akan menampilkan cover grafis otomatis.
7. Pastikan setiap artikel memiliki `id` unik dan URL publik tidak duplikat.
8. Simpan perubahan dan commit ke GitHub. GitHub Pages akan menerbitkan perubahan dari branch yang dipilih.

## Cara memasang di GitHub Pages

1. Upload `index.html`, `articles.js`, dan seluruh folder `assets/` ke root repository.
2. Di GitHub buka **Settings → Pages**.
3. Pilih **Deploy from a branch**, pilih branch (umumnya `main`) dan folder `/(root)`, lalu simpan.

Jangan mengunggah `index.html` saja: gambar dan database artikel dibutuhkan agar website tampil lengkap.

## Catatan kredibilitas

Posisi ranking pada studi kasus ditranskripsikan dari PDF yang diberikan. Karena tanggal pengecekan tidak tercantum, posisi tersebut merupakan catatan pada dokumen sumber dan dapat berubah. Jangan mempresentasikannya sebagai ranking Google terkini atau jaminan hasil.
