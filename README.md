# Big Data
## Tugas 1

### Business Understanding

### Data Understanding
```
jumlah baris data: 303 baris 
makna kolom-kolom yang ada di dalam data:
age       : umur pasien
sex       : jenis kelamin pasien
cp        : tipe chest pain (Terdiri dari 4 tipe)
trestbps  : resting blood pressure
chol      : serum cholestoral in mg/dl 
fbs       : fasting blood sugar > 120 mg/dl
restecg   : resting electrocardiographic results (values 0,1,2)
thalach   : maximum heart rate achieved 
exang     : exercise induced angina 
oldpeak   : ST depression induced by exercise relative to rest 
slope     : the slope of the peak exercise ST segment 
ca        : number of major vessels (0-3) colored by flourosopy 
thal      : 3 = normal; 6 = fixed defect; 7 = reversable defect
target    : 1 : terkena heart disease; 0: tidak terkena heart disease
```

### Data Preparation

```
Data Heart Disease hanya terdiri atas 1 tabel yang berisi 14 kolom maka dari data tersebut bisa dilakukan proses append.
Dari data awal yang tersebut saya split data menjadi 2 bagian masing-masing berisi 7 kolom. Proses splitting tersebut menggunakan excel. 
```
```
Dari excel tersebut 7 kolom awal saya simpan ke dalam database. Untuk proses memasukkan ke dalam database saya ubah file hasil splitting tersebut ke dalam CSV lalu dengan bantuan HeidiSQL saya import file CSV tersebut ke dalam database 
```
![test](/screenshot/DB_split.JPG)
```
sedangkan 7 kolom berikutnya disimpan ke dalam bentuk CSV 
```
![test](/screenshot/CSV_split.JPG)

### Modeling

![test](/screenshot/workflow.JPG)
#### Proses membaca dari CSV
![test](/screenshot/CSV_Reader_setting.JPG)
```
menggunakan CSV Reader dengan setting sebagai berikut:
- Pilih File CSV yang akan dibaca
- Karena file tersebut memiliki header maka centang option "Has Column Header"
- Klik apply
```

#### Proses membaca dari Database
![test](/screenshot/SQL_Connect_setting.JPG)
```
Pertama, buat koneksi dengan database sesuai langkah-langkah berikut:
1. Pilih MySQLConnector
2. Lakukan configuration khusus dengan memasukkan Hostname, Database name, Username, dan Password sesuai gambar diatas
3. Klik Apply
4. Jalankan MySQLConnector
```
![test](/screenshot/DB_Selector_setting.JPG)
```
Kedua, Pilih table mana yang akan dibaca pada database sesuai langkah-langkah berikut:
1. Pilih DB Table Selector
2. Sambungkan dengan MySQLConnector yang telah disetting sebelumnya
3. Pilih table mana yang diinginkan dan Schema nya
4. Klik Apply
5. Jalankan DB Table Selector
```
![test](/screenshot/DB_Reader_setting.JPG)
```
Kedua, Pilih table mana yang akan dibaca pada database sesuai langkah-langkah berikut:
1. Pilih DB Reader
2. Sambungkan dengan DB Table Selector yang telah disetting sebelumnya
3. Jalankan DB Reader
```
![test](/screenshot/Append_setting.JPG)
```
Setelah data dari CSV dan Database dapat dibaca maka selanjutnya adalah proses menggabungkan dua data tersebut menjadi satu.
```

Jelaskan proses modeling (join atau append) yang dilakukan beserta setting node pada KNIME

### Evaluation

Jelaskan apakah hasil join atau append berhasil

### Deployment
```

Proses deployment dilakukan dengan menyimpan data hasil append sebelumnya ke dalam tabel database dan file csv.
Untuk penyimpanan data ke dalam tabel pada database maka sebelum itu kita harus membuat tabel tujuan dan menyetting format dan nama kolomnya
Untuk penyimpanan data ke dalam file CSV maka pertama kali harus dibuat file CSV kosong lalu file hasil append tersebut akan disimpan pada file CSV tersebut
```
Simpan hasil join append ke dalam file dan database
