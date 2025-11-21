Flow 2 – Safety Hazard Report

**A. Hazard Reporting (Mobile App)**
TC-HR-01 – Open Hazard Menu (Positive)
Expected:
- Berhasil masuk ke menu hazard
- Menampilkan list hazard
- Menampilkan button “Report Hazard”

**TC-HR-02 – Hazard List Empty (Positive)**
Step:
1. Buka menu Hazard pada akun yang belum pernah membuat laporan
Expected:
- Menampilkan state “No hazard reports yet”
- Tetap ada tombol “Report Hazard”
Prioritas: Low

**TC-HR-03 – Hazard List Loaded with Pagination/Infinite Scroll (Positive)**

Step:
1. Scroll list hingga bawah
Expected:
- Sistem load data berikutnya (pagination/infinite list)
Prioritas: Medium


**TC-HR-04 – Failed to Load Hazard List (Negative)**

Step:
1. Matikan koneksi internet
2. Buka halaman Hazard

Expected:
- Menampilkan error message “Unable to load hazards”
- Retry button tampil
Prioritas: High


**TC-HR-05 – Open Hazard Report Form (Positive)**

Step:
1. Klik tombol “Report Hazard”
Expected:
- Form input tampil dengan semua field:
Location, Sublocation, Area, Area Description, Evidence, PIC
- PIC terisi otomatis dengan reporter
Prioritas: High

**TC-HR-06 – Submit Empty Form (Negative)**
Step:
1. Klik Submit tanpa mengisi field apapun
Expected:
- Error validation muncul pada field mandatory: Location, Sublocation, Area, Evidence, PIC
Prioritas: High

**TC-HR-07 – Missing Location (Negative)**

Step:
1. Isi semua field kecuali Location
Expected:
Menampilkan error message “Location is required”
Prioritas: High

**TC-HR-08 – Missing Sublocation (Negative)**

Step:
1. Isi semua kecuali Sublocation
Expected:
- Menampilkan error message “Sublocation is required”
Prioritas: High

**TC-HR-09 – Missing Area (Negative)**
Step:
1. Isi semua kecuali Area
Expected:
- Menampilkan error message “Area is required”
Prioritas: High

**TC-HR-10 – Missing Evidence (Negative)**

Step:
1. Isi semua field selain Evidence
Expected:
- Menampilkan error message “Evidence is required”
Prioritas: High

**TC-HR-11 – Missing PIC (Negative)**
Step:
1. Hapus PIC yang otomatis terpilih (jika possible)
Expected:
- Menampilkan error message “PIC is required”
Prioritas: Medium


**TC-HR-12 – Successfully Submit Hazard Report (Positive)**

Step:
1. Isi semua mandatory fields
2. Upload image evidence
3. Klik button Submit
Expected:
- Hazard entry dibuat di sistem
- Follow-up task otomatis dibuat
- User redirect kembali ke Hazard list
Prioritas: High

**TC-HR-13 – Evidence Upload Failure (Negative)**

Step:
1. Upload image saat internet mati
Expected:
- Menampilkan error message “Upload failed”
- User tetap di form
Prioritas: Medium


**C. Follow-up Task (PIC)**
**TC-HR-14 – PIC Receives Follow-up Task (Positive)**
Step:
1. Login sebagai PIC
Expected:
- Notifikasi follow-up task muncul
- Task tampil di task list
Prioritas: High


**TC-HR-15 – Submit Follow-up Task (Positive)**

Step:
1. PIC membuka task
2. Input Evidence
3. Input Resolution Date
4. Tambah Co-Observer (optional)
5. Klik button Submit

Expected:
- Task updated to “Resolved”
- Hazard status updated
Prioritas: High


**TC-HR-16 – Missing Resolution Date (Negative)**
Step:
1. Submit follow-up tanpa Resolution Date

Expected:
- Error: “Resolution date is required”
Prioritas: High


**TC-HR-17 – Notification to PIC for Follow-up Task (Positive)**
Precondition:
- Sebuah hazard report telah berhasil dibuat
- Sistem sudah otomatis membuat follow-up task
- PIC sudah ditentukan pada laporan hazard

Step:
1. PIC login ke aplikasi
2. Pastikan device menerima push notification
3. Cek inbox/notification center aplikasi

Expected:
- PIC menerima push notification berisi informasi follow-up task baru
- Notification muncul di device
- Task muncul dalam task list ketika dibuka

Prioritas: High

**TC-HR-18 – Notification to Area Members (Positive)**
Precondition:
- Hazard report dibuat dengan Area = X
- User A, B, C termasuk area X (area members)

Step:
1. Kirim hazard report (oleh reporter)
2. Area members membuka device mereka
3. Cek notification center

Expected:
- Semua user di area tersebut menerima push notification hazard report
- Isi pesan notifikasi relevan (misal: “New hazard reported in your area”)
Prioritas: Medium


**TC-HR-19 – Notification to Supervisor After Follow-up (Positive)**
Precondition:
- Follow-up task telah dibuat dan assigned ke PIC
- Supervisor area telah terdaftar sebagai approver/monitoring role

Step:
1. PIC menyelesaikan follow-up task
2. Submit follow-up form (evidence + resolution date + co observer)
3. Supervisor membuka device
4. Cek notification center

Expected:
- Supervisor menerima notifikasi bahwa follow-up task telah selesai
- Isi notifikasi berisi hazard ID atau summary
Prioritas: Medium
