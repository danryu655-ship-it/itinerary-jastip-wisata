# Itinerary, Jastip & Wisata — Versi Statis

Website statis (satu file `index.html`) untuk membuat itinerary, mencatat jastip, dan menyimpan tempat wisata, tempat makan, dan hotel — untuk semua destinasi.

Buka lewat GitHub Pages: https://danryu655-ship-it.github.io/itinerary-jastip-wisata/

## Fitur

- **Rencana & Itinerary** — buat trip (nama, kota, tanggal, budget), itinerary harian otomatis, tambah item (jam, kategori wisata/makan/hotel/transport/belanja, perkiraan biaya), centang selesai, bar budget, salin itinerary sebagai teks.
- **Jastip** — catat titipan (yang nitip, barang, toko, harga, fee, prioritas), status Dicari → Dibeli → Dibawa → Selesai, total + total belum lunas.
- **Jelajah & Inspirasi** — katalog 10 destinasi: Osaka, Kyoto, Tokyo, Bali, Yogyakarta, Seoul, Bangkok, Singapore, Kuala Lumpur, Labuan Bajo, lengkap dengan panduan wisata/kuliner/area hotel/ide jastip dan tombol "Buat rencana". Pencarian kota di luar katalog menampilkan pesan jujur bahwa datanya belum ada — tidak ada link booking atau harga palsu.
- **Tempatku** — simpan tempat (nama, kota, kategori, rating, link Google Maps), filter per kategori.
- **Navbar floating bawah** — pill gelap, tombol aktif teal, bisa digeser menyamping di HP.
- **Asisten AI floating** — tombol di kanan bawah di atas navbar. Chatbot **rule-based client-side saja** (tanpa server / API key). Bisa memberi contoh itinerary, ide wisata/kuliner/hotel/jastip untuk kota katalog, dan membaca data trip/jastip/tempat yang tersimpan di browser kamu.

## Data

Semua data tersimpan di browser kamu (localStorage, prefix `ijw_`). Tidak ada server, tidak ada akun, tidak ada data yang dikirim ke mana pun.

## Batasan yang jujur

- Harga yang tampil adalah **perkiraan, cek ulang** sebelum berangkat.
- Chatbot versi statis ini rule-based, **tidak bisa booking dan tidak bisa mengubah data**.
- Versi fullstack asli di Muse (dengan penyimpanan server dan AI sungguhan) tidak bisa diekspor — ini adalah versi statis yang dibuat ulang untuk GitHub Pages.
