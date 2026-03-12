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

# 3. Request API - Sign Up (Membuat Akun Baru)

Endpoint yang digunakan: "POST https://identitytoolkit.googleapis.com/v1/accounts:signUp"
---

## 3.1 Parameter Request

Pada bagian **Params**, tambahkan parameter berikut:

| Key | Value |
|----|----|
| key | {{firebase_api_key}} |

![Params SignUp](tugas/sign-up-1.png)

---

## 3.2 Header Request

Pada bagian **Headers**, tambahkan konfigurasi berikut:

| Key | Value |
|----|----|
| Content-Type | application/json |

![Header SignUp](tugas/gambar5.png)

---

## 3.3 Body Request

Gunakan format **JSON** pada body request.

Contoh nilai yang dimasukkan ke dalam body: email, password, dan returnSecureToken

![Body SignUp](tugas/sign-up-2.png)
















