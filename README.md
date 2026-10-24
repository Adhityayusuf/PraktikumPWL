# PraktikumPWL

Aplikasi admin manajemen data untuk praktikum **Pemrograman Web Lanjut (PWL)**,
dibangun dengan **Laravel 12** dan panel admin **Filament 4**.

Alih-alih menulis CRUD manual, seluruh manajemen data dilakukan lewat panel
admin di `/admin` — mulai dari user, kategori, post, sampai produk.

## Fitur

- Panel admin (`/admin`) berbasis Filament 4
- Resource **Users** — daftar, tambah, edit user
- Resource **Categories** — manajemen kategori
- Resource **Posts** — manajemen post beserta relasi kategori
- Resource **Products** — daftar, tambah, edit, dan detail produk
- Migrasi tabel: `users`, `categories`, `posts`, `products`

## Tech Stack

- PHP ^8.2
- Laravel 12
- Filament 4 (admin panel)
- Vite (aset front-end)

## Instalasi

```bash
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
npm install
npm run build
php artisan serve
```

Atau langsung pakai script bawaan:

```bash
composer run setup
```

Buka `http://127.0.0.1:8000/admin` untuk masuk panel admin.

## Struktur Penting

```
app/Filament/Resources/
├── Users/        # CRUD user
├── Categories/   # CRUD kategori
├── Posts/        # CRUD post
└── Products/     # CRUD produk (termasuk halaman view)
database/migrations/
└── create_categories, create_posts, create_products
```

## Konteks

Repo ini bagian dari praktikum Pemrograman Web Lanjut,
Politeknik Negeri Malang (Polinema), Jurusan Teknologi Informasi.
