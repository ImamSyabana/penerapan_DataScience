# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Jaya Jaya Maju

## Business Understanding

**Jaya Jaya Maju** adalah perusahaan multinasional yang telah berdiri sejak tahun 2000 dengan lebih dari 1000 karyawan yang tersebar di seluruh penjuru negeri. Meskipun telah berkembang selama lebih dari dua dekade, perusahaan tersebut masih mengalami kesulitan dalam mengelola karyawan, yang berdampak pada tingginya angka attrition rate (lebih dari 10%). Manajemen perusahaan bagian departemen HR berkomitmen untuk menurunkan attrition rate ini agar tidak semakin parah, Maka dari itu, diperlukan bantuan untuk identifikasi faktor-faktor yang memengaruhi tingginya angka karyawan yang keluar. Faktor yang memengaruhi tingkat attrition pegawai dapat ditemukan melalui analisis data-data berikut.

* **EmployeeId** - Employee Identifier
* **Attrition** - Did the employee attrition? (0=no, 1=yes)
* **Age** - Age of the employee
* **BusinessTravel** - Travel commitments for the job
* **DailyRate** - Daily salary
* **Department** - Employee Department
* **DistanceFromHome** - Distance from work to home (in km)
* **Education** - 1-Below College, 2-College, 3-Bachelor, 4-Master,5-Doctor
* **EducationField** - Field of Education
* **EnvironmentSatisfaction** - 1-Low, 2-Medium, 3-High, 4-Very High
* **Gender** - Employee's gender
* **HourlyRate** - Hourly salary
* **JobInvolvement** - 1-Low, 2-Medium, 3-High, 4-Very High
* **JobLevel** - Level of job (1 to 5)
* **JobRole** - Job Roles
* **JobSatisfaction** - 1-Low, 2-Medium, 3-High, 4-Very High
* **MaritalStatus** - Marital Status
* **MonthlyIncome** - Monthly salary
* **MonthlyRate** - Mounthly rate
* **NumCompaniesWorked** - Number of companies worked at
* **Over18** - Over 18 years of age?
* **OverTime** - Overtime?
* **PercentSalaryHike** - The percentage increase in salary last year
* **PerformanceRating** - 1-Low, 2-Good, 3-Excellent, 4-Outstanding
* **RelationshipSatisfaction** - 1-Low, 2-Medium, 3-High, 4-Very High
* **StandardHours** - Standard Hours
* **StockOptionLevel** - Stock Option Level
* **TotalWorkingYears** - Total years worked
* **TrainingTimesLastYear** - Number of training attended last year
* **WorkLifeBalance** - 1-Low, 2-Good, 3-Excellent, 4-Outstanding
* **YearsAtCompany** - Years at Company
* **YearsInCurrentRole** - Years in the current role
* **YearsSinceLastPromotion** - Years since the last promotion
* **YearsWithCurrManager** - Years with the current manager


### Permasalahan Bisnis

1. **Tingginya angka attrition**: Perusahaan Jaya Jaya Maju menghadapi attrition rate lebih dari 10%, yang mengganggu stabilitas dan efektivitas operasional perusahaan.
2. **Ketidakpastian faktor penyebab attrition**: Perusahaan belum memahami secara mendalam faktor-faktor apa saja yang paling berpengaruh menyebabkan banyak karyawan keluar. Maka dari itu, akan diteliti tentang semua hal yang sekiranya dapat menyebabkan attrition rate meningkat, seperti kurangnya promosi jabatan pegawai, frekuensi kepindahan tempat kerja pegawai sebelumnya, dampak overtime terhadap level work life balance, frekuensi peningkatan gaji, rentang usia, tingkat kepuasan pegawai terhadap pekerjaan, lingkungan, dan relasi, atau dari segi jarak antara kantor dengan rumah.

### Cakupan Proyek

Proyek ini akan mencakup:
1. Mengidentifikasi variabel-variabel yang paling memengaruhi keputusan karyawan untuk keluar.
2. Menganalisis data yang diperoleh dari divisi HR untuk memahami pola dan tren attrition.
3. Membuat dashboard yang membantu manajemen dalam memahami informasi penting terkait attrition.

### Persiapan

Sumber data: Data berasal dari informasi masing-masing pegawai yang dikumpulkan oleh divisi Human Resource (HR) perusahaan Jaya Jaya Maju.

