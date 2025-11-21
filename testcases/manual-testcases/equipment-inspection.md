Equipment Inspection – Test Scenarios
1. Open Form Builder Page

**TC-FB-01 – Halaman Form Builder terbuka (Positive)**

Step:
- Login ke web / app
- Buka menu Form Builder

Expected:
- Berhasil masuk ke halaman Equipment Inspection Form
- Menampilkan daftar form
- Tombol untuk membuat form baru muncul

Prioritas: High

------------------------------------------------------------------------------------------------

2. Create New Form

**TC-FB-02 – Membuat form baru (Positive)**

Step:
1. Klik Create Form
2. Input form yang tersedia
3. Klik button Submit

Expected:
- Form baru berhasil dibuat
- Form equipment inspection berhasil tersimpan
- Form muncul dalam list form builder

Prioritas: High

------------------------------------------------------------------------------------------------

3. Add Field Types

**TC-FB-03 – Tambahkan Input Text (Positive)**

Expected:
- Field Text dapat dibuat dan disimpan
- Label dan mandatory flag tersimpan

------------------------------------------------------------------------------------------------

**TC-FB-04 – Tambahkan Date Picker (Positive)**

Expected:
- Field Date dapat ditambahkan
- Format tanggal sesuai

------------------------------------------------------------------------------------------------

**TC-FB-05 – Tambahkan Select (Positive)**

Expected:
- Pilihan dropdown dapat ditambahkan
- Opsi-opsi dapat disimpan

------------------------------------------------------------------------------------------------

**TC-FB-06 – Tambahkan Radio (Positive)**

Expected:
- Radio dapat dibuat (max 4 opsi)
- Muncul semua opsi

------------------------------------------------------------------------------------------------

**TC-FB-07 – Tambahkan Image Picker (Positive)**

Expected:
- Field Image Picker tampil pada preview form

------------------------------------------------------------------------------------------------

4. Validate Maximum Field Count

**TC-FB-08 – Lebih dari 50 field (Negative)**

Step: 
- Tambahkan field lebih dari 50 field

Expected:
- Gagal menambahkan field
- Menampilkan Error message “Maximum 50 fields per form”

Prioritas: High

------------------------------------------------------------------------------------------------

5. Save Form

**TC-FB-09 – Form berhasil disimpan (Positive)**

Step:
- Tambahkan beberapa field
- Klik button Submit

Expected:
- Form berhasil tersimpan
- Aplikasi menampilkan error message sukses/berhasil

Prioritas: High

------------------------------------------------------------------------------------------------

**TC-FB-10 – Gagal save karena internet mati (Negative)**

Step:
- Input form
- Matikan koneksi internet
- Klik button Submit

Expected:
- Menampilkan error message tidak ada koneksi
- Form gagal tersimpan

Prioritas: Medium

------------------------------------------------------------------------------------------------

1. Open Equipment Inspection Page

**TC-EI-01 – Halaman list inspection terbuka (Positive)**

Step :
1. Klik menu Equipment Inspection

Expected:
- Berhasil masuk ke halaman Equipment Inspection
- Riwayat submission tampil
- Menampilkan button “New Inspection”

------------------------------------------------------------------------------------------------

2. Select Form Code

**TC-EI-02 – Form Code muncul (Positive)**

Expected:
- List Form Code dari backend berhasil tampil
- User bisa memilih salah satu form

------------------------------------------------------------------------------------------------

3. Dynamic Form Load

**TC-EI-03 – Field dinamis berhasil dimuat (Positive)**

Step:
1. Pilih Form Code
2. Aplikasi memuat field berdasarkan konfigurasi form builder

Expected:

Field tampil sesuai definisi:
- Text field
- Date Picker
- Select/dropdown field
- Radio button
- Image Picker
- Urutan field sesuai form builder
- Mandatory flag bekerja

------------------------------------------------------------------------------------------------

**TC-EI-04 – Field gagal dimuat (Negative)**

Expected:
- Menampilkan error message
- User tetap di halaman form

------------------------------------------------------------------------------------------------
