Nama = Nur Aisyah
Nim = 241011402656
kelas = 05TPLM001


# Ringkasan Hasil UTS Machine Learning

## 1. Linear Regression
Model digunakan untuk memprediksi penjualan berdasarkan biaya iklan.
Persamaan regresi yang diperoleh:
**Ŷ = 28,5405 + 8,9851X**

Hasil evaluasi:
| Metrik | Training | Testing |
| ------ | -------: | ------: |
| MAE    |   5,1345 |  2,2890 |
| MSE    |  43,2469 |  8,2377 |
| RMSE   |   6,5762 |  2,8701 |
| R²     |   0,9276 |  0,9873 |
**Analisis:** Nilai R² testing sebesar 0,9873 menunjukkan bahwa model dapat menjelaskan sekitar 98,73% variasi penjualan pada data pengujian. Nilai RMSE testing sebesar 2,8701 menunjukkan rata-rata kesalahan prediksi dalam ukuran RMSE sekitar 2,87 juta rupiah.

## 2. Logistic Regression
Model digunakan untuk mengklasifikasikan email sebagai spam atau bukan spam berdasarkan jumlah link dan kata promosi.
Hasil evaluasi pada data testing:
| Metrik              |   Hasil |
| ------------------- | ------: |
| Accuracy            |  93,33% |
| Precision           |  80,00% |
| Recall              | 100,00% |
| F1-Score            |  88,89% |
| True Negative (TN)  |      10 |
| False Positive (FP) |       1 |
| False Negative (FN) |       0 |
| True Positive (TP)  |       4 |
**Analisis:** Model memperoleh akurasi 93,33%, dengan 14 dari 15 email berhasil diklasifikasikan dengan benar. Recall sebesar 100% menunjukkan seluruh email spam pada data testing berhasil terdeteksi, tetapi terdapat satu email bukan spam yang salah diklasifikasikan sebagai spam.

## 3. Perbandingan dengan Scikit-learn
Hasil perbandingan pada data testing:
- **Linear Regression:** MAE = 2,2890, RMSE = 2,8701, dan R² = 0,9873.
- **Logistic Regression:** Accuracy = 93,33%, dengan confusion matrix yang sama, yaitu [[10, 1], [0, 4]].
**Analisis:** Hasil Linear Regression NumPy dan Scikit-learn hampir sama karena keduanya menghasilkan persamaan regresi yang setara. Hasil Logistic Regression juga sama pada evaluasi ini. Namun, hasil Logistic Regression dapat berbeda pada konfigurasi lain karena metode optimasi, regularisasi, dan parameter pelatihan yang digunakan.

## 4. Kesimpulan
Berdasarkan hasil pengujian, Linear Regression mampu memprediksi penjualan dengan nilai R² testing sebesar 0,9873. Sementara itu, Logistic Regression mampu mengklasifikasikan email dengan akurasi 93,33%. Kedua model menunjukkan hasil yang baik pada data pengujian yang digunakan, tetapi evaluasi pada data yang lebih banyak tetap diperlukan untuk mengetahui kemampuan model pada data baru.
