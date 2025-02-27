## CRON
CRON merupakan job scheduler yang ada di system Linux/Unix

### WP Cron
#### Penjelasan singkat
WordPress memiliki sistem cron sendiri yang dikenal sebagai WP-Cron, sistem ini menangani pekerjaan rutin (jadwal) yang ada di WordPress antarai lain:
- Memeriksa apakah ada update terbaru untuk WordPress core, plugin, maupun theme.
- Menerbitkan postingan yang terjadwal.
- Melakukan memeriksa jadwal backup yang dibuat oleh plugin backup.
- Memeriksa jadwal lain yang dibuat oleh plugin terpasang di WordPress kita.

#### Kekurangan WP-Cron
WP-Cron ditriger oleh request dari visitor atau bot, sehingga ada potensi masalah yang ditumbulkan antara lain:
- Potensi pekerjaan tidak terlaksana sesuai jadwal
- Potensi pekerjaan menumpuk sehingga bisa memberatkan load server
- Page caching biasanya membypass PHP, sehingga WP Cron tidak terekskusi meskipun ada request dari visitor maupun bot.

### Mengalihkan alih WP-Cron

Non Aktifkan WP-Cron
```bash
wp config set DISABLE_WP_CRON true --raw
```

buat CRON job
```
*/5 * * * * cd /home/elemento/public_html; /home/elemento/bin/wp cron event run --due-now >/dev/null 2>&1
```