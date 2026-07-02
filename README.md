# 📖 Deskripsi Aplikasi

**Dompet Kita** merupakan aplikasi **E-Money berbasis Flutter** yang dikembangkan sebagai proyek **Ujian Akhir Semester (UAS) Mata Kuliah Aplikasi Mobile Lanjutan** di Institut Teknologi dan Bisnis Bina Sarana Global.

Aplikasi ini berfungsi sebagai dompet digital yang memungkinkan pengguna melakukan transaksi pembayaran secara aman melalui mekanisme **App-to-App Integration** menggunakan **Deep Link**. Dompet Kita terhubung dengan aplikasi **E-Commerce (Merchant)** sehingga pengguna dapat menerima permintaan pembayaran, melakukan verifikasi transaksi menggunakan **Two-Factor Authentication (2FA)**, memotong saldo secara otomatis, dan mengirimkan hasil transaksi kembali ke aplikasi Merchant melalui callback Deep Link.

Selain fitur pembayaran, aplikasi juga menyediakan autentikasi pengguna menggunakan **Firebase Authentication**, pengelolaan saldo, riwayat transaksi, serta notifikasi transaksi secara real-time menggunakan **Firebase Cloud Messaging (FCM)**. Seluruh proses komunikasi data dilakukan melalui **RESTful API** yang terhubung dengan backend untuk memastikan keamanan dan konsistensi data selama proses transaksi berlangsung.

Aplikasi ini dikembangkan dengan tujuan untuk mengimplementasikan konsep integrasi antar aplikasi (App-to-App Integration), komunikasi dengan Backend API, pengelolaan transaksi digital, serta penerapan keamanan transaksi pada aplikasi mobile menggunakan Flutter.

---
# 👨‍💻 Nama

Nama : Regina Safarina

Program Studi : Teknik Informatika
Kelas         : TI SE 23 P2 

---

# 📱 Fitur Utama

- 🔐 Login menggunakan Firebase Authentication
- 👤 Registrasi akun pengguna
- 💰 Melihat saldo E-Money
- 📊 Riwayat transaksi
- 💳 Pembayaran melalui Deep Link
- 🔑 Verifikasi transaksi menggunakan Two Factor Authentication (2FA)
- 🔔 Notifikasi transaksi menggunakan Firebase Cloud Messaging (FCM)
- 📥 Callback hasil pembayaran ke aplikasi Merchant
- 🌙 UI Modern dan Responsive

---

### Teknologi yang digunakan

- Flutter
- Dart
- Firebase Authentication
- Firebase Cloud Messaging
- Dio
- Provider
- Deep Link (app_links)
- REST API
- Shared Preferences

---

# 🏗️ Arsitektur Aplikasi

Project menggunakan **Feature First Architecture** dengan pemisahan berdasarkan fitur dan layer sehingga mudah dikembangkan dan dipelihara.

```text
lib/
│
├── main.dart
├── firebase_options.dart
│
├── core/
│   ├── constantss/
│   ├── error/
│   ├── network/
│   ├── router/
│   ├── services/
│   ├── theme/
│   └── utils/
│
├── data/
│   ├── datasources/
│   ├── models/
│   ├── repositories/
│   
│
└── domain/
│   ├── entities/
│   ├── repositories/
│   ├── usecases/
│   
│
└── injection/
│   ├── entities/
│   ├── repositories/
│   ├── usecases/
│   
│
└── presentation/
│   ├── blocs/
│   ├── pages/
│   ├── widgets/
│   
│
└── firebase_options.dart
└── main.dart

```


# 🔄 Arsitektur Sistem

```
User
   │
   ▼
Flutter E-Money
   │
   ├──────────────► Firebase Authentication
   │
   ├──────────────► Backend API
   │                    │
   │                    ▼
   │                 Database
   │
   └──────────────► Deep Link
                         │
                         ▼
               Aplikasi Merchant
```

---

# 🔗 Implementasi Deep Link

Aplikasi menggunakan **Custom Scheme Deep Link** sebagai media komunikasi antar aplikasi.

Flow pembayaran:

```
Merchant
    │
    ▼
Deep Link
(dompetkita://pay)
    │
    ▼
Dompet Kita
    │
    ▼
Verifikasi PIN + 2FA
    │
    ▼
Potong Saldo
    │
    ▼
Callback
merchant://payment-callback
```

---

# 🔒 Two Factor Authentication (2FA)

Untuk menjaga keamanan transaksi, setiap pembayaran akan melalui proses:

1. User memilih pembayaran E-Money.
2. Merchant mengirim Deep Link.
3. Dompet Kita menerima request pembayaran.
4. User melakukan verifikasi PIN / OTP (2FA).
5. Backend memvalidasi transaksi.
6. Saldo dipotong.
7. Callback dikirim ke aplikasi Merchant.

---
 
#🖥️ Backend

Repository Backend:

https://github.com/ginaa07/be-money

Backend menangani:

- Authentication
- Wallet
- Saldo
- Payment
- Transaction
- Deep Link Callback
- Firebase Token
- Two Factor Authentication

---

#🖥️ Frontend Aplikasi Toko sepatu heels wanita

Repository frontend:

https://github.com/ginaa07/Toko_Sepatu_Heels_Wanita.git

#🖥️ Backend Aplikasi Toko sepatu heels wanita

Repository Backend:

https://github.com/ginaa07/ReginaSafarina-gin-firebase-backend.git

# 🚀 Cara Menjalankan Project

## 1 Clone Repository

```bash
git clone https://github.com/ginaa07/be-money.git
```

## 2 Masuk Folder

```bash
cd be-money
```

## 3 Install Dependency

```bash
flutter pub get
```

## 4 Jalankan Project

```bash
flutter run
```

---

# 📦 Dependency Utama

```yaml
firebase_core
firebase_auth
firebase_messaging
dio
provider
shared_preferences
app_links
url_launcher
flutter_local_notifications
intl
```

---

## Tampilan UI Dompet Kita
- **Nama** : Dompetkita

## 📸 Screenshots
<p align="center">
  <img src="assets/images/dompetkita.jpg" width="300" alt="Dompet Kita">
<img src="assets/images/buatakun.jpg" width="300" alt="Dompet Kita">
<img src="assets/images/lanjutdengangoogle.jpg" width="300" alt="Dompet Kita">
<img src="assets/images/masukemailotp.jpg" width="300" alt="Dompet Kita">
<img src="assets/images/saldodompetkita.jpg" width="300" alt="Dompet Kita">
<img src="assets/images/transaksi.jpg" width="300" alt="Dompet Kita">
<img src="assets/images/akunregina.jpg" width="300" alt="Dompet Kita">

    ---

    # 📂 Struktur Project

```
lib
│
├── core
├── data
├── domain
├── injection
├── presentation
├── firebase_options.dart
└── main.dart
```
---
# 🛠️ Tools

- Flutter SDK
- Dart
- Android Studio
- Visual Studio Code
- Firebase
- Postman
- Git
- GitHub

---

# 📚 Mata Kuliah

Aplikasi Mobile Lanjutan

Institut Teknologi dan Bisnis Bina Sarana Global

Semester Genap 2026

---


# 🎥 Video Demo Aplikasi

 Link YouTube di sini


https://youtu.be/xxxxxxxxxx

---

