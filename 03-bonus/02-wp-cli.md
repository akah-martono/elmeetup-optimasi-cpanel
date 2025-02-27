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


## Mengkonfigure WordPress
wp-config.php docs: https://developer.wordpress.org/advanced-administration/wordpress/wp-config/

## Maintain Plugin

## Maintain Theme


## Backup Database
```bash
wp db export ../db.sql
```
