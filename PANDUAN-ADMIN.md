# Panduan Admin – Website Marijo Rasa

Website ini memakai **Pages CMS** (gratis) sebagai panel Admin. Semua teks, foto, produk, harga, dan kontak disimpan di file `content.json`. Admin cukup mengisi formulir di panel, tanpa menyentuh kode.

Alurnya: **Admin edit di Pages CMS → perubahan tersimpan di GitHub → Netlify memperbarui website otomatis (±1 menit).**

## Isi folder

| File | Fungsi |
|---|---|
| `index.html` | Tampilan website (tidak perlu diubah) |
| `content.json` | Semua isi website (diedit lewat panel Admin) |
| `.pages.yml` | Pengaturan formulir panel Admin |
| `images/` | Foto-foto website |

## Setup sekali saja (±20 menit)

### 1. Simpan file di GitHub
1. Buat akun gratis di https://github.com.
2. Klik **New repository**, beri nama misalnya `marijorasa-website`, pilih **Public** atau **Private**, lalu **Create repository**.
3. Klik **uploading an existing file**, seret semua isi folder (termasuk folder `images`), lalu **Commit changes**.
4. Pastikan file `.pages.yml` ikut terunggah. File berawalan titik kadang tersembunyi di komputer. Jika tidak ada, klik **Add file → Create new file**, beri nama `.pages.yml`, tempel isinya, lalu **Commit changes**.

### 2. Online-kan di Netlify
1. Masuk ke https://app.netlify.com dengan akun GitHub.
2. Klik **Add new site → Import an existing project → GitHub**, pilih repository `marijorasa-website`.
3. Kosongkan *Build command*, isi *Publish directory* dengan `.` (titik), lalu **Deploy**.
4. Ganti alamat di **Site configuration → Change site name**, misalnya `marijorasa` → website menjadi `marijorasa.netlify.app`.

### 3. Hubungkan panel Admin (Pages CMS)
1. Buka https://app.pagescms.org dan **Sign in with GitHub**.
2. Izinkan Pages CMS mengakses repository `marijorasa-website`.
3. Pilih repository tersebut. Menu **Isi Website Marijo Rasa** akan muncul.

## Cara update website

1. Buka https://app.pagescms.org → pilih repository → **Isi Website Marijo Rasa**.
2. Ubah yang perlu:
   - **Teks**: judul, kalimat pembuka, deskripsi, kontak, footer.
   - **Foto**: klik kolom foto → upload gambar baru dari HP/komputer.
   - **Produk**: tambah produk baru, ubah harga, atau matikan **Stok tersedia** saat stok habis (tombol pesan berubah menjadi "Tanya ketersediaan").
   - **Kontak**: nomor WhatsApp dan Instagram.
3. Klik **Save**. Tunggu ±1 menit, lalu refresh website.

## Tips

- **Harga** tulis angka saja, mis. `35000` (tampil otomatis sebagai Rp35.000).
- **Nomor WhatsApp untuk link** pakai format `62...` tanpa `+`, spasi, atau `0` di depan. Contoh: `0821 2231 2502` → `6282122312502`.
- **Ukuran foto** usahakan di bawah 500 KB supaya website cepat dibuka di HP. Foto utama lebar (mis. 1254×890 px), foto produk tegak (mis. 380×500 px).
- Ingin menambah Admin lain? Undang akun GitHub-nya di repository: **Settings → Collaborators**.
- Salah edit? Semua riwayat perubahan tersimpan di GitHub (tab **Commits**) dan bisa dikembalikan.
