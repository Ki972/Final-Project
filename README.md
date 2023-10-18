# Final Project: Holiday Packages Prediction using Machine Learning
## **by 7 Bola Naga**


![logo 7 bola naga](https://github.com/putrikirey11/Final-Project/assets/131474475/6497a4c8-332c-4b38-9603-62ada401e349)


The Members:
1. Fatimah Azzahra A
2. Fulka Ilmy Avicenna
3. Fenny Experence Rompis
4. Putri Kirey Eki Yogaswari
5. Siti Zahrotul Jannah
6. Bagus Ario Bimo
7. Steve
8. Cholifatur Rohman Dimi Saputra
# Business Understanding
Perusahaan Trips&Travel.com merupakan suatu perusahaan dengan model bisni berbasis customer. Saat ini kami memiliki lima tipe paket tersedia; Basic, Standard, Deluxe, Super Deluxe, dan King. Bersamaan dengan paket yang sudah ada kami juga berencana untuk meluncurkan paket baru yang bernama 'Wellness Tourism Package'.
# Problem Statement
Hanya 19% customer yang melakukan pembelian package pada tahun lalu.
Ini menunjukkan bahwa targeting pelanggan yang tidak tepat atau bahkan tidak ada tageting pelanggan yang dilakukan, mengakibatkan tingginya pengeluaran biaya marketing.
# Goal
Effective customer targeting berdasarkan karakter customer yang dapat menurunkan biaya marketing
# Objective
Membuat model machine learning yang dapat memprediksi customer yang berpotensi membeli package dengan memanfaatkan data pelanggan yang tersedia di perusahaan. 
# Business Metric 
Conversion Rate
# Tools
Alat yang kami gunakan dalam proyek ini yaitu Jupyter Notebook dan Google Colab.
# Contents
## Exploratory Data Analysis (EDA)
Data tersebut memiliki jumlah kolom 20 columns,dan bari 4888 row. Terdapat beberapa kolom yang memiliki missing value, yaitu kolom-kolom dengan jumlah baris yang kurang dari 4888, dan mempunyai type data int64, float64, serta object.

Terdapat data yang kosong (missing value) pada beberapa kolom data tersebut, seperti kolom : 
- Age,
- TypeofContact,
- DurationOfPitch,
- NumberOfFollowups,
- PreferredPropertyStar,
- NumberOfTrips,
- NumberOfChildrenVisiting,
- MonthlyIncome

Untuk type data dari data yang dimiliki sudah sesuai, terdapat 2 jenis type data dalam data tersebut yaitu:
- Numeric(Type int dan float): CustomerID, ProdTaken, Age, CityTier, DurationOfPitch, NumberOfPersonVisiting, NumberOfFollowups, PreferredPropertyStar, NumberOfTrips, Passport, PitchSatisfactionScore, OwnCar, NumberOfChildrenVisiting, MonthlyIncome.
- Categorical(type data object): TypeofContact, Occupation, Gender, ProductPitched,MaritalStatus, Designation.
## Univariate Analysis
## Numerical Features
- Pada fitur ProdTaken DurationOfPitch NumberOfPersonVisiting terdapat 1 outlier
- pada fitur NumberOfFollowups terdapat 2 outlier
- pada fitur NumberOfTrips terdapat 5 outlier
- pada fitur MonthlyIncome terdapat 4 outlier
- Age : Distribusi normal
- DurationOfPitch NumberOfTips MonthlyIncome : Positively Skewed
- OwnCar Passport ProdTaken : Bimodal
- NumberOfPersonVisiting City Tier PreferredPropertyStar: Trimodal
## Categorical Features
- Pada fitur Occupation kategori Free lancer mengalami ketimpangan, hal ini dapat menyebabkan bias dalam interpretasi hasil. Maka sebaiknya kita melakukan transformasi data pada tahap pre-processing.
- Pada fitur MaritalStatus kategori Unmarried dengan Single dapat diasumsikan sama, sehingga pada proses preprocessing dapat di gabung menjadi 1 kategorik saja.
- Terdapat keselahan penulisan pada fitur Gender, 'Fe Male' yang menyebabkan terbagi dua-nya value pada 'Female'
## Multivariate Analysis
- Kolom Age dengan DurationOfPitch dan NumberOfFollowups memiliki korelasi negatif lemah
- Kolom Age memiliki nilai korelasi positif tinggi (mendekati 0.7), nantinya dapat digabung menjadi fitur baru
- Kolom MonthlyIncome memiliki korelasi negatif lemah terhadap kolom DurationOfPitch
## Data Pre-Processing
## Data Cleansing
Pada tahap ini dilakukan Handling Missing Values, Handling Incosistent Data, dan Handling Duplicate Data
## Business Insight

**Conversion Rate on Gender**
![1](https://github.com/putrikirey11/Final-Project/assets/131474475/8e4a8fb2-4929-4ef9-8686-0270872dedc1)
Jika dibandingkan berdasarkan gender maka dapat dilihat bahwa Male lebih cenderung membeli produk tersebut dibandingkan dengan female. Lebih lanjut Male memiliki porsi sebesar 53,3% diatas female yang memiliki 46,7%.

**Conversion Rate on Type of Contact**
![2](https://github.com/putrikirey11/Final-Project/assets/131474475/ddea6feb-6769-4892-95ea-9241de2ac660)
Jika dibandingkan berdasarkan Type of Contact maka dapat dilihat bahwa Company Invited lebih banyak membeli produk tersebut dibanding self inquiry. Company invited memiliki porsi sebesar 54,7% diatas Self Enquiry yang memiliki 45,3%.

**Conversion Rate on Occupation**
![3](https://github.com/putrikirey11/Final-Project/assets/131474475/4be970c6-89ae-44be-99ff-5d1c98eebe11)
Jika dibandingkan berdasarkan Occupation maka dapat dilihat bahwa Free Lancer memiliki 100% product purchase, jauh diatas dibandingkan dengan Large Business, Salaried dan Small Business. Free Lancer sendiri memiliki pangsa pasar sebesar 61.1% lebih besar dari pangsa pasar gabungan Large Business, Salaried dan Small Business.

**Conversion Rate on Age**
![4](https://github.com/putrikirey11/Final-Project/assets/131474475/e0120bf2-4fc8-455f-91ba-1132b105884a)
kelompok usia yang memiliki presentase terbesar untuk mengambil produk setelah pitch produk oleh sales adalah kelompok usia 18-29 tahun (32.1%). "Travel&Trips.com" dapat lelbih berfokus pada kelompok usia ini untuk pitch product terbaru mereka untuk merendahkan cost marketing.

## Modelling & Evaluation
## Model Comparison

<img width="417" alt="Screenshot 2023-10-19 at 00 48 46" src="https://github.com/putrikirey11/Final-Project/assets/131474475/374746e0-088c-438d-ac8b-40d80fc405e0">

Dengan mencoba 5 algoritma model di atas, nilai akurasi dan precision paling tinggi diperoleh oleh Decision Tree dengan akurasi 90% dan precision 95%.

## Decision Tree & Hyperparameter Tuning

<img width="226" alt="Screenshot 2023-10-19 at 00 50 52" src="https://github.com/putrikirey11/Final-Project/assets/131474475/f2a7d0bd-a10c-4e7b-90a5-060ad7d9eaa6">

**Confusion Matrix**

![Picture1](https://github.com/putrikirey11/Final-Project/assets/131474475/81a70573-6ea1-4be2-aa66-49c88e93c4ec)

## Feature Importance

![6](https://github.com/putrikirey11/Final-Project/assets/131474475/4e2f572e-70fb-4a97-9f7d-4ed83ccbbc0f)

Jumlah penghasilan berpengaruh terhadap keputusan customer untuk membeli package. Calon customer yang sudah memiliki paspor atau yang duration of pitch nya lebih lama memiliki probabilitasnya yg lebih tinggi untuk membeli package. 

## Shap Values

![7](https://github.com/putrikirey11/Final-Project/assets/131474475/4a866414-4a23-42e9-83ee-17b2ba6cc3bd)

Fitur Passport memiliki kontribusi yang tinggi dalam membuat prediksi. Hal ini menunjukkan bahwa status memiliki paspor dapat mempengaruhi hasil dari pitch penjualan. Mungkin ada faktor-faktor terkait perjalanan atau mobilitas yang mempengaruhi minat atau kemampuan seseorang untuk membeli produk.

# Business Recommendations
Recommend Customer Type:
- > 22 menit Duration Of Pitch
- Lower Middle Monthly Income ($11.000 - $20.000)
- Memiliki Passport
- Preferred Property dengan Star 5
- Belum Menikah
# Conversion Rate
Perhitungan Conversion Rate menggunakan hasil TP dan FP dari confusion matrix yang digunakan setelah melakukan tuning hyperparameter. Disimpulkan dari hasil conversion rate sebelum dan sesudah terdapat kenaikan sebesar 50.3%.
# Simulation
Asumsi paket akan di tawarkan kepada 1000 customer dengan harga paket yang sama dan budget marketing yang sama (menggunakan paket Basic ($100)). Dengan model yang telah dibuat, dapat menaikan Gross Sales sampai $50,300 atau sebesar 259%. Oleh karena itu model ini dapat direkomendasikan untuk mencari pelanggan baru.
## Marketing Costs
Average range telemarketing costs per calls $2.4 - $5.6 (median -> $4.15)

Dengan model yang telah dibuat, dapat mengurangi biaya marketing sebesar $3,253 .6 atau sebesar 80.33%. Oleh karena itu model ini dapat direkomendasikan untuk melakukan pitching produk terhadap customer yang sudah ada.
