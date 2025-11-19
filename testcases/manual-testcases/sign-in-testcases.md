Flow 0 - Sign in

**TC-SI-01 – Username valid (Positive)**

Step:
1. Input username yang terdaftar, lalu lanjutkan.

Expected Result:
Sistem menemukan tenant, kemudian layar login Microsoft muncul

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
1. Turn off internet
2. Input username

Expected Result:Sistem menampilkan error koneksi dan tidak melanjutkan.

Prioritas: High

-------------------------------------------------------------------------------------------------------------------

**TC-SI-05 – Password benar (Positive)**
Step:
1. Input username yang valid
2. Input password yang valid
3. Klik button Sign In

Expected Result: User berhasil login dan diarahkan ke dashboard utama sesuai role.

Prioritas: High

-------------------------------------------------------------------------------------------------------------------

**TC-SI-06 – Password salah (Negative)
Step:**
1. Input username yang valid
2. Input password yang tidak valid
3. Klik button Sign In

Expected Result: Sistem menampilkan error message “Incorrect password” dan login gagal

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
