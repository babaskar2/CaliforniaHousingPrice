## **A. Context**
Pada tahun 1990, pemerintah melakukan sensus di California untuk memahami harga rumah di setiap daerah. Lonjakan besar dalam transaksi jual beli rumah menciptakan kebutuhan yang tinggi akan penilaian harga rumah (home appraisal) untuk menentukan nilai jual yang tepat. Data sensus ini membantu pemerintah dalam mengumpulkan informasi yang akurat untuk analisis dan pengambilan keputusan terkait pasar perumahan di berbagai wilayah California.

"In the front yards of many towns along California's coast, 'For Sale' signs have become as common as palm trees, and for some sellers they appear to be permanent fixtures. After years of stunning price increases and demand so strong that homes sold within hours of being listed, California's giant real estate market has slowed drastically" .

Source: <a href="https://www.nytimes.com/1990/08/29/business/california-sees-housing-boom-become-slump.html">New York Times</a> 
## **B. Problem Statemtn**
Terjadi penjualan rumah secara masif di California yang menyebabkan agensi properti perlu memperkerjakan lebih banyak home appraisal, tapi untuk mempekerjakan seorang home appraisal akan menjadi sebuah cost di perusahaan dan akan merugikan jika permintaan untuk memvaluasi sebuah rumah sudah tidak sebanyak sekarang yang akan berujung memecat orang tersebut.

Permasalahan ini menuntut perusahaan untuk mengembangkan sebuah machine learning untuk memprediksi harga median di sebuah distrik California, sehingga perusahaan:

1. **Mengurangi Pengeluaran :** Berdasarkan <a href="https://www.houzeo.com/blog/how-much-is-a-home-appraisal-in-california/#:~:text=What%20Is%20the%20Cost%20of,spend%20nearly%20%24700%2D%241000">Houzeo</a> biaya yang diperlukan dari seorang home appraisal mencapai $1000 USD untuk setiap rumah, hal tersebut membuat perusahaan ingin membuat biaya yang diperlukan untuk menentukan valuasi rumah menjadi lebih murah

2. **Penentuan Harga yang Tepat :** Memastikan harga jual rumah tidak terlalu mahal ataupun terlalu murah untuk menarik pembeli tanpa mengorbankan margin keuntungan

3. **Efisiensi Proses :** Berdasarkan <a href="https://www.rocketmortgage.com/learn/how-long-does-an-appraisal-take">Rokcet Mortage</a> waktu yang diperlukan untuk memvaluasi suatu rumah adalah 6-20 hari kerja, hal ini menjadi hambatan waktu bagi perusahaan untuk mejual sebuah rumah

4. ## **C. Goals**
5. Berdasarkan masalah yang ada, perusahaan menghire seorang data scientist untuk dapat menyelsaikan permasalahan yang ada dengan membuat suatu model yang dapat digunakan untuk melakukan prediksi suatu harga rumah, sehingga dapat menyelsaikan:
1. Biaya yang dikeluarkan dalam menggunakan machine learning dapat jauh lebih murah dibandingkan menggunakan home appraisal
2. Memberikan predisi harga dengan tikat error yang sekecil mungkin
3. Waktu yang diperlukan untuk menghitung valuasi suatu rumah menjadi instant

4. ## **D. Analytic Approach**
5. 1. Data Understanding and Collection:

- Sourcing Data: Mengumpulkan data historis terkait harga rumah di California yang diperlukan.
- Exploratory Data Analysis (EDA): Melakukan analisis eksploratif untuk memahami distribusi, tren, dan pola dalam data. Ini termasuk analisis statistik dasar dan visualisasi data untuk mengidentifikasi outliers, missing values, dan hubungan antar fitur.

2. Data Preprocessing:

- Data Cleaning: Mengatasi missing values, mengoreksi kesalahan data, dan menghapus outliers yang tidak wajar.
- Feature Engineering: Membuat fitur baru yang relevan dan mengonversi fitur kategorikal menjadi format yang dapat digunakan oleh algoritma machine learning, seperti one-hot encoding untuk fitur seperti ocean_proximity.
- Scaling and Normalization: Menormalkan data untuk memastikan semua fitur berada dalam skala yang sama, sehingga model dapat belajar dengan lebih efektif.

