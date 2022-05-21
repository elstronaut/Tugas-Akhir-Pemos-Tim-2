# Tugas-Akhir-Pemos-Tim-2
Repositori ini dibuat untuk memenuhi Tugas Akhir Praktikum Pemodelan Oseanografi Oseanografi 2022. Repositori ini memuat IPYNB file yang dapat memproses beberapa persamaan untuk pemodelan oseanografi. Pengerjaan untuk repositori kali ini menggunakan bahasa pemrograman python yang dapat dilakukan pada beberapa platform seperti Google Colaboratory, VS Code, dan Jupyter Notebook. Sedangkan untuk library yang digunakan kali ini adalah Numpy, Matplotlib, Python, Siphon. Seluruh script yang dibuat adalah hasil tim 2 Oseanografi 2020. Semoga dapat bermanfaat!

## 1. Authors Tim 2
1. Aditya Yoga Pratama
2. Refaldi Rizky Maulana 26050120130048 Oseanografi A
3. Rendy Zandika 26050120130057 Oseanografi A
4. Salsabila Auliya Putri 26050120120025 Oseanografi A
5. Aqidatul Izzah 26050120140167 Oseanografi B 
6. Ahmad Nico Fitriadi 26050120140134 Osenografi B 
7. Michael Joshua Xavier 26050120140045 Osenografi B
8. Raza Izzuddien Qossam Ramadhani 26050120170001 Oseanografi B

## 2. Instalasi Modul Pemodelan Oseanografi
Pada pemodelan oseanografi, praktikan dapat menggunakan software, seperti Jupyter Notebook, VS Code, Google Colaboratory, atau yang lainnya untuk mengoperasikan _script_ pemodelan yang telah dibuat. Untuk mengerjakan pemodelan oseanografi, diperlukan beberapa modul tambahan untuk menjalankan _script_ program. Modul-modul tersebut, antara lain matplotlib, siphon, dan numpy. 
- Matplotlib merupakan modul untuk menciptakan visualisasi statis, animasi, dan interaktif dalam program Python.
- Siphon merupakan modul untuk ...
- Numpy merupakan modul untuk menjalankan operasi matematika.

Install Jupyter Notebook:
1. Buka website https://anaconda.org/conda-forge/prompt untuk mengunduh Anaconda Prompt.
2. Tunggu proses dan install ketika selesai mengunduh.
3. Nggatau i bingung apalagi wkkwk boleh tambahin, aku lupa install anacondanya

Untuk menginstall ketiga modul tersebut, langkah-langkah yang perlu dilakukan adalah sebagai berikut:
1. Buka Anaconda Prompt.
2. Ketik "pip install matplotlib" (tanpa tanda petik). Kemudian klik enter.
3. Tunggu proses selesai.
4. Kemudian, ketik "pip install numpy" (tanpa tanda petik). Dan klik enter.
5. Tunggu proses selesai.
6. Terakhir, ketik "pip install siphon"
7. Tunggu proses selesai.

## 3. Materi dan Metode Pengerjaan
- Modul 1: Adveksi 1D
- Modul 2: Adveksi-Difusi 2D
- Modul 3: Hidrodinamika 1D
- Modul 4: Hidrodinamika 2D

### 3.1 Modul 1: Adveksi 1D
- Adveksi merupakan suatu mekanisme perpindahan dari suatu massa dari sebuah materi dari satu titik ketitik lainnya. 
- Adveksi juga dapat diartikan sebagai suatu aliran rata-rata atau arus, seperti sungai atau gerakan pasang-surut yang digerakkan oleh gaya gravitasi atau tekanan dan berupa gerak horizontal. Pada kasus adveksi akan sangat erat kaitannya dengan aliran dari suatu fluida. 
- Persamaan adveksi adalah suatu persmaan diferensial-parsial dimana pada persamaan ini akan memodelkan pergerkan suatu konsentrat dalam suatu fluida yang mengalir. Persmaan adveksi juga sering dikenal dengan persmaan konveksi. Persamaan adveksi muncul dalam pemodelan berbagaifenomena yang melibatkan transportasi zat secara progresif atau gerakan gelombang.

### 3.2 Modul 2: Adveksi-Difusi 2D
- Adveksi merupakan mekanisme perpindahan massa suatu materi dari satu titik ke titik lainnya. Contoh dari adveksi adalah pergerakan kayu dari hulu ke hilir sungai akibat adanya penggerak berupa aliran arus sungai.
- Persamaan adveksi 2D adalah 

