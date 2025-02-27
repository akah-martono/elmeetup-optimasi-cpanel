# WP CLI

## Install WP CLI

Docs: 
- Instalasi: https://make.wordpress.org/cli/handbook/guides/installing/
- Perintah: https://developer.wordpress.org/cli/commands/


Download wp-cli.phar menggunakan curl:
```bash
curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
```

Periksa apakah bisa jalan:
```bash
php wp-cli.phar --info
```

Lihat folder-folder PATH yang disediakan oleh hosting:
```bash
echo $PATH
```

Periksa apakah folder PATH yang kita ingin kan tersedia (misalnya kita pilih '/home/elemento/bin')
```bash
ls /home/elemento/bin
```

Jika belum tersedia buat foldernya
```bash
mkdir /home/elemento/bin
```

Jadikan executable dan pindahkan ke folder PATH agar bisa dijalankan dari mana saja:
```bash
chmod +x wp-cli.phar
mv wp-cli.phar /home/elemento/bin/wp
```

Test hasilnya:
```bash
wp --info
```

## Perintah WP CLI yang sering digunakan

### Update Plugin, Theme, dan Core
```bash
wp plugin update --all
wp theme update --all
wp core update
```

### Hapus Plugin dan Theme
```bash
wp plugin delete akismet
wp plugin delete hello
wp theme delete twentytwentyfour
wp theme delete twentytwentythree
```


### Optimasi Database
```bash
wp db optimize
```

### Backup Database
```bash
wp db export ../db.sql
```
Jika ingin backup file menggunakan zip:
```bash
zip -r ../siteku.zip ./
```

### Search Replace
```bash
wp search-replace 'https://example.test' 'https://www.example.com'
```

### Bersihkan Cache
```bash
wp cli cache clear
```

### Hapus Transient yang expired
```bash
wp transient delete --expired
```

