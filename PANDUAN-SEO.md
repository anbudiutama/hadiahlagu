# Panduan SEO & Google Search Console — Hadiah Lagu

## Yang Sudah Terpasang di Website

### 1. Meta Tags (index.html & formulir.html)
- `title` — mengandung keyword utama + harga + brand
- `meta description` — ringkasan persuasif dengan keyword
- `meta keywords` — target keyword lengkap
- `canonical` — mencegah duplicate content
- `robots` — index, follow (kedua halaman)
- Open Graph (og:title, og:description, og:image) — preview di WA/FB/IG
- Twitter Card — preview di Twitter/X

### 2. Structured Data (JSON-LD)
- **LocalBusiness** — agar muncul di Google Maps & knowledge panel
- **Product** — menampilkan harga Rp 199.000 langsung di hasil pencarian
- **FAQPage** — FAQ muncul sebagai rich snippet (dropdown) di Google
- **BreadcrumbList** — navigasi breadcrumb di hasil pencarian

### 3. File Teknis
- `sitemap.xml` — daftar halaman untuk Google crawl
- `robots.txt` — instruksi crawler + pointer ke sitemap
- `vercel.json` — cache headers, security headers, redirects

---

## LANGKAH WAJIB: Daftarkan ke Google Search Console

### Step 1: Buka Google Search Console
1. Buka https://search.google.com/search-console
2. Login dengan akun Google

### Step 2: Tambahkan Property
1. Klik **"Add Property"**
2. Pilih **"URL prefix"**
3. Masukkan: `https://hadiahlagu.com`
4. Klik **Continue**

### Step 3: Verifikasi Kepemilikan
Pilih metode **"HTML tag"**:
1. Google akan berikan meta tag seperti:
   ```html
   <meta name="google-site-verification" content="KODE_UNIK_ANDA">
   ```
2. Buka file `index.html`
3. Tambahkan meta tag tersebut di dalam `<head>` (di bawah `<meta charset="UTF-8">`)
4. Tambahkan juga ke `formulir.html`
5. Push ke GitHub:
   ```bash
   git add .
   git commit -m "Add Google verification"
   git push
   ```
6. Kembali ke Search Console, klik **Verify**

### Step 4: Submit Sitemap
1. Di Search Console, buka menu **Sitemaps** (sidebar kiri)
2. Ketik: `sitemap.xml`
3. Klik **Submit**
4. Status harus berubah menjadi **"Success"**

### Step 5: Request Indexing
1. Di Search Console, buka **URL Inspection** (sidebar kiri)
2. Ketik: `https://hadiahlagu.com`
3. Klik **Request Indexing**
4. Ulangi untuk: `https://hadiahlagu.com/formulir`

---

## Keyword Target

### Keyword Utama (high intent)
| Keyword | Volume Est. | Persaingan |
|---------|------------|------------|
| lagu pernikahan custom | Medium | Rendah |
| hadiah pernikahan unik | Tinggi | Sedang |
| bikin lagu pernikahan | Medium | Rendah |
| jasa pembuatan lagu | Medium | Sedang |
| kado nikahan unik | Tinggi | Sedang |

### Keyword Long-tail (low competition, high conversion)
- hadiah pernikahan islami unik
- lagu pernikahan dari kisah nyata
- bikin lagu untuk lamaran
- hadiah nikah murah tapi berkesan
- lagu custom untuk pengantin
- lagu pernikahan AI
- buat lagu pernikahan online

### Keyword Lokal
- hadiah pernikahan Yogyakarta
- lagu pernikahan custom Indonesia
- jasa bikin lagu nikah murah

---

## Optimasi Lanjutan (Opsional, Tapi Disarankan)

### A. Google Business Profile
1. Buka https://business.google.com
2. Daftarkan "Hadiah Lagu" sebagai bisnis online
3. Isi lengkap: nama, kategori (Music Production Service), website, WA, jam operasional
4. Upload og-image.png sebagai foto profil
5. Ini membuat bisnis muncul di Google Maps

### B. Buat Konten Blog (Sangat Direkomendasikan)
Tambahkan halaman `/blog` dengan artikel yang mentarget keyword long-tail:
- "5 Hadiah Pernikahan Islami Paling Berkesan"
- "Cara Membuat Lagu Pernikahan dari Kisah Cinta Kalian"
- "Kenapa Lagu Custom Lebih Bermakna dari Souvenir Biasa"
- "Ide Hadiah Lamaran yang Bikin Dia Menangis Bahagia"

Setiap artikel harus:
- 800-1500 kata
- Mengandung keyword target
- Ada internal link ke halaman utama/formulir
- Ada CTA di akhir artikel

### C. Backlink
- Submit ke direktori bisnis Indonesia (Yellow Pages, Indonetwork)
- Submit ke marketplace vendor pernikahan (Bridestory, WeddingKu)
- Tulis guest post di blog pernikahan/wedding

### D. Monitoring
Cek Search Console seminggu sekali:
- **Performance** — keyword apa yang mendatangkan traffic
- **Coverage** — apakah ada error indexing
- **Core Web Vitals** — kecepatan loading

---

## Estimasi Timeline SEO

| Waktu | Target |
|-------|--------|
| Hari 1 | Submit ke Google Search Console, request indexing |
| Minggu 1 | Halaman terindex di Google |
| Minggu 2-4 | FAQ rich snippet mulai muncul |
| Bulan 1-2 | Mulai ranking untuk long-tail keyword |
| Bulan 3-6 | Traffic organik stabil, ranking keyword utama |

SEO adalah permainan jangka panjang. Untuk hasil cepat, kombinasikan dengan iklan berbayar (Google Ads, IG/TikTok Ads).