![Adveksi](https://user-images.githubusercontent.com/87216822/169637114-90725056-89bd-4720-b213-3ca931ba8025.png)

- Difusi merupakan mekanisme penyebaran konsentrasi akibat adanya kecepatan aliran dan perbedaan konsentrasi. Contoh dari difusi adalah tumpahan tinta yang mulanya menetes pada satu titik lama kelamaan akan menyebar dan konsentrasinya akan berkurang seiring bertambahnya waktu.
- Persamaan difusi 2D adalah

![Difusi](https://user-images.githubusercontent.com/87216822/169637151-0fa7a329-d535-4779-a449-ff7b3b957ae5.png)

Adveksi-difusi menggunakan diskretisasi 2 dimensi yang menggambarkan proses adveksi-difusi pada suatu materi sehingga membentuk persamaan model yang mendekati proses kejadian di alam.
- Diskretisasi adveksi: 

![Adveksi Turunan](https://user-images.githubusercontent.com/87216822/169637158-06624dd5-2f7a-4601-99e8-acc3bb2b8a97.png)

- Diskretisasi difusi: 

![Difusi Turunan](https://user-images.githubusercontent.com/87216822/169637168-21c98ab4-e89a-4da6-8400-9e9a22bc7363.png)

dengan n merupakan indeks waktu dan i, j merupakan indeks ruang.

Pengolahan adveksi-difusi 2 dimensi dapat menggunakan metode eksplisit maupun implisit. 
- Pada metode eksplisit, model adveksi menggunakan persamaan beda hingga menggunakan pendekatan beda maju untuk turunan waktu, sedangkan turunan ruang dilakukan dengan melihat arah kecepatan. Jika u > 0, pendekatan beda mundur. Jika u < 0, pendekatan beda maju.
- Sedangkan, pada model difusi menggunakan pendekatan beda maju untuk turunan waktu dan beda pusat untuk turunan ruang.

#### 3.2.1 _Script_ Pemodelan Adveksi-Difusi 2D
![Script 1](https://user-images.githubusercontent.com/87216822/169637543-f74e8461-26f3-4ac5-b420-a98815caeadb.jpg)
![Script 2](https://user-images.githubusercontent.com/87216822/169637548-a3afd038-8171-4b5d-a753-005a0a324670.jpg)
![Script 3](https://user-images.githubusercontent.com/87216822/169637551-273bc84d-3900-42fe-8b3b-d3589d8d567f.jpg)
![Script 4](https://user-images.githubusercontent.com/87216822/169637561-086eafa7-04e6-430a-89b1-217871c4ec00.jpg)


### 3.3 Modul 3: Hidrodinamika 1D

#### 3.3.1 Pengertian Hidrodinamika 1D
Hidro memiliki arti air dan dinamika memiliki arti benda bergerak atau tenaga yang menggerakan. Dimana model hidrodinamika adalah suatu model yang dibangun dari adanya proses-proses yang mempengaruhi pergerakan massa air. Jadi hidrodinamika dapat didefinisikan sebagai salah satu cabang ilmu pengetahuan yang mempelajari gerak liquid atau gerak fluida cair khususnya gerak air. Dimana kondisi hidrodinamika merupakan salah satu aspek yang sangat berpengaruh terhadap proses - proses yang terjadi di pantai terutama gelombang dan arus bergantung pada bentuk dan karakteristik pantai. Pada praktikum pemodelan oseanografi ini melakukan pembuatan grafik hidrodinamika 1 dimensi yang dilakukan dengan pembuatan model kecepatan arus dan elevasi muka air terhadap waktu dan ruang (grid). Persamaan pembangun hidrodinamika 1 dimensi sederhana adalah persamaan kontinuitas dan persamaan momentum. Hasil yang diperoleh adalah 4 grafik yang mewakili kondisi kecepatan arus dan perubahan elevasi terhadap waktu dan ruang. Grafik-grafik tersebut adalah Grafik Perubahan Kecepatan Arus dalam Grid Tertentu di Sepanjang Waktu, Grafik Perubahan Elevasi Permukaan Air dalam Grid Tertentu di Sepanjang Waktu, Grafik Perubahan Kecepatan Arus dalam Waktu Tertentu di Sepanjang Grid, dan grafik Perubahan Elevasi Permukaan Air dalam Waktu Tertentu di Sepanjang Grid. 

#### 3.3.2 Persamaan-persamaan Model Hidrodinamika 1 Dimensi

#### 3.3.3 Model Hidrodinamika 1 Dimensi

#### 3.3.4 Hasil Model Hidrodinamika 1 Dimensi
![1](https://user-images.githubusercontent.com/87216822/169637972-76081948-e111-4cd0-9e94-38049e76584a.jpg)

**Gambar 1.** Perubahan Kecepatan Arus dalam Grid Tertentu di Sepanjang Waktu

![2](https://user-images.githubusercontent.com/87216822/169637999-c63d83a9-edf9-4020-93bd-0c0ced5397d6.jpg)

**Gambar 2.** Perubahan Elevasi Permukaan Air dalam Grid Tertentu di Sepanjang Waktu

![3](https://user-images.githubusercontent.com/87216822/169638020-7db899b2-a0aa-43fd-8c1a-eb4096082c81.jpg)

**Gambar 3.** Perubahan Kecepatan Arus dalam Waktu Tertentu di Sepanjang Grid

![4](https://user-images.githubusercontent.com/87216822/169638038-71cd1d67-922b-4170-acfd-29c31285491c.jpg)

**Gambar 4.** Perubahan Elevasi Permukaan Air dalam Waktu Tertentu di Sepanjang Grid

### 3.4 Modul 4: Hidrodinamika 2D

## 4. Pengaplikasian Pemodelan dalam Oseanografi
Dalam bidang oseanografi, pemodelan oseanografi sangat penting dilakukan untuk memetakan atau memodelkan suatu perhitungan dari kejadian-kejadian alam yang terjadi di laut. Pemodelan oseanografi dapat digunakan untuk:
1. Menghitung dan memodelkan sebaran polutan yang ada di laut.
2. Memodelkan sebaran nutrien di perairan sungai maupun laut.
3. Mengetahui kebocoran minyak.
4. dst
5. dst

## 5. Penutup