Setup environment:

* Setup IDE Google Colab untuk dapat menulis dan menjalankan model machine learning atau analisis data langsung di Google Colab, memanfaatkan CPU atau GPU yang disediakan secara gratis

1. Akses Google Colab: Membuka Google Colab lewat browser.
2. Dataset hasil analisis faktor-faktor yang memengaruhi attrition rate menggunakan Google Colab dapat diunggah ke database management tool PostgreSQL menggunakan supabase untuk nantinya bisa digunakan untuk membuat dashboard menggunakan metabase.

* Setup Metabase dan Docker 
1. **Install Docker**: Docker bisa diunduh dari website resminya dan dapat di instal dengan mengikuti langkah-langkah yang ditampilkan.

2. **Setup Metabase**: Menggunakan Metabase untuk membuat dashboard yang interaktif dan terhubung ke database. Menyiapkan metabase dengan menggunakan Docker dilakukan dengan perintah docker pull metabase/metabase:v0.46.4 dan jalankan metabase dengan menggunakan perintah docker run -p 3000:3000 --name metabase metabase/metabase

 * Menghubungkan ke Supabase

1. **Upload CSV ke Supabase**: Menggunakan Supabase untuk menyimpan data attrition rate yang sudah disiapkan dengan melakukan feature engineering sebelumnya ke data base agar bisa diakses oleh Metabase. Untuk dapat menggunakan supabase perlu disiapkan terlebih dahulu akun user yang akan digunakan untuk mengakses supabase yang mana juga terdapat opsi menggunakan akun GitHub. Selanjutnya projek baru perlu dibuat dengan mendefinisikan nama, organisasi, dan password. Setelah itu didapatkan username dan password untuk projek ini adalah **postgres.uxzwesijexuasxnywyuf** dan **52H9suDMxF5lWrjq**. Password dan username tersebut dibutuhkan saat akan mengirim data hasil feature engineering ke supabase untuk masuk ke databse PostgreSQL.
   
2.  **Menghubungkan Metabase dengan Supabase**:
Untuk dapat mengolah database PostgreSQL yang ada pada Supabase, diperlukan pengaturan pada metabase dengan memberikan informasi database yang sama dengan yang sudah dikirim ke supabase tersebut. Informasi yang perlu dimasukkan meliputi tipe databse, yaitu PostgreSQL, host, port, database name, username, dan password. Username dadn password yang dipilih untuk menggunakan metabase, yaitu **root@mail.com** dan **root123**. 


### Business Dashboard

Business dashboard dibuat menggunakan Metabase, yang menampilkan beberapa informasi penting terkait faktor-faktor yang berkontribusi pada attrition di perusahaan. Dashboard tersebut menunjukkan bahwa:

Karyawan yang paling berisiko berhenti adalah mereka yang berumur antara 26-35 tahun.
Jarak rumah ke kantor juga menjadi faktor penting, dengan karyawan yang tinggal dalam jarak 0-5 km dari kantor memiliki tingkat attrition yang lebih tinggi.
Ketiga, alasan yang menyebabkan attrition rate meningkat adalah kerja lembur (overtime) yang dikombinasikan dengan rendahnya tingkat work-life balance berperan signifikan dalam menyebabkan karyawan keluar dari perusahaan.
Dashboard ini membantu manajemen untuk memahami distribusi dan tren attrition, serta memungkinkan pengambilan keputusan yang lebih baik dalam hal perbaikan work-life balance dan kebijakan lembur.

### Conclusion
Proyek ini berhasil mengidentifikasi beberapa faktor utama yang berkontribusi terhadap tingginya tingkat attrition di perusahaan Jaya Jaya Maju. Faktor-faktor seperti usia, jarak rumah ke kantor, dan lembur dengan work-life balance yang rendah adalah penyebab utama mengapa karyawan berhenti. Dengan menggunakan business dashboard, manajemen dapat memahami pola-pola ini dan membuat langkah-langkah strategis untuk menurunkan attrition rate. Beberapa rekomendasi meliputi peninjauan kembali kebijakan lembur, sosialisasi kepada pegawai tentang cara meningkatkan keseimbangan antara pekerjaan dan aktivitasi kehidupan pribadi, serta perhatian khusus kepada kelompok umur yang lebih rentan.