3. Model Development:

- Model Selection: Memilih beberapa algoritma machine learning yang sesuai untuk masalah regresi, seperti Linear Regression, Decision Tree, Random Forest, dan Gradient Boosting.
- Model Training: Melatih model menggunakan data yang telah diproses, dengan membagi data menjadi set pelatihan dan set pengujian untuk menghindari overfitting.
- Hyperparameter Tuning: Mengoptimalkan hyperparameters dari model menggunakan teknik seperti Grid Search atau Random Search untuk meningkatkan kinerja model.

4. Model Evaluation:

- Performance Metrics: Menggunakan metrik evaluasi seperti Mean Absolute Error (MAE), Mean Squared Error (MSE), dan Mean Absolute Percentage Error (MAPE) untuk menilai kinerja model.
- Cross-Validation: Melakukan cross-validation untuk memastikan model memiliki generalisasi yang baik dan tidak overfitting terhadap data pelatihan.

5. Model Deployment:

- Deployment Strategy: Mengintegrasikan model ke dalam sistem perusahaan, memungkinkan pengguna untuk memasukkan data rumah dan mendapatkan prediksi harga secara real-time.
- Monitoring and Maintenance: Mengatur sistem monitoring untuk melacak kinerja model setelah deployment dan melakukan pembaruan model secara berkala berdasarkan data baru.

6. Business Integration:

- Cost-Benefit Analysis: Melakukan analisis cost-benefit untuk memastikan bahwa penerapan model machine learning lebih ekonomis dibandingkan metode tradisional.
- Stakeholder Training: Melatih pengguna akhir dan stakeholders tentang cara menggunakan model prediksi dan menginterpretasikan hasilnya.

- ## **Metrics**
- Pada tujuan terkait permasalahan yang ada adalah membuat model yang akurat untuk memprediksi harga suatu rumah dengan begitu terdapat konskuensi yang dapat merugikan semua pihak jika harga yang diprediksi itu salah, baik underprice maupun overprice.

Hal tersebut membuat, perusahaan properti ingin mendapatkan suatu model yang memiliki peresntase tingkat error serendah mungkin untuk meminimalisir kesalahan prediksi yang dilakukan, oleh karena itu metric utama yang digunakan dalam membuat model adalah MAPE (Mean Absolute Percetange Error)

Berdasarkan <a href="https://dqlab.id/kriteria-jenis-teknik-analisis-data-dalam-forecasting">DQLab</a> Metode Mean Absolute Percentage Error (MAPE) memberikan informasi seberapa besar kesalahan peramalan dibandingkan dengan nilai sebenarnya dari series tersebut. Semakin kecil nilai presentasi kesalahan (percentage error) pada MAPE maka semakin akurat hasil peramalan tersebut. Beberapa analisa menyebutkan variasi nilai Mean Absolute Percentage Error memiliki arti yang berbeda.

# **Kesimpulan**
Pemanfaatan machine learning untuk memprediksi median house value di California tahun 1990 memberikan beberapa keuntungan signifikan. Berdasarkan analisis cost-benefit yang telah dilakukan, penggunaan model machine learning menghasilkan pengurangan biaya yang substansial serta peningkatan efisiensi dalam proses penilaian rumah. Implementasi machine learning dapat memberikan keuntungan besar, terutama dalam hal biaya dan kecepatan, sambil tetap mempertimbangkan cara untuk mengatasi keterbatasannya.

Pemodelan yang dilakukan menggunakan algoritma **XGBoostRegressor** berhasil mencapai nilai **Mean Absolute Percentage Error (MAPE) sebesar 16%** dalam memprediksi median house value. Ini berarti model memiliki tingkat kesalahan sebesar 16% dalam prediksinya. Analisis menunjukkan bahwa fitur yang paling berpengaruh dalam memprediksi median harga rumah adalah **'ocean_proximity_NOT INLAND'** dan **'median_income'**.
