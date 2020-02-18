![test](/screenshot/CSV_Writer_setting.JPG)

big_data_tugas1

Business Understanding

##### Data Understanding
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

##### Data Preparation

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

##### Modeling

Jelaskan proses membaca data dari dua sumber yang berbeda

Jelaskan proses modeling (join atau append) yang dilakukan beserta setting node pada KNIME

##### Evaluation

Jelaskan apakah hasil join atau append berhasil

##### Deployment
```
Proses deployment dilakukan dengan menyimpan data hasil append sebelumnya ke dalam tabel database dan file csv.
Untuk penyimpanan data ke dalam tabel pada database maka sebelum itu kita harus membuat tabel tujuan dan menyetting format dan nama kolomnya
Untuk penyimpanan data ke dalam file CSV maka pertama kali harus dibuat file CSV kosong lalu file hasil append tersebut akan disimpan pada file CSV tersebut
```
Simpan hasil join append ke dalam file dan database
