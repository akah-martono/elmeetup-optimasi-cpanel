# Simple Security

## Amankan File dan Folder
Buka terminal, lalu masuk ke folder WordPress, kemudian set file permissions:
- Folder: 755
    ```bash
    find . -type d -exec chmod 755 {} \;
    ```
- File: 644
    ```bash
    find . -type f -exec chmod 644 {} \;
    ```
- wp-config.php: 600
    ```bash
    chmod 600 wp-config.php
    ```

## Disable Theme and Plugin Update
Cegah penambahan dan update plugin menggunakan WP CLI
```bash
wp config set DISALLOW_FILE_MODS true --raw
```

Pastikan kita melakukan update secara berkala dengan perintah berikut
```bash
wp core update
wp plugin update --all
```

## Cegah isi folder terlihat
Tambahkan pada .htaccess
```
Options All -Indexes
```
