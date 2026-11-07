# Katalog Online Garem Store

Landing page katalog stok HP second yang **ready** di Garem Store
(Poncol, Kota Pekalongan) — responsif, gratis, dan selalu mutakhir.

## Cara kerja

```text
[ Saluran WhatsApp Garem Store ]  (update stok & payu diumumkan di sini)
        │
        ▼
[ Google Sheets ]  "Katalog Garem Store — Stok Ready"
        │  disinkronkan Muse dari data stok terverifikasi setiap ada perubahan
        ▼
[ Halaman ini ]  menarik data sheet sebagai JSON (gviz) — muat ulang otomatis 60 detik
        │
        ▼
[ HP Pembeli ]  lihat katalog → klik "Beli via WhatsApp" → chat toko langsung
```

- Sumber data: Google Sheet `1vc4LBoI2mOudxjqklI-8emm3-9HM9OyfhHKZiGj7RHY`
  (tab `Katalog`: Model, Varian, Warna, Harga, Stok, Foto, Catatan).
- Harga yang tampil adalah **harga pasang publik** (siap COD Wilayah
  Kota Pekalongan – Batang). Tidak ada harga internal di sheet maupun halaman.
- Baris dengan Stok 0 otomatis tidak ditampilkan.
- Tombol "Beli via WhatsApp" membuka chat ke 0882-1226-9688 dengan pesan
  yang sudah terisi model + varian + harga.

## Memperbarui katalog

Cukup perbarui sheet-nya (atau kabari Muse bila ada payu/unit baru — sinkron
sheet adalah bagian dari alur update stok Garem Store). Halaman publik
mengikuti isi sheet dalam ±60 detik tanpa deploy ulang.
