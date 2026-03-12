# email_firebase-postmain
Dokumentasi ini menjelaskan proses pengujian API Firebase Authentication menggunakan Postman.  
Pengujian yang dilakukan meliputi:

- Membuat akun baru (Sign-Up)
- Mengirim email verifikasi
- Mengecek status verifikasi akun

Teknologi yang digunakan:
- Firebase Authentication
- Postman
- Firebase REST API

---

# 1. Persiapan Firebase

## 1.1 Masuk ke Firebase Console

Langkah pertama adalah membuka Firebase Console dan membuat atau memilih project yang akan digunakan.

![Firebase Console](tugas/firebase-console.png)

---

## 1.2 Mengaktifkan Authentication Method

Masuk ke menu **Authentication → Sign-in Method** lalu aktifkan:

- Google Sign-In
- Email/Password

Hal ini memungkinkan pengguna untuk melakukan autentikasi menggunakan email atau akun Google.

![Enable Authentication](tugas/enable-google.png)

---

## 1.3 Mengambil Firebase API Key

Untuk menggunakan Firebase REST API, kita memerlukan **API Key** dari project Firebase.

Langkah:
1. Masuk ke **Project Settings**
2. Cari bagian **Web API Key**

API Key ini akan digunakan pada request API di Postman.

![Firebase API Key](tugas/website-setting-firebase.png)

---

# 2. Setup Postman Environment

## 2.1 Membuat Environment Baru

Buka Postman lalu buat **Environment baru** untuk menyimpan variabel seperti:

- `firebase_api_key`

Hal ini memudahkan penggunaan API Key di berbagai request.

![Postman Environment](tugas/environment.png)

---
