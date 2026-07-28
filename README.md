# Dokumentasi Foto IoT SmartFarm Aquaculture

<table>
<tr>
<td align="center" width="50%">

### Prototype Pelontar Pakan
<img src="https://github.com/user-attachments/assets/a33e8026-c8cd-485c-bee2-1cd77a854ed2" width="350"/>

</td>
<td align="center" width="50%">

### Prototype Aerator
<img src="https://github.com/user-attachments/assets/b30d1d2e-2aeb-4f3c-927e-517298c54c8d" width="350"/>

</td>
</tr>

<tr>
<td align="center">

### Prototype Sensor
<img src="https://github.com/user-attachments/assets/a55051ca-82d3-4f64-a586-63092ed455d3" width="350"/>

</td>
<td align="center">

### Gambaran Rangkaian Sistem Smart Aquaculture
<img src="https://github.com/user-attachments/assets/76588949-4db7-420d-b6dc-25eb47c2eefc" width="350"/>

</td>
</tr>
</table>


# Link Vidio Demo Aplikasi SmartFarm Aquaculture
Link GDrive : https://drive.google.com/drive/folders/1ustF-T44Lzk9xnpRewehroSwVmLbxCfB?usp=sharing

# Desain Figma SmartFarm Aquaculture App
Link Figma High Fidelity : https://www.figma.com/design/HrD9DUBxa3wY8k8kyggjcA/High-Fidelity---Aplikasi-Sadewa-SmartFarm?node-id=0-1&t=bLOjM4lI8JK7XekC-1

# Tools & Teknologi SmartFarm Aquaculture App

- **Express.js** (Backend Framework)
- **MongoDB** (Database NoSQL untuk menyimpan data)
- **Firebase Realtime Database** (Integrasi realtime data IoT)
- **Flutter** (Frontend mobile apps)
- **VS Code** (Development Environment Backend)
- **Android Studio** (Development Environment Frontend)


## SmartFarm Aquaculture Backend

Repository ini merupakan backend service untuk aplikasi **Sadewa Smart Farm** yang dibangun menggunakan **Node.js (Express.js)** dan berfungsi sebagai jembatan antara aplikasi Flutter dan layanan database seperti **Firebase Realtime Database** serta **MongoDB**.


### Instalasi

---

Clone the repositori

```bash
  git clone https://github.com/121140084-Rizki-Esa-Fadillah/Sadewa_SmartFarm.git
```

Navigate ke directori

```bash
  cd Sadewa_SmartFarm/backend
```

Install dependencies

```bash
  npm install
```


### Setup Environment

Buat file .env di direktori root dan tambahkan konfigurasi berikut:

`PORT`=5000

`MONGO_URI`=mongodb+srv://<user>:<password>@<cluster>.mongodb.net/<dbname>?retryWrites=true&w=majority

`JWT_SECRET`=your_jwt_secret_key

`EMAIL_HOST`=smtp.your-email-provider.com

`EMAIL_PORT`=465

`EMAIL_USER`=your-email@example.com

`EMAIL_PASS`=your-email-password


### Tambahkan FIle Firebase

Tambahkan file firebase-admin.json ke direktori root. File ini dapat diunduh dari:

`Firebase Console > Project Settings > Service Accounts > Generate New Private Key`


### Jalankan Server

```bash
  node server.js
```


## SmartFarm Aquaculture Frontend

Pada file `api_service.dart` terdapat base URL API yang menghubungkan antara backend dengan frontend.

Secara default, backend telah dideploy ke platform Railway dengan base URL production sebagai berikut:

`static const String baseUrl = "https://backendsmartfarm-production.up.railway.app/api";`

Untuk penggunaan di perangkat lain seperti smartphone untuk keperluan testing dapat menggunakan URL:

`static const String baseUrl = "http://<IP Lokal>/api";`



### Cara Mengetahui IP Lokal

Untuk mengakses backend dari perangkat lain seperti HP (misalnya saat testing Flutter), Anda perlu mengetahui IP lokal dari komputer yang menjalankan backend.


### 🖥️ Windows

Buka **Command Prompt** lalu jalankan perintah berikut:

```bash
ipconfig
```

Cari bagian seperti ini:

```bash
Wireless LAN adapter Wi-Fi:

   IPv4 Address. . . . . . . . . . . : 192.168.xx.xx
```

Gunakan IP tersebut dalam URL Anda, misalnya:

`static const String baseUrl = "http://192.168.xx.xx:5000/api";`


### 🖥️ MAC/Linux

Buka Terminal dan jalankan salah satu perintah berikut:

```bash
ifconfig
```

atau

```bash
hostname -I
```

Hasilnya akan menampilkan IP lokal seperti:

```bash
192.168.xx.xx
```

## Akses Aplikasi SmartFarm Aquaculture


Pengguna dapat mengakases aplikasi dengan Root User sebagai berikut:

Role Admin

`Username`: OwnerTambak

`Password`: Admin@123

Role User

`Username`: PekerjaTambak

`Password`: User@123
