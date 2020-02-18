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

Jelaskan proses splitting data menjadi dua bagian

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
