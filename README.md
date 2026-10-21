# Nextcloud & MariaDB Stack (Developed by Harish)

Template Docker Compose siap pakai untuk menjalankan layanan Nextcloud lengkap dengan MariaDB sebagai database dan phpMyAdmin untuk pengelolaan database berbasis web yang intuitif. Stack ini dirancang bersih, efisien, dan siap digunakan tanpa konfigurasi yang rumit.

---

## Fitur Utama
- Nextcloud (Latest): Platform penyimpanan awan mandiri (self-hosted cloud storage) berkinerja tinggi.
- MariaDB (10.11): Sistem manajemen database relasional yang stabil dan teroptimasi khusus untuk Nextcloud.
- phpMyAdmin: Antarmuka web visual untuk mempermudah manajemen database MariaDB.
- Plug-and-Play: Dilengkapi variabel lingkungan (environment variables) bawaan untuk kemudahan pengujian cepat.

---

## Kredensial Default

Catatan: Kredensial di bawah ini dikonfigurasi secara bawaan untuk keperluan pengujian lokal / pengembangan.

### Nextcloud Admin
- Username: admin
- Password: 1234

### Database MariaDB
- Root Password: 1234
- Database Name: nextcloud
- User: nextcloud
- Password: 1234

### phpMyAdmin
- Host / Server: db
- Username: root (atau nextcloud)
- Password: 1234

---

## Port Akses Layanan
- Nextcloud Web UI: http://<IP-Server>:8080
- phpMyAdmin UI: http://<IP-Server>:8082

---

## Cara Penggunaan

### Opsi 1: Menggunakan Portainer Custom Template (Rekomendasi)
1. Buka dashboard Portainer Anda.
2. Masuk ke menu Templates > Custom Templates > + Add Custom Template.
3. Pada opsi Build method, pilih Repository.
4. Isi formulir sebagai berikut:
   - Title: NextCloud By HarishR
   - Repository URL: https://github.com/hrabbani487-creator/nextcloud-template
   - Compose path: docker-compose.yaml
   - Logo URL: https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/png/kali-linux.png
5. Klik Create custom template.
6. Gunakan template tersebut untuk mendeploy Stack Nextcloud Anda dengan sekali klik!

### Opsi 2: Menggunakan Docker Compose Manual (Terminal)
```bash
# 1. Clone repositori ini
git clone [https://github.com/hrabbani487-creator/nextcloud-template.git](https://github.com/hrabbani487-creator/nextcloud-template.git)
cd nextcloud-template

# 2. Salin variabel lingkungan contoh menjadi file .env
cp catatan.env.example .env

# 3. Jalankan container secara background
sudo docker compose up -d
