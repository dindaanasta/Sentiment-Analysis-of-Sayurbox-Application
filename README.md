# Sentiment Analysis of Sayurbox Application

## PERKENALAN

> Hello 👋. Pada projek kali ini, saya akan melakukan analisis sentimen terhadap ulasan pengguna aplikasi Sayurbox. Sayurbox merupakan aplikasi e-grocery yang memberikan kemudahan bagi petani lokal untuk menjual hasil panennya dalam keadaan segar kepada konsumen. 

> Tujuan dilakukannya analisis sentimen adalah untuk mengetahui ulasan pengguna aplikasi Sayurbox, cenderung positif atau negatif. 

> Pengambilan data ini dilakukan melalui website google play menggunakan teknik web crawling dimulai dari bulan Maret 2020 sampai dengan Maret 2022 dengan jumlah data sebesar 1905 ulasan. 

> Analisis ini menggunakan kamus slangword yang berisi kata baku dan tidak baku berasal dari github taudataid dan dapat diakses melalui link https://github.com/taudataid/eLearning untuk merubah kata ulasan yang mengandung kata tidak baku, salah eja, dan kata singkat menjadi kata baku sesuai dengan Kamus Besar Bahasa Indonesia.

> Metode yang digunakan untuk klasifikasi sentimen adalah lexicon-based menggunakan kamus Inset Lexicon yang dapat diunduh melalui github https://github.com/fajri91/InSet sedangkan algoritma yang digunakan adalah Support Vector Machine.


## RINGKASAN

- Pengumpulan Data 
Pengumpulan data ulasan aplikasi Sayurbox dilakukan melalui website play.google.com menggunakan bantuan library google-play-scraper dan bahasa pemrograman Python dimulai dari bulan Maret 2020 sampai dengan Maret 2022. Jumlah data ulasan aplikasi Sayurbox yang berhasil dikumpulkan sebesar 1905 ulasan. 

![image](https://user-images.githubusercontent.com/71063726/192546850-86e5bef3-8400-4ac4-87df-50e7354f0a5c.png)

- Eksplorasi Data

![image](https://user-images.githubusercontent.com/71063726/192547985-ec9b4cb7-e06b-44dd-9e64-ef8f77aca520.png)

Dari gambar di atas, persebaran rating tertinggi berada di rating 5 atau very satisfied sebanyak 1326. 

![image](https://user-images.githubusercontent.com/71063726/192548402-cb888a20-5d6d-4033-a922-f14348109ee9.png)

Jika dilihat berdasarkan tahun, rating 5 atau very satisfied di tahun 2021 mendapatkan jumlah paling besar sebanyak 683 tetapi ditahun 2022 mengalami penurunan menjadi 245. 

- Persiapan Data
Persiapan data terdiri dari beberapa tahap, yaitu case folding, cleaning (emoji, hashtag, tanda baca, angka, pengulangan huruf dan kata, whitespaces, serta kata abstrak), Normalization (merubah kata tidak baku menjadi baku), tokenizing, stopword, dan stemming.  

![image](https://user-images.githubusercontent.com/71063726/192547829-386c2dbb-ccdc-4371-bf22-ae8d91688bd2.png)

- Klasifikasi Sentimen Menggunakan Metode Lexicon Based
Data ulasan yang telah bersih, ditentukan polaritas sentimen dengan cara mengklasifikasikannya menjadi positif dan negatif menggunakan kamus Indonesia Sentiment Lexicon yang dapat diakses melalui github https://github.com/fajri91/InSet. Setiap kata ulasan akan dihitung nilai polaritasnya dengan memberikan nilai +5 untuk kata paling positif dan -5 untuk kata paling negatif. Setelah itu, keseluruhan nilai polaritas tiap kata akan dihitung agar dapat diketahui ulasan yang mengandung sentimen positif dan negatif. Visualisasi dari klasifikasi sentimen, dapat dilihat pada gambar dibawah ini:

![image](https://user-images.githubusercontent.com/71063726/192549808-12b2031d-f1c0-4ca6-b309-66a73aa57b6c.png)

Worcloud Kata Positif
![image](https://user-images.githubusercontent.com/71063726/192549931-af1e08a5-ab96-4d25-b4e1-c1eee07b2424.png)

WordCloud Kata Negatif
![image](https://user-images.githubusercontent.com/71063726/192549991-2d7d2ce3-de6d-4279-acf3-2f7fc289e59d.png)

## PEMODELAN


![image](https://user-images.githubusercontent.com/71063726/192552262-cd013550-7b92-4a33-880a-e5c60103a81d.png)


![image](https://user-images.githubusercontent.com/71063726/192552067-081bf50b-8575-492e-8e57-c801eae660f6.png)

![image](https://user-images.githubusercontent.com/71063726/192552139-ebe1debe-e8fe-4e5e-8149-bf913d5e09e7.png)


