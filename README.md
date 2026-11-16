# Proyek UTS Pemrograman Web Dasar: KlinWash Laundry Express

Website profil UMKM untuk usaha jasa binatu **KlinWash Laundry Express** di Rawamangun, Jakarta Timur. Proyek ini dibangun sebagai pemenuhan tugas Ujian Tengah Semester (UTS) mata kuliah Pemrograman Web Dasar menggunakan HTML5 dan CSS3 murni tanpa framework.

---

## 1. Identitas Mahasiswa

* **Nama Lengkap** : Mia Rahmawati
* **NIM** : 2559201011
* **Mata Kuliah** : Pemrograman Web Dasar (Semester 3)
* **Dosen Pengampu** : Ditra Iiandaputra, S.Kom., M.Kom
* **Nama Repositori** : `2559201011-Mia-Rahmawati-UTS`

---

## 2. Tema dan Usaha yang Dipilih

* **Tema** : Tema A - Profil UMKM
* **Nama Usaha** : KlinWash Laundry Express
* **Bidang Usaha** : Jasa Laundry Kiloan, Satuan, Sepatu, Bed Cover, Karpet, dan Dry Cleaning
* **Alamat Outlet** : Jl. Pemuda No. 45, RT 03 / RW 05, Rawamangun, Pulo Gadung, Jakarta Timur
* **Alasan Pemilihan** :
  Usaha laundry ini dipilih karena relevan dengan kebutuhan mahasiswa dan masyarakat perkotaan yang memerlukan jasa pencucian pakaian yang cepat, bersih, dan higienis dengan aturan satu mesin untuk satu pelanggan.

---

## 3. Struktur Halaman Website

Website terdiri dari 4 halaman utama:

1. **`index.html` (Beranda)**
   - Hero banner dengan tagline usaha dan tombol ajakan pesan.
   - Ringkasan keunggulan usaha (air filtrasi 3 tahap, deterjen ramah lingkungan, pengerjaan tepat waktu).
   - 3 Layanan unggulan (Cuci Kiloan Express 24 Jam, Deep Clean Sepatu, Cuci Bed Cover).
   - Banner informasi layanan antar-jemput.

2. **`tentang.html` (Tentang Kami)**
   - Sejarah singkat berdirinya usaha sejak 2023 di Rawamangun.
   - Visi dan misi usaha.
   - Profil pengelola (Mia Rahmawati, Budi Santoso, Siti Aisyah).
   - Tabel standar fasilitas mesin cuci, pengering, filtrasi, dan finishing.

3. **`katalog.html` (Katalog Layanan)**
   - 7 Kartu layanan lengkap dengan foto, nama paket, deskripsi, durasi pengerjaan, dan harga resmi.
   - Tata letak menggunakan CSS Grid.
   - Tabel tarif resmi dan estimasi waktu pengerjaan.

4. **`kontak.html` (Kontak)**
   - Alamat lengkap, nomor WhatsApp, email, dan akun media sosial.
   - Tombol langsung untuk chat WhatsApp.
   - Formulir kontak online dengan validasi bawaan HTML5 (`required`, `type="email"`, `type="tel"` dengan regex pattern, pilihan subjek pesan, serta batas minimal/maksimal karakter pesan).
   - Tabel jam buka outlet dan jadwal operasional mingguan.

---

## 4. Spesifikasi Teknis CSS

* Seluruh styling diatur di file eksternal `css/style.css` tanpa inline style (`style=""`) dan tanpa tag `<style>`.
* **Flexbox** digunakan untuk mengatur navigasi navbar (`.navbar`).
* **CSS Grid** digunakan untuk menyusun kartu katalog layanan (`.catalog-grid`).
* **Variabel CSS** di `:root` untuk warna utama, warna teks, background, dan font.
* **Efek Interaksi CSS**:
  - Efek `:hover` pada tombol, kartu katalog, baris tabel, dan link navigasi.
  - Efek `transition: 0.3s ease` agar perubahan warna saat hover terlihat halus.
  - Animasi `@keyframes fadeIn` saat halaman dimuat agar tampilan muncul perlahan.
* **Responsif**:
  - Breakpoint mobile (`@media (max-width: 600px)`): Kartu katalog berubah menjadi 1 kolom dan menu navigasi tersusun vertikal di bawah logo.
  - Breakpoint desktop (`@media (min-width: 992px)`): Tata letak multi-kolom horizontal.

---

## 5. Sumber Gambar

Aset visual disimpan di folder `img/` dalam format vektor SVG:
- `img/logo.svg` : Logo usaha KlinWash Laundry Express.
- `img/hero-laundry.svg` : Ilustrasi mesin cuci dan pakaian pada bagian hero.
- `img/about-facility.svg` : Ilustrasi workshop dan mesin cuci.
- `img/team-mia.svg`, `img/team-budi.svg`, `img/team-siti.svg` : Ilustrasi profil tim pengelola.
- `img/service-*.svg` : Ilustrasi untuk masing-masing kartu layanan pada halaman katalog.

---

## 6. Kendala yang Dihadapi dan Solusi

1. **Kendala**: Tampilan navigasi desktop bertumpuk saat dibuka di layar handphone yang sempit.
   * **Solusi**: Menggunakan media query `@media (max-width: 600px)` untuk mengubah arah flexbox menu menjadi kolom (`flex-direction: column`) sehingga tersusun rapi ke bawah.

2. **Kendala**: Kartu katalog menjadi terlalu kecil jika dipaksakan 3 kolom di layar handphone.
   * **Solusi**: Menyesuaikan CSS Grid pada tampilan layar ponsel menjadi `grid-template-columns: 1fr`, sehingga setiap kartu otomatis melebar penuh 1 kolom.

3. **Kendala**: Validasi input nomor telepon agar pengguna memasukkan angka dengan jumlah digit yang tepat.
   * **Solusi**: Menggunakan atribut HTML5 `pattern="[0-9]{10,13}"` agar browser secara otomatis memeriksa nomor yang dimasukkan harus berupa 10 sampai 13 digit angka.

---

## 7. Catatan Commit Bertahap

Urutan commit git bertahap yang dilakukan saat pengerjaan proyek:

```bash
git init
git add img/
git commit -m "Inisialisasi folder dan aset gambar website"

git add index.html tentang.html
git commit -m "Membuat struktur halaman beranda dan tentang kami"

git add katalog.html kontak.html
git commit -m "Membuat halaman katalog layanan dan form kontak"

git add css/style.css
git commit -m "Menambahkan styling CSS flexbox dan grid"

git add css/style.css index.html tentang.html katalog.html kontak.html
git commit -m "Menambahkan media query responsif untuk tampilan HP"

git add README.md
git commit -m "Menyelesaikan dokumentasi README proyek"
```
