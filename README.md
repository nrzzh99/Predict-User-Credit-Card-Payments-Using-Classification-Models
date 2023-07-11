# Predict-User-Credit-Card-Payments-Using-Classification-Models
This project aims to predict customers based on previous payments to classify whether customers will fail to pay in the next month's payments or not

X. Pegambilan Kesimpulan
- Rata-rata umur nasabah adalah 35 tahun dengan rentang usia antara 21 sampai 69 tahun.
- Rata-rata limit_balance (batas kredit) nasabah adalah 163,369.31 dengan standar deviasi 125,030.42. Nilai minimum limit_balance adalah 10,000 dan nilai maksimumnya adalah 800,000.
- Rata-rata tagihan bulanan (bill_amt) nasabah pada bulan ke-3 sampai ke-6 adalah lebih tinggi dibandingkan bulan sebelumnya.
- Rata-rata jumlah pembayaran (pay_amt) nasabah pada bulan ke-1 sampai ke-3 lebih rendah dibandingkan bulan berikutnya.
- Proporsi nasabah yang mengalami default payment next month adalah sekitar 21%.
- Mayoritas nasabah berjenis kelamin wanita (rata-rata 1.61).
- Mayoritas nasabah memiliki pendidikan level 2 (rata-rata 1.85).
- Mayoritas nasabah sudah menikah (rata-rata 1.56).
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
