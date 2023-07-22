# Predict-User-Credit-Card-Payments-Using-Classification-Models
Objective :
This project aims to predict customers based on previous payments to classify whether customers will fail to pay in the next month's payments or not

Latar belakang masalah :
Dalam menghadapi risiko pembayaran terlambat, perusahaan membutuhkan informasi yang akurat untuk mengelola risiko dengan lebih baik. perusahaan dapat mengidentifikasi pelanggan yang berpotensi gagal membayar lebih awal. Hal ini akan membantu mengurangi kerugian dan meningkatkan efisiensi dalam pengelolaan risiko.

Data ini berasal dari BigQuery dari database bernama credit_card_default
- data ini terdiri dari 2965 baris dan 24 kolom
- Terdapat beberapa kolom yang mengindikasikan informasi tentang pengguna, seperti jenis kelamin (sex), tingkat pendidikan (education_level), status pernikahan (marital_status), dan usia (age)
- Terdapat kolom default_payment_next_month yang merupakan target prediksi dari model, yaitu apakah pengguna akan mengalami gagal bayar pada bulan berikutnya atau tidak.
- Terdapat juga kolom limit_balance yang menunjukkan batas kredit pengguna

Dari hasil confusion matrix, terlihat bahwa model memiliki kemampuan yang baik dalam memprediksi class 0(tidak akan mengalami keterlambatan pembayaran) dengan akurasi 94% pada true negative (class 0 diprediksi benar) dan 6% false positive (class 0 diprediksi salah). Namun, model memiliki kemampuan yang kurang baik dalam memprediksi class 1(akan mengalami keterlambatan pembayaran, hanya memiliki akurasi 40% pada true positive (class 1 diprediksi benar) dan 60% false negative (class 1 diprediksi salah)

Model yg digunakan adalah Logistic Regression, SVM, Decision Tree, K-Neighbors (KNN), Naive Bayes, Random Forest dan Gradient Boosting
serta menggunakan Cross Validation untuk menentukan model mana yg terbaik digunakan untuk dataset ini
Pegambilan Kesimpulan
- Rata-rata umur nasabah adalah 35 tahun dengan rentang usia antara 21 sampai 69 tahun.
- Rata-rata batas kredit nasabah adalah 163,369.31. Nilai minimum adalah 10,000 dan nilai maksimumnya adalah 800,000.
- Rata-rata tagihan bulanan nasabah pada bulan ke-3 sampai ke-6 adalah lebih tinggi dibandingkan bulan sebelumnya.
- Rata-rata jumlah pembayaran nasabah pada bulan ke-1 sampai ke-3 lebih rendah dibandingkan bulan berikutnya.
- Proporsi nasabah yang mengalami default payment next month adalah sekitar 21%.
- Mayoritas nasabah berjenis kelamin wanita.
- Mayoritas nasabah memiliki pendidikan level 2.
- Mayoritas nasabah sudah menikah.
- Rata-rata nilai pay_0 dan pay_2 adalah mendekati 0, yang menunjukkan mayoritas nasabah membayar tagihan mereka pada waktu yang tepat.
- Sedangkan nilai pay_5 dan pay_6 cenderung negatif, yang berarti sebagian besar nasabah melakukan pembayaran keterlambatan pada bulan tersebut.
- mayoritas wanita yg melakukan default_payment_next_month ada 373 orang
- pendidikan level 2 memiliki jumlah terbanyak, yaitu sekitar 1400 untuk melakukan default_payment_next_month
- maritas status tertinggi berada di class 2 untuk default_payment_next_month class 1 memiliki jumlah 1600
- limit saldo kredit tertinggi berada di 800000 tetapi mayoritas nasabah hanya menggunakan sampai 500000
- sebagian besar nasabah memiliki tagihan yang relatif kecil atau bahkan tidak memiliki tagihan pada bulan tersebut. Hal ini dapat menjadi indikasi bahwa sebagian besar nasabah cenderung membayar tagihan kredit mereka secara tepat waktu
- sebagian besar nasabah melakukan pembayaran dalam jumlah yang relatif kecil. Hal ini juga terbukti bahwa nilai rata-rata pembayaran pada setiap bulan cenderung lebih rendah dari batas kredit yang diberikan pada nasabah
- setelah di pilih menggunaka cross validation, model terbaik adalah gradient boosting
- hyperparameter yg digunakan adalah gridsearch, tetapi antara sebelum dan sesudah di tuning, hasilnya sama, hanya saja untuk ROC AUC score mengalami penurunan setelah tuning
- ketika mencoba menggunakan SMOTE, hasilnya untuk kelas minoritas terdapat peningkatan
- setelah memasukan data infarence, data baru telah terklasifikasi masuk ke class 0 yg artinya tidak akan mengalami keterlambatan pembayaran
- Kelebihannya adalah model dapat mengklasifikasi model dengan baik
- Kekurangannya adalah mencoba mengukur menggunakan metriks lain seperti MSE


