# Liburan Seru — Versi Statis

Website statis (satu file `index.html`) **Liburan Seru** untuk membuat itinerary, mencatat jastip, dan menyimpan tempat wisata, tempat makan, dan hotel — untuk semua destinasi.

Logo: logo lama dari aplikasi Flutter Liburan Seru (16 Nov 2026) — globe teal tersenyum di latar oranye + tas belanja & koper, dan logo lengkap "Liburan Seru — JASTIP • TRAVEL DUNIA". File aslinya (`logo-icon.webp` dan `logo-full.webp`, byte-for-byte dari repo `liburan-seru-flutter`) disimpan di folder ini, dan karena konektor GitHub menolak upload file biner, logo itu di-embed ke `index.html` sebagai data URI (byte yang sama persis) supaya tampil di GitHub Pages. Nama brand "Liburan Seru" sama di mode Bahasa Indonesia dan Inggris.

Buka lewat GitHub Pages: https://danryu655-ship-it.github.io/itinerary-jastip-wisata/

## Fitur

- **Rencana & Itinerary** — buat trip (nama, kota, tanggal, budget), itinerary harian otomatis, tambah item (jam mulai + durasi dengan jam selesai otomatis, kategori wisata/makan/hotel/transport/belanja, biaya dalam mata uang apa pun dengan konversi IDR otomatis dari kurs tersimpan, moda transportasi). Jarak & waktu tempuh dari tempat sebelumnya bisa dihitung otomatis dari peta (tombol "🗺️ Hitung otomatis dari peta", juga tombol 🗺️ di tiap item) via Nominatim + OSRM — kereta/pesawat memakai perkiraan garis lurus dan dilabeli jelas; kalau tempat tidak ketemu di peta, isi manual (tidak dikarang). Ringkasan per hari dan total trip: total biaya (IDR), total jarak, total waktu tempuh, total durasi kegiatan. Centang selesai, bar budget, salin itinerary sebagai teks, dan tombol **🖨️ Cetak / PDF** di tiap trip dan di form item — membuka lembar cetak rapi lalu `window.print()` (pilih "Save as PDF" di dialog printer).
- **Jastip** — catat titipan (yang nitip, barang, toko, harga dalam 15+ mata uang dengan estimasi IDR otomatis dari kurs tersimpan, fee, prioritas), status perjalanan Dicari → Dibeli → Dibawa → Selesai plus status bayar Belum Bayar / DP / Lunas (ketuk chip untuk ganti), total + total belum lunas.
- **Kurs & Konverter** — 17 mata uang ke IDR (kurs default perkiraan Nov 2026 dari aplikasi lama, bisa diubah manual, tersimpan di browser, dan diperbarui online via open.er-api.com dengan fallback manual kalau offline).
- **Jelajah & Tempatku** — katalog 19 destinasi: Osaka, Kyoto, Tokyo, Bali, Yogyakarta, Seoul, Bangkok, Singapore, Kuala Lumpur, Labuan Bajo, London, Paris, Roma, Madrid, Swiss Alps, Dubai, Istanbul, New York, Sydney, lengkap dengan panduan wisata/kuliner/area hotel/ide jastip, city pass, contoh itinerary 3–4 hari, dan tombol "Buat rencana". Pencarian kota di luar katalog menampilkan pesan jujur bahwa datanya belum ada — tidak ada link booking atau harga palsu. Di bawah katalog ada seksi **Tempatku** — simpan tempat (nama, kota, kategori, rating, link Google Maps), filter per kategori.
- **Navbar floating bawah** — pill gelap, tombol aktif teal, bisa digeser menyamping di HP.
- **Asisten AI floating** — tombol di kanan bawah di atas navbar. Chatbot **rule-based client-side saja** (tanpa server / API key). Bisa memberi contoh itinerary, ide wisata/kuliner/hotel/jastip untuk kota katalog, dan membaca data trip/jastip/tempat yang tersimpan di browser kamu.

## Data

Semua data tersimpan di browser kamu (localStorage, prefix `ijw_`). Tidak ada server, tidak ada akun, tidak ada data yang dikirim ke mana pun.

## Batasan yang jujur

- Harga yang tampil adalah **perkiraan, cek ulang** sebelum berangkat.
- Chatbot versi statis ini rule-based, **tidak bisa booking dan tidak bisa mengubah data**.
- Versi fullstack asli di Muse (dengan penyimpanan server dan AI sungguhan) tidak bisa diekspor — ini adalah versi statis yang dibuat ulang untuk GitHub Pages.
