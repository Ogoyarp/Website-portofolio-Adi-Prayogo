# Website portofolio Adi Prayogo

Portofolio pribadi — Adi Prayogo (OGOYARP). Web builder & automation.

**Live:** https://ogoy.web.id

## Struktur

```
├── index.html        # Portofolio: repositori GitHub + project berjalan
├── articles.html     # Daftar artikel
├── tentang.html      # Tentang
├── articles/         # Artikel lengkap + _template.html untuk artikel baru
└── assets/           # Avatar, foto profil
```

## Teknologi

- HTML + CSS + vanilla JS (satu file per halaman, tanpa framework)
- Dark/light theme + toggle bahasa ID/EN (localStorage)
- Hosting: Cloudflare Pages, domain custom ogoy.web.id (CNAME proxied)

## Deploy

Deploy manual dari clone lokal:

```bash
export CLOUDFLARE_API_TOKEN=<token dengan izin Pages Edit>
wrangler pages deploy . --project-name=ogoyarp --branch=main --commit-dirty=true
```

## Menambah artikel

1. Copy `articles/_template.html` → `articles/<slug>.html`
2. Isi judul, deskripsi, meta, dan sampul (taruh gambar di `articles/img/`)
3. Tambah kartu baru di `articles.html` (pattern `.article` yang sudah ada)

## Update konten

Edit `index.html` / `articles.html` langsung, lalu deploy ulang. Versi lokal clone: `/root/ogoyarp-site` di VPS.
