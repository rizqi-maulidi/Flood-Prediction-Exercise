# Flood Prediction Exercise

## Deskripsi
Project latihan ini saya kerjakan ketika menjadi peserta di Coding Camp powered by DBS Foundation, fokus utama dari latihan ini adalah memahami cara kerja model Regresi Linier cocok untuk pola data yang seperti apa. Sebagai latihan dataset ini juga cukup bersih sehingga tidak terlalu banyak memerlukan proses data cleaning. Data yang saya gunakan berasal dari kaggle dengan link: https://www.kaggle.com/competitions/playground-series-s4e5/data

## Setup Environment - Python (venv)
mkdir Flood Prediction Exercise
cd Flood Prediction Exercise
python -m venv venv_floodpredict
.\floodpredict\Scripts\Activate
pip install -r requirements.txt

## Kesimpulan Analisis
Berdasarkan hasil evaluasi model dengan metrik MAE (Mean Absolute Error), MSE (Mean Squared Error), dan R² (Koefisien Determinasi), berikut adalah kesimpulan performa model:

**Lars (Least Angle Regression)**

Memiliki MAE tertinggi (0.806497) dan MSE tertinggi (0.998246), yang menunjukkan bahwa model ini memiliki kesalahan rata-rata yang besar dalam prediksi.
R² sangat kecil (0.000764), yang berarti model hampir tidak dapat menjelaskan variabilitas data.
Secara keseluruhan, Lars adalah model dengan performa paling buruk, hampir setara dengan tebakan rata-rata tanpa model.

**Linear Regression**

Memiliki MAE terkecil (0.329142) dan MSE terkecil (0.171296), yang menunjukkan bahwa model ini lebih akurat dibandingkan dengan dua model lainnya.
R² sebesar 0.828534, menunjukkan bahwa 82.85% variabilitas dalam data dapat dijelaskan oleh model ini, yang merupakan nilai yang cukup baik.
Berdasarkan metrik ini, Linear Regression adalah model terbaik untuk dataset ini.

**Gradient Boosting Regressor**

Memiliki MAE sebesar 0.512672 dan MSE sebesar 0.380491, lebih tinggi dibandingkan Linear Regression tetapi lebih rendah dibandingkan Lars.
R² sebesar 0.619132, menunjukkan bahwa model ini menjelaskan sekitar 61.91% variabilitas dalam data, yang lebih rendah dibandingkan Linear Regression tetapi jauh lebih baik dibandingkan Lars.
Model ini cukup baik, tetapi masih kalah dari Linear Regression dalam hal akurasi.

**Kesimpulan Akhir:**
Linear Regression adalah model terbaik untuk dataset ini karena memiliki MAE dan MSE terendah serta R² tertinggi (82.85%).
Hal ini mungkin karena banyak fitur dalam dataset sudah terdistribusi normal, Linear Regression memang sering menjadi pilihan yang baik karena model ini bekerja optimal dengan asumsi distribusi normal pada variabel independen dan residual.
