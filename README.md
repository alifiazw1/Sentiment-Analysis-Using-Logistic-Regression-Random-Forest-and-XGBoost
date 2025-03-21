# Sentiment-Analysis-Using-Logistic-Regression-Random-Forest-and-XGBoost

## Overview

Proyek ini berfokus pada analisis sentimen dalam postingan media sosial menggunakan teknik Machine Learning. Dataset yang digunakan berasal dari Kaggle dengan judul "Social Media Sentiment Analysis". Tujuan dari proyek ini adalah untuk membandingkan kinerja model yang dibangun, dalam memprediksi sentimen menjadi tiga kategori yaitu positif, negatif, dan netral. 

## Dataset
Dataset terdiri dari 732 Baris dan 13 kolom dengan keterangan setiap variabel adalah sebagai berikut:
1. Teks Postingan: Konten yang dibuat oleh pengguna yang menunjukkan sentimen.
2. Label Sentimen: Kategori emosi yang diklasifikasikan.
3. Timestamp: Informasi tanggal dan waktu.
4. User: Identitas unik dari pengguna yang berkontribusi.
5. Platform: Platform media sosial tempat konten berasal.
6. Hashtags: Tagar yang mengidentifikasi topik dan tema yang sedang tren.
7. Likes: Jumlah suka yang mencerminkan keterlibatan pengguna.
8. Retweets: Jumlah retweet yang mencerminkan popularitas konten.
9. Country: Asal geografis dari setiap postingan.
10. Year: Tahun dari postingan.
11. Month : Bulan dari postingan
12. Day : Hari dari postingan

## Pre Processing
Untuk mempersiapkan data sebelum masuk ke pemodelan, dilakukan beberapa langkah terutama pada kolom "Text" yang menjadi bahan utama dalam pembangunan model. 
1. Pembersihan Teks: Menghapus karakter khusus, angka, dan spasi berlebih.
2. Konversi ke Huruf Kecil: Mengubah semua teks menjadi huruf kecil agar seragam.
3. Penghapusan Stopword: Menghapus kata-kata umum yang tidak terlalu berkontribusi pada makna.
4. Tokenisasi: Memisahkan teks menjadi kata-kata individu.
5. Lematisasi: Mengubah kata-kata ke bentuk dasar.
6. Vektorisasi: Mengubah teks menjadi representasi numerik menggunakan TF-IDF.

## Pemodelan
Model yang digunakan dalam proyek ini adalah Logistic Regression, Random Forest, dan XGBoost. Ketiga model tersebut akan dibandingkan kinerjanya dalam hal akurasi. 

## Hasil
Hasil pemodelan dan evaluasi kinerja model dengan menggunakan accuracy score adalah sebagai berikut:
1. Logistic Regression
                   precision    recall  f1-score   support

           0       0.50      0.24      0.32        17
           1       0.69      0.86      0.77        90
           2       0.64      0.45      0.53        40
2. Random Forest
                 precision    recall  f1-score   support

           0       0.33      0.12      0.17        17
           1       0.65      0.88      0.75        90
           2       0.63      0.30      0.41        40
3. XGBoost
                 precision    recall  f1-score   support

           0       0.62      0.47      0.53        17
           1       0.73      0.79      0.76        90
           2       0.59      0.55      0.57        40

Dari ketiga model, algoritma XGBoost menghasilkan nilai presisi, recall, dan f1-score paling baik daripada algoritma Logistic Regression dan Random Forest. Namun, terlihat bahwa model XGBoost juga masih kesulitan dalam memprediksi sentimen negatif (0) dan positif (2), ditunjukkan dengan nilai f1-score yang masih berada dibawah angka 70%. 

## Saran
1. Menggunakan model deep learning seperti LSTM
2. Mengoptimalkan Pre Processing data untuk menghasilkan data yang lebih bersih dan lebih baik.

# Dashboard
Dashboard analisis digunakan untuk memahami hasil analisis dan karakteristik data dengan menggunakan visualisasi yang menarik dan mudah untuk dimengerti. Pada proyek ini, dashboard analisis dibuat dengan menggunakan Looker Studio, yang menampilkan hasil analisis sentimen dari postingan, dan informasi-informasi pendukung lainnya.
