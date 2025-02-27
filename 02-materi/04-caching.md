# Caching

## Page Caching
Halaman website hasil produksi (digenerate oleh PHP) yang disimpan untuk digunakan saat ada permintaan/request ulang.

![Lego Pack as Page Cache Ilustration](/assets/page-cache.jpg)

## Object Caching
Docs: https://developer.wordpress.org/reference/classes/wp_object_cache/

![Lego Door as Object Cache Ilustration](/assets/object-cache.jpg)

Object bisa kita bayangkan sebagai group komponen lego yang menjadi bagian dari pembentuk rumah, contohnya pintu.

WordPress menggunakan cache pada object agar tidak perlu memproduksi ulang untuk group komponen yang sama. mulai dari versi 2.5 object cache tidak dibuat persisten, sehingga object cache hanya berlaku untuk sekali jalan. Untuk membuatnya menjadi persisten kita perlu menggunakan plugin tambahan.

## Masalah Umum pada Teknik Caching
### Masalah
- Tampilan tidak terupdate.
- Tampilan rusak.
- Tampilan mobile dan desktop tidak bisa sama-sama bagus.

### Penyebab
- Settingan kurang pas atau lupa clear cache.
- Menggunakan asset generator yang tidak tepat.
- Tidak menggunakan cache berdasarkan device.