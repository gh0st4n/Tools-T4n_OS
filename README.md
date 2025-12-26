# VUR-Helper (vur)

**VUR-Helper** adalah tool **wrapper** untuk Void Linux yang menggunakan **xbps-src sebagai backend**, dengan konsep mirip **AUR (Arch User Repository)**.

Tool ini dibuat untuk mempermudah:
- Build package dari **VUR (Void User Repo)**
- Mengelola package custom
- Menjembatani `xbps` dan `xbps-src` dalam satu perintah

Tidak menggantikan xbps.  
Tidak menutupi cara kerja Void.  
Hanya **membungkus dan menyederhanakan**.


## 🎯 Tujuan

- Menyederhanakan workflow `xbps-src`
- Memberi pengalaman seperti AUR helper
- Tetap transparan & bisa diaudit
- Cocok untuk:
  - Power-user
  - Sysadmin
  - Developer
  - User Void Linux yang benci ribet

## 🧱 Backend

- **Package manager**: `xbps`
- **Build system**: `xbps-src`
- **Repo tambahan**: VUR (Void User Repo)

VUR-Helper **tidak melakukan magic**.  
Semua proses tetap mengikuti mekanisme Void Linux.


## 📦 Konsep (Mirip AUR)

| Arch Linux | Void Linux |
|----------|------------|
| AUR | VUR |
| makepkg | xbps-src |
| yay / paru | vur |

## 🚀 Cara Penggunaan

### Install / Build Package dari VUR
```sh
vur pkg <nama-pkg>
````

* Fetch template
* Build dengan `xbps-src`
* Install hasil build

### Fetch Template Saja

```sh
vur fetch <nama-pkg>
```

* Clone / update template dari VUR
* Tidak build
* Tidak install

### Remove Package

```sh
vur remove <nama-pkg>
```

Wrapper dari:

```sh
xbps-remove <nama-pkg>
```

### Query Package

```sh
vur query <nama-pkg>
```

Wrapper dari:

```sh
xbps-query <nama-pkg>
```

### Update Semua (Wrapper + VUR)

```sh
vur -au
```

Fungsi:

* Update package via `xbps`
* Cek update template di VUR
* Sinkronisasi wrapper

### Sync Repository

```sh
vur -S
```

Wrapper dari:

```sh
xbps-install -S
```

### Update Sistem

```sh
vur -Su
```

Wrapper dari:

```sh
xbps-install -Su
```

## 🧰 Fitur Lainnya

VUR-Helper juga membungkus perintah lain dari:

* `xbps-install`
* `xbps-remove`
* `xbps-query`
* `xbps-src`

Tujuan:

* Satu entry point
* Konsisten
* Tidak perlu menghafal banyak perintah


## ⚠️ Catatan Penting

* Ini **BUKAN** tool pemula
* User **harus paham Void Linux**
* Konflik dependency = tanggung jawab user
* Build error = debug sendiri

Kalau lu nyari:

* Auto-fix
* GUI
* Error disembunyiin

➡️ **Jangan pakai ini**

## 🧪 Status Proyek

* Eksperimental
* Digunakan di **T4n OS**
* Bisa berubah sewaktu-waktu
* Tidak ada jaminan stabil

## 🧠 Filosofi

* Wrapper, bukan pengganti
* Transparan
* Minimal
* User pegang kontrol penuh

## 📜 Lisensi

Bebas.
Pakai, fork, modif, rusak, ulangi.
