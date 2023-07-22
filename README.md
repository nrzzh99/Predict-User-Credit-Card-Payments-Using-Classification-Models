# Predict-User-Credit-Card-Payments-Using-Classification-Models
Objective :
This project aims to predict customers based on previous payments to classify whether customers will fail to pay in the next month's payments or not

## Latar belakang masalah :
Dalam menghadapi risiko pembayaran terlambat, perusahaan membutuhkan informasi yang akurat untuk mengelola risiko dengan lebih baik. perusahaan dapat mengidentifikasi pelanggan yang berpotensi gagal membayar lebih awal. Hal ini akan membantu mengurangi kerugian dan meningkatkan efisiensi dalam pengelolaan risiko.

## Data yang Digunakan:
Data dalam proyek ini berasal dari BigQuery dengan nama database "credit_card_default". Terdapat 2965 baris dan 24 kolom. Data mencakup informasi tentang pengguna, seperti jenis kelamin, tingkat pendidikan, status pernikahan, dan usia. Terdapat juga kolom "default_payment_next_month" yang menjadi target prediksi, yaitu apakah pelanggan akan mengalami keterlambatan pembayaran pada bulan berikutnya. Selain itu, ada kolom "limit_balance" yang menunjukkan batas kredit pengguna.

## Metode yang Digunakan:
Dalam proyek ini, beberapa model klasifikasi seperti Logistic Regression, SVM, Decision Tree, K-Neighbors (KNN), Naive Bayes, Random Forest, dan Gradient Boosting digunakan untuk memprediksi keterlambatan pembayaran pelanggan. Model-model ini dievaluasi menggunakan metrik seperti confusion matrix dan ROC AUC score. Cross Validation juga digunakan untuk menentukan model terbaik untuk dataset ini.

## Kelebihan dan Kekurangan Proyek:
Kelebihan dari proyek ini adalah model dapat mengklasifikasikan dengan baik dan memberikan wawasan yang berarti dalam mengidentifikasi pelanggan yang berpotensi gagal membayar. Namun, proyek ini mungkin dapat ditingkatkan dengan mencoba mengukur menggunakan metrik lain seperti Mean Squared Error (MSE) untuk penilaian performa model.
