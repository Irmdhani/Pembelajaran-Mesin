## Bitcoin Price Trends Detection dengan Machine Learning

## Mohamad Ilham Ramadhani - A11.2022.14587


Ringkasan dan Tujuan Proyek

Project ini dibuat karena banyak orang yang ingin berinvestasi tanpa memikirkan pola - pola yang harus dipelajari, sehingga project ini di buat untuk mengatasi permasalahan orang yang ingin berinvestasi namun tidak memiliki banyak waktu untuk belajar trading. Cukup dengan modal yang dimiliki dan Machine Learning ini maka modal yang dimiliki akan berputar secara otomatis setiap 4 jam berdasarkan logika mesin dan history pasar.

Model / Alur Penyelesaian 

               +-----------------------+
               |     Data Collect      |
               |  Dataset from Kaggle  |
               +-----------+-----------+
                           |
                           v
               +-----------------------+
               |      Data Process     |
               |      Reformatting     |
               +-----------+-----------+
                           |
                           v
           +---------------+----------------+
           |                                  |
           v                                  v
    +-----------------+               +-------------------+
    |   Model 1:      |               |     Model 2:      |
    |  Neural Network |               |K-Nearest Neighbour|
    +--------+--------+               +---------+---------+
             |                                  |
             v                                  v
    +--------+---------+               +--------+--------+
    |  Classification  |               |    Model 3:     |
    |      Model       |               |    XGBoost      |
    +--------+--------+               +--------+--------+
             |                                  |
             v                                  v
          +-------------------------------------------+
          |          Select Best Model                |
          +-------------------------------------------+
                             |
                             v
                 +-----------------------+
                 |     Data Sampling     |
                 +-----------------------+
                             |
                             v
                 +-----------------------+
                 |      Load Machine      |
                 |Automated Order Every 4H|
                 +-----------------------+

Datasets

Dataset yang digunakan berasal dari Kaggle dan Dataset yang saya gunakan adalah trend pergerakan harga bitcoin setiap hari hingga tahun 2022, variabel yang tersedia seperti tanggal, harga rata - rata orang membuka, harga tertinggi, harga terendah, harga rata - rata close, volume BTC, dan volume USD, dengan adanya dataset ini, model NN, KNN, dan XGBoost dalam machine learning dapat melakukan analisa trend harga yang akan muncul kedepannya.

https://www.kaggle.com/datasets/prasoonkottarathil/btcinusd/data

Model

NN(Neural Network) : model komputasi yang meniru cara kerja otak manusia, terdiri dari neuron-neuron yang terhubung dalam lapisan-lapisan: input, hidden, dan output. Setiap neuron menerima input, mengalikan dengan bobot, menambahkan bias, dan menerapkan fungsi aktivasi untuk menghasilkan output.

KNN(K-Nearest Neighbour) : algoritma supervised learning yang mengklasifikasikan atau mengelompokkan data ke dalam beberapa kelompok berdasarkan kemiripan sifat dari data. Algoritma ini hampir mirip dengan algoritma K-Means, yang membedakan adalah pada K-Means melakukan proses clustering sedangkan pada KNN melakukan proses klasifikasi.

XGBoost : berbasis pada teknik boosting, di mana pohon keputusan dibangun secara bertahap, dan setiap pohon baru berusaha untuk memperbaiki kesalahan dari pohon sebelumnya. Model ini terkenal karena efisiensinya dalam hal kecepatan dan performa, terutama pada data besar dan kompetisi machine learning.

setelah dataset berhasil di ambil, dataset akan di proses ulang dan diformat sesuai dengan variabel yang dibutuhkan model. Dengan NN setelah data diolah data akan di klasifikasikan, sedangkan di KNN data akan di bandingkan dengan model XGBoost untuk mencari model paling efisien, setelah berhasil menemukan Model yang paling efisien, lalu dilakukan data sampling untuk uji coba. Setelah berhasil, maka langkah terakhir adalah machine akan melakukan trading secara otomatis setiap 4 jam, dan mengirimkan report trading ke email yang di masukkan di mesin. 

Kesimpulan

Berdasarkan Model - Model yang digunakan, tingkat akurasi yang dicapai dalam memprediksi harga bitcoin kedepan setiap harinya adalah sekitar 95% yang mengartikan bahwa Machine tersebut sangat akurat dalam memprediksi harga Bitcoin kedepannya berdasarkan data - data yang sudah ada dari tahun 2014. Ini mengartikan bahwa Machine ini dapat menyelesaikan masalah yang ada di dunia sekitar jika orang - orang ingin mengelola modal untuk trading secara otomatis, namun tingkat ke akuratan yang di hasilkan bukan menjadi patokan bahwa prediksi machine akan selalu benar, karena terkadang harga Bitcoin juga bisa berubah sangat tinggi hingga sangat rendah. Untuk itu siapkan persiapan dan modal dingin dengan matang untuk siap menghindari segala resiko yang ada.
