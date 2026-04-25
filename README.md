# Ramein - Event Management System (Frontend)

Ramein adalah platform manajemen kegiatan digital yang dirancang untuk mengotomatisasi siklus hidup acara, mulai dari publikasi, manajemen peserta, hingga sistem sertifikasi otomatis.

## Tech Stack

* **Runtime:** Node.js (v18+)
* **Framework:** Express.js with TypeScript
* **Database:** PostgreSQL
* **ORM:** TypeORM
* **Security:** JWT (Access & Refresh Token), RBAC, CORS Whitelisting
* **Services:** Nodemailer (OTP & Notifications)
* **DevOps:** Docker, Railway (Deployment)

## Core Features

### Security & Authentication
* **Identity Management:** Autentikasi berbasis JWT dengan mekanisme refresh token.
* **Access Control:** Role-Based Access Control (RBAC) untuk memisahkan hak akses User dan Admin.
* **Verification:** Sistem verifikasi email berbasis OTP dan prosedur reset password yang aman.

### Event & Participant Management
* **Event Lifecycle:** Manajemen CRUD event dengan validasi jadwal (H-3) dan sistem publikasi.
* **Discovery:** Fitur pencarian dan filter berdasarkan kategori, rentang tanggal, dan harga.
* **Attendance:** Pelacakan kehadiran (attendance tracking) secara real-time untuk setiap peserta.
* **Data Handling:** Fitur bulk import peserta melalui file Excel/CSV.

### Certification System
* **Automated Generation:** Pembuatan sertifikat otomatis dalam format PDF dengan template custom.
* **Validation:** Verifikasi keaslian sertifikat menggunakan sistem QR Code dan metadata unik.
* **Revocation:** Sistem pencabutan sertifikat jika terjadi pembatalan status peserta.

### Admin & Analytics
* **Dashboard:** Ringkasan statistik performa event, statistik user, dan metrik kehadiran.
* **Reporting:** Ekspor data laporan (bulanan/per event) ke format Excel, CSV, atau PDF.

## Project Structure

```text
src/
├── config/      # Database & Environment configurations
├── controllers/ # Express request handlers
├── entities/    # Data models (TypeORM)
├── middlewares/ # Authentication & validation layers
├── routes/      # API endpoint definitions
├── services/    # Core business logic
└── utils/       # Utility functions & helpers
```

## Setup & Installation

### Prerequisites
* Node.js v18+
* PostgreSQL v12+

### Quick Start
1.  **Clone Repository**
    ```bash
    git clone https://github.com/OwlDane/ramein-backend.git
    cd ramein-backend
    ```
2.  **Install Dependencies**
    ```bash
    npm install
    ```
3.  **Environment Configuration**
    Salin file `.env.example` menjadi `.env` dan lengkapi kredensial database serta SMTP email.
4.  **Database Migration**
    ```bash
    npm run db:setup
    ```
5.  **Run Development Server**
    ```bash
    npm run dev
    ```

## API Documentation
Dokumentasi API lengkap dapat diakses melalui:
* **Swagger:** `/api/docs` (jika diaktifkan)
* **Postman Collection:** Tersedia pada folder `docs/` di repositori ini.

## License
Project ini dilisensikan di bawah **ISC License**.

---
