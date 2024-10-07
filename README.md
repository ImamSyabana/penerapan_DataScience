# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Jaya Jaya Maju

## Business Understanding

**Jaya Jaya Maju** adalah perusahaan multinasional yang telah berdiri sejak tahun 2000 dengan lebih dari 1000 karyawan yang tersebar di seluruh penjuru negeri. Meskipun telah berkembang pesat, perusahaan mengalami kesulitan dalam mengelola karyawan, yang berdampak pada tingginya angka attrition rate (lebih dari 10%). Manajemen perusahaan berkomitmen untuk menurunkan attrition rate ini agar tidak semakin parah, dan memerlukan bantuan untuk mengidentifikasi faktor-faktor yang memengaruhi tingginya angka karyawan yang keluar.

### Permasalahan Bisnis

1. **Tingginya angka attrition**: Perusahaan Jaya Jaya Maju menghadapi attrition rate lebih dari 10%, yang mengganggu stabilitas dan efektivitas operasional perusahaan.
2. **Ketidakpastian faktor penyebab attrition**: Perusahaan belum memahami secara mendalam faktor-faktor apa saja yang menyebabkan karyawan keluar.
3. **Efek negatif pada produktivitas**: Pekerja yang lembur dengan work-life balance yang rendah menjadi perhatian khusus karena mereka rentan untuk keluar dari perusahaan.
4. **Karyawan di usia tertentu lebih rentan**: Karyawan berumur 26-35 tahun teridentifikasi sebagai kelompok dengan risiko tinggi untuk berhenti.

### Cakupan Proyek

Proyek ini akan mencakup:
1. Mengidentifikasi variabel-variabel yang paling memengaruhi keputusan karyawan untuk keluar.
2. Menganalisis data yang diperoleh dari divisi HR untuk memahami pola dan tren attrition.
3. Membuat dashboard yang membantu manajemen dalam memahami informasi penting terkait attrition.
4. Mengusulkan rekomendasi berdasarkan hasil analisis untuk membantu mengurangi angka attrition.

### Persiapan

Sumber data: Data berasal dari divisi Human Resource (HR) perusahaan Jaya Jaya Maju.

Setup environment:

1. **Install Docker**: Menggunakan Docker untuk pengelolaan environment yang konsisten.
2. **Setup Metabase di port 3000**: Menggunakan Metabase untuk membuat dashboard yang interaktif dan terhubung ke database.
3. **Upload CSV ke Supabase**: Menggunakan Supabase sebagai database untuk menyimpan data HR agar bisa diakses oleh Metabase.


* Install Docker
sudo apt-get update
sudo apt-get install docker

* Menjalankan Metabase di Docker
docker run -d -p 3000:3000 --name metabase metabase/metabase

* Menghubungkan ke Supabase
# Upload file CSV ke Supabase dan atur aksesnya agar dapat digunakan oleh Metabase.


### Business Dashboard

Business dashboard dibuat menggunakan Metabase, yang menampilkan beberapa informasi penting terkait faktor-faktor yang berkontribusi pada attrition di perusahaan. Dashboard tersebut menunjukkan bahwa:

Karyawan yang paling berisiko berhenti adalah mereka yang berumur antara 26-35 tahun.
Jarak rumah ke kantor juga menjadi faktor penting, dengan karyawan yang tinggal dalam jarak 0-5 km dari kantor memiliki tingkat attrition yang lebih tinggi.
Kerja lembur (overtime) dikombinasikan dengan rendahnya tingkat work-life balance berperan signifikan dalam menyebabkan karyawan keluar dari perusahaan.
Dashboard ini membantu manajemen untuk memahami distribusi dan tren attrition, serta memungkinkan pengambilan keputusan yang lebih baik dalam hal perbaikan work-life balance dan kebijakan lembur.

### Conclusion
Proyek ini berhasil mengidentifikasi beberapa faktor utama yang berkontribusi terhadap tingginya tingkat attrition di perusahaan Jaya Jaya Maju. Faktor-faktor seperti usia, jarak rumah ke kantor, dan lembur dengan work-life balance yang rendah adalah penyebab utama mengapa karyawan berhenti. Dengan menggunakan business dashboard, manajemen dapat memahami pola-pola ini dan membuat langkah-langkah strategis untuk menurunkan attrition rate. Beberapa rekomendasi meliputi peninjauan kembali kebijakan lembur, peningkatan keseimbangan antara pekerjaan dan kehidupan pribadi, serta perhatian khusus kepada kelompok umur yang lebih rentan.
