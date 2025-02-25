# Efisiensi Resource

## Konfigurasi PHP

### Memory limit
Untuk mengontrol seberapa besar memory yang bisa digunakan oleh PHP dalam sekali produksi (sekali jalan). 

Untuk WordPress standar memory limit 128M cukup aman, untuk pengguna Elementor pro standar bisa antara 256M - 512M. Silahkan sesuaikan dengan kebutuhan.
```
memory_limit = 256M
```

### Max execution time
Untuk membatasi berapa lama skrip PHP dapat dijalankan sebelum diberhentikan. Gunakan default 30 detik cukup aman.
```
max_execution_time = 30
```

### Upload max filesize
Untuk membatasi ukuran maksimum file yang dapat diunggah ke website kita. Ini mencakup semuanya, mulai dari tema dan plugin hingga file media seperti gambar dan video. 

Jika semua plugin/tema sudah terpasang dan tidak ada keperluan upload video sebenarnya 1M - 2M cukup, namun untuk di awal bisa set 16M atau sesuai dengan kebutuhan.
```
upload_max_filesize = 16M
```

### Post max size
Untuk membatasi ukuran data yang bisa dikirim, nilainya disamakan saja dengan Upload max filesize. 
```
post_max_size = 16M
```

### Max file uploads
Batas jumlah file yang dapat diunggah secara bersamaan, jika tidak ada kebutuhan khusus gunakan default 20
```
max_file_uploads = 20
```

## Penggunaan CRON