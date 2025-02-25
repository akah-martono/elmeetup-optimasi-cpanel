# Optimasi Website

![Cara Kerja Web Server](/assets/cara-kerja-webserver.jpg)

Mungkin kita bisa bayangkan halaman website itu adalah sebuah rumah yang terbuat dari lego, agar rumah lego itu terbentuk ada 3 pihak yang terlibat yaitu:
1. Penyedia (web server/hosting): Menyiapkan bagian-bagian lego yang dibutuhkan.
2. Kurir (jaringan internet): Mengantarkan paket yang disiapkan oleh Penyedia.
3. Perakit (browser): Merakit bagian-bagian lego yang diterima dari Kurir agar menjadi bentuk rumah.

## Optimasi Penyedia

### Optimalkan Mesin Produksi
Gunakan mesin produksi yang sesuai dan terbaru

### Efisiensi Resource
Misalkan resource adalah daya listrik yang tersedia untuk memproduksi lego. Jika Penyedia punya resource 1000W dan memiliki 5 line produksi maka masing-masing line sebaiknya dibatasi 200W/line agar produksi bisa jalan di 5 line sekaligus.

### Caching
Jika jenis rumah yang dipesan begitu-begitu saja maka si Penyedia bisa menyiapkan paket sebelum dipesan (misal paket untuk jenis Rumah A, Rumah B, dan Rumah C). Dengan cara ini Penyedia bisa langsung kirim paket tanpa memproduksi terlebih dahulu. Penyiapan paket sebelum dipesan ulang ini disebut Caching.

## Optimasi Kurir/Pengiriman

### Ringkas
Agar kurir bisa lebih cepat mengirim bagian-bagian lego ke perakit, maka packagingnya harus baik (ringan dan ringkas). ini biasanya menggunakan compressing atau minify.

### Jalur yang bagus
Gunakan jalur yang bagus agar pengiriman lancar dan lebih cepat. Jalur yang bisa digunakan oleh website bisa HTTP/1.0, HTTP/1.1, HTTP/2, HTTP/3 (QUIC)

## Optimasi Perakit

### Struktur tidak rumit
Hindari desain rumah dengan struktur yang rumit agar proses perakitan lebih cepat.

### Instruksi Jelas
Agar bentuk rumahnya bisa segera dilihat maka Perakit harus diberi instruksi yang jelas, kita juga perlu instruksikan ke Perakit agar merakit bagian-bagian yang penting dulu sehingga bentuk rumah bisa segera dilihat tanpa perlu menunggu proses perakitan selesai semua. Dalam hal ini instruksi-instruksi yang biasa digunakan adalah preload, defer, delay, dan lazyload