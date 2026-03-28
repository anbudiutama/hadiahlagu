# Hadiah Lagu — hadiahlagu.com

Landing page + formulir brief untuk jasa pembuatan lagu pernikahan custom.

**Tech:** Static HTML/CSS/JS → GitHub → Vercel  
**Domain:** hadiahlagu.com  
**WA:** +6285224660075 (Sandra)  
**Harga:** Rp 199.000 / lagu  
**Delivery:** Maksimal 1x24 jam

## Struktur File

```
hadiahlagu/
├── index.html        ← Landing page (hadiahlagu.com)
├── formulir.html     ← Form brief (hadiahlagu.com/formulir)
├── og-image.png      ← OG image / hero background
├── og-image2.png     ← Foto CTA section
├── audio/            ← Sample lagu MP3
├── sitemap.xml       ← Sitemap untuk Google
├── robots.txt        ← Instruksi crawler
├── vercel.json       ← Config Vercel
├── PANDUAN-SEO.md    ← Panduan SEO & Google Search Console
├── .gitignore
└── README.md
```

## Cara Deploy (Step-by-Step)

### 1. Buat Repository GitHub

1. Buka https://github.com/new
2. Repository name: `hadiahlagu`
3. Visibility: **Private** (atau Public)
4. Klik **Create repository**
5. Di komputer lokal, buka terminal:

```bash
cd /path/ke/folder/hadiahlagu
git init
git add .
git commit -m "Initial commit - Hadiah Lagu website"
git branch -M main
git remote add origin https://github.com/USERNAME/hadiahlagu.git
git push -u origin main
```

Ganti `USERNAME` dengan username GitHub Anda.

### 2. Deploy ke Vercel

1. Buka https://vercel.com dan login dengan akun GitHub
2. Klik **"Add New" → "Project"**
3. Pilih repository **hadiahlagu** → klik **Import**
4. Settings (biarkan default):
   - Framework Preset: **Other**
   - Root Directory: `./`
   - Build Command: *(kosongkan)*
   - Output Directory: `./`
5. Klik **Deploy**
6. Tunggu ~30 detik, site live di `hadiahlagu.vercel.app`

### 3. Setup Custom Domain hadiahlagu.com

**Di Vercel:**
1. Buka project → **Settings** → **Domains**
2. Ketik `hadiahlagu.com` → klik **Add**
3. Vercel akan tampilkan DNS records yang perlu ditambahkan

**Di domain registrar (tempat beli domain):**

Tambahkan DNS records berikut:

| Type  | Name  | Value                    |
|-------|-------|--------------------------|
| A     | @     | 76.76.21.21              |
| CNAME | www   | cname.vercel-dns.com     |

4. Tunggu propagasi DNS (5 menit – 48 jam, biasanya <1 jam)
5. Vercel otomatis sediakan SSL certificate (HTTPS)

### 4. Verifikasi

Setelah domain aktif, cek:
- ✅ https://hadiahlagu.com → Landing page
- ✅ https://hadiahlagu.com/formulir → Form brief
- ✅ Klik "Isi Formulir & Pesan Sekarang" → ke /formulir
- ✅ Klik "← Kembali ke Beranda" → ke /
- ✅ Submit form → buka WhatsApp Sandra
- ✅ https://www.hadiahlagu.com → redirect ke hadiahlagu.com

## Update Konten

1. Edit file di lokal atau langsung di GitHub
2. Push ke `main`:
```bash
git add .
git commit -m "Update konten"
git push
```
3. Vercel auto-deploy dalam ~15 detik

## Catatan

- **Supabase** tidak diperlukan untuk versi ini (static site, no database). Jika nanti butuh database (menyimpan orders, tracking leads), bisa ditambahkan Supabase.
- **og-image.png**: Buat gambar 1200x630px untuk preview saat link di-share di WA/IG/FB, lalu taruh di root folder.
