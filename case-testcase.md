**How to Read This Repository**

Repository ini berisi kumpulan test case untuk aplikasi mobile dengan dua kategori utama:
1. Manual Test Cases
2. Automation Test Cases

Struktur folder dibuat sesuai cara kerja saya sebagai QA Engineer, serta mengikuti praktik terbaik dalam penyusunan test documentation.

**manual/**

Berisi test case lengkap yang dilakukan secara manual. Sudah termasuk:
- Step-by-step
- Expected results
- Positive / Negative cases
- Prioritas
- Precondition (optional)

**automation/**

Berisi daftar test case yang dipilih untuk automated testing.
Folder ini hanya memuat judul test case sebagai indikasi coverage automation.
Detail automation akan dibuat dalam tools (misal Katalon), bukan di repo ini.

-------------------------------------------------------------------------------------------------------------------

**Penamaan Test Case**<br>
Penamaan menggunakan pola:<br>
_TC-[FlowCode]-[Nomor] – [Judul] ([Positive/Negative])_

Contoh:<br>
- TC-SI-01 – Username valid (Positive)
- TC-HR-12 – Successfully Submit Hazard Report (Positive)
-------------------------------------------------------------------------------------------------------------------

**Folder automation/** hanya berisi judul test case yang dipilih untuk di-automate, tanpa isi detail.<br>
Tujuan pemisahan ini adalah:<br>
- Menunjukkan test case mana saja yang sesuai untuk automation
- Menjelaskan fokus automation (high priority, regression-prone, stable flow)
- Mempermudah reviewer melihat automation coverage

Automation dipilih berdasarkan kriteria:<br>
- High priority
- Tidak membutuhkan banyak data dynamic
- Stabil dan tidak bergantung pada external system yang unpredictable
- Menjadi bagian dari regressi

**Tools Used**<br>

Manual testing:<br> 
- Test management tools seperti : Jira/Azzure, spreadsheet
- Dbeaver untuk pengecekan data di database menggunakan SQL Query
- Postman API

Automation testing:<br> 
- Katalon Studio
- BDD Cucumber

Repository: <br>
- GitHub / Gitlab


-------------------------------------------------------------------------------------------------------------------
**Author**

Vergi Nardian Lufyandi<br>
QA Engineer (Manual & Automation)
