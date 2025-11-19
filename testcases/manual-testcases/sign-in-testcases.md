Flow 0 - Sign in

**TC-SI-01 – Username valid (Positive)**

Step:
1. Input username yang terdaftar, lalu lanjutkan.

Expected Result:
- Backend mengembalikan tenant info
- Aplikasi membuka layar login Microsoft

Prioritas: High

-------------------------------------------------------------------------------------------------------------------

**TC-SI-02 – Username tidak terdaftar (Negative)**

Step:
1. Input username tidak valid

Expected Result:
Muncul pesan “User not found”.

Prioritas: High

-------------------------------------------------------------------------------------------------------------------

**TC-SI-03 – Koneksi internet mati (Negative)**

Step:
1. Turn off koneksi internet
2. Input username

Expected Result:
- Request gagal
- Aplikasi menampilkan error message tidak ada koneksi internet
- Tidak melanjutkan ke Microsoft login

Prioritas: High

-------------------------------------------------------------------------------------------------------------------

**TC-SI-05 – Login Berhasil (Positive)**

Step:
1. Input username yang valid
2. Input password yang valid
3. Klik button Sign In

Expected Result:
- User berhasil login melalui Microsoft
- Aplikasi get data profil via endpoint /user/me
- Aplikasi get master data via endpoint /tenant/master
- Aplikasi download / get master data (locations, areas, employees, forms, dll.) sesuai list yang diberikan
- Progress bar berjalan selama proses download master data

Prioritas: High

-------------------------------------------------------------------------------------------------------------------

**TC-SI-06 – Password salah (Negative)

Step:**
1. Input username yang valid
2. Input password yang tidak valid
3. Klik button Sign In

Expected Result: 
- Muncul error dari Microsoft
- User tetap di halaman login Microsoft

Prioritas: High

-------------------------------------------------------------------------------------------------------------------

**TC-SI-07 – Password kosong (Negative)**

Step:
1. Input username yang valid
3. Klik button Sign In

Expected Result: Field password menampilkan error message validation “Password is required”

Prioritas: Medium

-------------------------------------------------------------------------------------------------------------------

**TC-SI-08 – Login gagal 5 kali (Negative)**

Step:

1. Input username yang valid
2. Input password salah dan klik button Sign In sebanyak 5 kali berturut-turut

Expected Result:
Akun terkunci sementara atau muncul error message “Too many attempts, please try again later” (menyesuaikan kebijakan security).

Prioritas: High
