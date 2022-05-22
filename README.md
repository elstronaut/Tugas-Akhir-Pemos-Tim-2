# Tugas Akhir Praktikum Pemodelan Oseanografi Tim 2
Repositori ini dibuat untuk memenuhi Tugas Akhir Praktikum Pemodelan Oseanografi Oseanografi 2022. Repositori ini memuat IPYNB file yang dapat memproses beberapa persamaan untuk pemodelan oseanografi. Pengerjaan untuk repositori kali ini menggunakan bahasa pemrograman python yang dapat dilakukan pada beberapa platform seperti Google Colaboratory, VS Code, dan Jupyter Notebook. Sedangkan, untuk modul yang digunakan kali ini adalah Numpy, Matplotlib, Python, Siphon. Seluruh script yang dibuat adalah hasil tim 2 Oseanografi 2020. Semoga dapat bermanfaat!

## 1. Authors Tim 2
1. Aditya Yoga Pratama 26050120130120 Oseanografi A
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
![install matplotlib](https://user-images.githubusercontent.com/105728766/169687513-3941866d-43c5-4cda-bcdd-593776586e80.png)
4. Tunggu proses selesai.
5. Kemudian, ketik "pip install numpy" (tanpa tanda petik). Dan klik enter.
![install numpy](https://user-images.githubusercontent.com/105728766/169687540-cbe89095-61fa-4964-a985-1b4e5d616e9f.png)

7. Tunggu proses selesai.
8. Terakhir, ketik "pip install siphon"
![install siphon](https://user-images.githubusercontent.com/105728766/169687546-7da6e556-d19e-4f56-b78b-0661ad60c687.png)

10. Tunggu proses selesai.

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
![Script 1](https://user-images.githubusercontent.com/96801637/169647598-37715e60-ec90-48ed-a58b-97c1d7b7f7ef.png)
![Script 2](https://user-images.githubusercontent.com/96801637/169647619-93079565-33b7-4546-ba07-ce69d0021182.png)
![Script 3](https://user-images.githubusercontent.com/96801637/169647900-f651449c-8d5d-474f-a031-b9218aa78cdc.png)

dalam pemodelan Adveksi-Difusi 2D ini menggunakan 4 skenario yang sama namun perbedaannya terletak pada nilai tetha yang berbeda. nilai tetha sangat berpengaruh terhadap pergerakan poluthan yang dipengaruhi oleh nilai U dan V dari hasil yang berbeda.

Berikut ini hasil dari timestep dari polutan pada nilai t yang berbeda
- untuk nilai t= 0.5
![download (1)](https://user-images.githubusercontent.com/96801637/169649389-08ee6d30-cc6e-4e9f-9417-860249ec7b3f.png)

- untuk nilai t= 16.0
![download (4)](https://user-images.githubusercontent.com/96801637/169649455-e8148f1b-a522-4228-a5bf-42fbd62c4de7.png)

#### 3.2.2 Pengaplikasian Adveksi-Difusi 2D dalam Oseanografi
Dalam bidang oseanografi, pemodelan oseanografi adveksi-difusi 2 dimensi sangat penting dilakukan untuk memetakan atau memodelkan suatu perhitungan dari kejadian-kejadian alam yang terjadi di laut. Pemodelan adveksi-difusi 2 dimensi dapat digunakan untuk:
1. Menghitung dan memodelkan sebaran polutan yang ada di laut.
2. Memodelkan sebaran nutrien di perairan sungai maupun laut.
3. Mengetahui kebocoran minyak.

### 3.3 Modul 3: Hidrodinamika 1D

#### 3.3.1 Pengertian Hidrodinamika 1D
Hidro memiliki arti air dan dinamika memiliki arti benda bergerak atau tenaga yang menggerakan. Dimana model hidrodinamika adalah suatu model yang dibangun dari adanya proses-proses yang mempengaruhi pergerakan massa air. Jadi hidrodinamika dapat didefinisikan sebagai salah satu cabang ilmu pengetahuan yang mempelajari gerak liquid atau gerak fluida cair khususnya gerak air. Dimana kondisi hidrodinamika merupakan salah satu aspek yang sangat berpengaruh terhadap proses - proses yang terjadi di pantai terutama gelombang dan arus bergantung pada bentuk dan karakteristik pantai. 

#### 3.3.2 Model Hidrodinamika 1 Dimensi 
Pada praktikum pemodelan oseanografi ini melakukan pembuatan grafik hidrodinamika 1 dimensi yang dilakukan dengan pembuatan model kecepatan arus dan elevasi muka air terhadap waktu dan ruang (grid). Persamaan pembangun hidrodinamika 1 dimensi sederhana adalah persamaan kontinuitas dan persamaan momentum. Hasil yang diperoleh adalah 4 grafik yang mewakili kondisi kecepatan arus dan perubahan elevasi terhadap waktu dan ruang. Grafik-grafik tersebut adalah Grafik Perubahan Kecepatan Arus dalam Grid Tertentu di Sepanjang Waktu, Grafik Perubahan Elevasi Permukaan Air dalam Grid Tertentu di Sepanjang Waktu, Grafik Perubahan Kecepatan Arus dalam Waktu Tertentu di Sepanjang Grid, dan grafik Perubahan Elevasi Permukaan Air dalam Waktu Tertentu di Sepanjang Grid

#### 3.3.3 Persamaan-persamaan Model Hidrodinamika 1 Dimensi
Pada model hidrodinamika 1 dimensi digunakan dua persmaan pengatur fluida yaitu persamaan momentum dan persmaan kontinuitas.
- Persmaan Kontinuitas: 
Pada persmaan kontinuitas menggambarkan dari konservasi zat pada fluida dalam memberikan ruang yang tidak dapat diciptakan maupun dihancurkan. Pada kasus fluida atau sejenisnya yang tidak dapat ditempa, prinsip kontinuitas digambarkan dengan konservasi dari volume. Kecuali pada kasus yang spesial dimana parsial nampak kosong. Prinsip kontinuitas memberikan hubungan antara V, densitas _p_ (rho) dan koordinat ruang dan waktu.
![image](https://user-images.githubusercontent.com/105764448/169650427-8b6b076c-4454-40e2-8cfe-35f1a8e58e1a.png)
- Persmaan Momentum:
Pada persamaan momentum prinsip yang digunakan adalah mengungkapkan hubungan antara gaya yang bekerja pada F pada sebuah unit volume dari densitas _p_ dan kemudian gaya Inersia d(pV)dt dari unit volume ini bagian dari gerak. Gaya Inersia berhubungan dengan  penerimaan  alami  dari  tubuh  untuk  menerima  kembali  perubahan dalam  gerak. Fluida mekanik dalam persamaan ini mengambil bentuk partikular yang mana di ambil dari hitungan faktanya bahwa partikel fluida mungkin telah tersusun. Untuk sebuah fluida incompersible (atau fluida yang tidak dapat di tempa) penggabungan persamaan momentum dengan memberikan jarak kerja persamaan dan energi, mengungkapkan sebuah bentuk dari perlindungan dari prinsip energi.
![image](https://user-images.githubusercontent.com/105764448/169650943-dca11812-bb70-4bf6-9cce-506a9d3d9fe1.png)

#### 3.3.4 Penggunaan Script Model Hidrodinamika 1 Dimensi
1. Memasukkan  library python matploblib untuk memberikan efek visual pada grafik, numpy untuk perhitungan numerik dan sys untuk mengakses konfigurasi interpreter pada saat runtime.
```
    import matplotlib.pyplot as plt
    import numpy as np
    
```
2. Selanjutnya, memasukkan parameter perhitungan yang akan digunakan.
```
    p = 7500 #Panjang Grid
    T = 2000 #Waktu Simulasi
    A = 0.1 #Amplitudo
    D = 5 #Depth/Kedalaman
    dt = 2 
    dx = 100
    To = 500 #Periode

    g = 9.8
    pi = np.pi
    C = np.sqrt(g*D) #Kecepatan Arus
    s = 2*pi/To #Kecepatan Sudut Gelombang
    L = C*To #Panjang Gelombang
    k = 2*pi/L #Koefisien Panjang Gelombang
    Mmax = int(p//dx)
    Nmax = int(T//dt)

    zo = [None for _ in range(Mmax)]
    uo = [None for _ in range(Mmax)]

    hasilu = [None for _ in range(Nmax)]
    hasilz = [None for _ in range(Nmax)]
    
```
3. Setelah itu, script perhitungan dibuat.
```
    for i in range(1, Mmax+1):
        zo[i-1] = A*np.cos(k*(i)*dx)
        uo[i-1] = A*C*np.cos(k*((i)*dx+(0.5)*dx))/(D+zo[i-1])

    for i in range(1, Nmax+1):
        zb = [None for _ in range(Mmax)]
        ub = [None for _ in range(Mmax)]
        zb[0] = A*np.cos(s*(i)*dt)
        ub[-1] = A*C*np.cos(k*L-s*(i)*dt)/(D+zo[-1])
        for j in range(1, Mmax):
            ub[j-1] = uo[j-1]-g*(dt/dx)*(zo[j]-zo[j-1])
        for k in range(2, Mmax+1):
            zb[k-1] = zo[k-1]-(D+zo[k-1])*(dt/dx)*(ub[k-1]-ub[k-2])
            hasilu[i-1] = ub
            hasilz[i-1] = zb
        for p in range(0, Mmax):
            uo[p] = ub[p]
            zo[p] = zb[p]

```
4. Setelah itu, script grafik dibuat.
```
    def rand_col_hex_string():
        return f'#{format(np.random.randint(0,16777215), "#08x")[2:]}'

    hasilu_np = np.array(hasilu)
    hasilz_np = np.array(hasilz)

    fig0, ax0 = plt.subplots(figsize=(12,8))
    for i in range(1, 16):
        col0 = rand_col_hex_string()
        line, = ax0.plot(hasilu_np[:,i-1], c=col0, label=f'n={i}')
        ax0.legend()

        ax0.set(xlabel='Waktu', ylabel='Kecepatan Arus',
               title='''KELOMPOK 2_OSEANOGRAFI 2020_PRAKTIKUM PEMODELAN OSEANOGRAFI 2022
               Perubahan Kecepatan Arus Dalam Grid Tertentu di Sepanjang Waktu''')
        ax0.grid()

    fig1, ax1 = plt.subplots(figsize=(12,8))
    for i in range(1, 16):
        col1 = rand_col_hex_string()
        line, = ax1.plot(hasilz_np[:,i-1], c=col1, label=f'n={i}')
        ax1.legend()

        ax1.set(xlabel='Waktu', ylabel='Elevasi Muka Air',
               title='''KELOMPOK 2_OSEANOGRAFI 2020_PRAKTIKUM PEMODELAN OSEANOGRAFI 2022
               Perubahan Elevasi Permukaan Air Dalam Grid Tertentu di Sepanjang Waktu''')
        ax1.grid()

    fig2, ax2 = plt.subplots(figsize=(12,8))
    for i in range(1, 16):
        col2 = rand_col_hex_string()
        line, = ax2.plot(hasilu_np[i-1], c=col2, label=f't={i}')
        ax2.legend()

        ax2.set(xlabel='Grid', ylabel='Kecepatan Arus',
               title='''KELOMPOK 2_OSEANOGRAFI 2020_PRAKTIKUM PEMODELAN OSEANOGRAFI 2022
               Perubahan Kecepatan Arus Dalam Waktu Tertentu di Sepanjang Grid''')
        ax2.grid()

    fig3, ax3 = plt.subplots(figsize=(12,8))
    for i in range(1, 16):
        col3 = rand_col_hex_string()
        line, = ax3.plot(hasilz_np[i-1], c=col3, label=f't={i}')
        ax3.legend()

        ax3.set(xlabel='Grid', ylabel='Elevasi Muka Air',
               title='''KELOMPOK 2_OSEANOGRAFI 2020_PRAKTIKUM PEMODELAN OSEANOGRAFI 2022
               Perubahan Elevasi Permukaan Air Dalam Waktu Tertentu di Sepanjang Grid''')
        ax3.grid()

    plt.show()
```

#### 3.3.5 Hasil Model Hidrodinamika 1 Dimensi
![Perubahan Elevasi Permukaan air dalam grid tertentu di sepanjang waktu](https://user-images.githubusercontent.com/103481626/169638705-96cdff1b-c191-4a21-a845-f25b4df9a141.png)
![Perubahan Elevasi Permukaan air dalam waktu tertentu di sepanjang grid](https://user-images.githubusercontent.com/103481626/169638710-2debfd04-e0d1-48db-9495-f3e60039024d.png)
![Perubahan Kecepatan Arus dalam grid tertentu di sepanjang waktu](https://user-images.githubusercontent.com/103481626/169638714-567c51ca-aba8-4a3f-a016-d389fbd083b5.png)
![Perubahan kecepatan arus dalam waktu tertentu di sepanjang grid](https://user-images.githubusercontent.com/103481626/169638717-3d1361e3-a592-4c5e-be44-df1445e080c3.png)

#### 3.3.6 Pengaplikasian Model Hidrodinamika 1D dalam Oseanografi
1. Pemodelan hidrodinamika untuk penentuan tipe pengaman pantai.  
2. Memodelkan hidrodinamika beserta transpor sedimen untuk membuktikan adanya sedimentasi dan kekeruhan.
3. Memprediksi laju sedimentasi dengan pemodelan numerik hidrodinamika.
4. Pemodelan Hidrodinamika untuk analisis arus dan transpor sedimen.
5. Analisis pemodelan hidrodinamika untuk mendesign breakwater.


### 3.4 Modul 4: Hidrodinamika 2D
Materi hidrodinamika 2D adalah untuk mininjau nilai informasi gelombang laut, angin, dan tekanan pada lokasi perairan yang diambil dari data gelombang National Buoy Data Center (NDBC) Milik NOAA.  Yang dimana data atau informasi yang kita ambil tersebut akan kita plotkan untuk memodelkan kolerasi antara beberapa parameter terkait.

### 3.4.1 Penerapan Hidrodinamika 2D di Oseanografi
1. Pemodelan gelombang karena angin
2. Pemodelan Arus 
3. Pemodelan Polutan /sampah di laut
4. pemodelan coastal dynamic dan sedimentasi pantai

#### 3.4.2 Penggunaan Script Model Data Gelombang National Buoy Data Center (NDBC) 
```
#Copyright (c) 2018 Siphon Contributors
#Distributed under the terms of the BSD 3-Clause License
#SPDX-License_Identifier:BSD-3-Clause
"""
NDBC Buoy Meteorological Data Request
=====================================
The NDBC keeps a 45-day recent rolling file for each buoy. This examples shows :
the basic meteorological data from a buoy and make a simple plot
"""

import matplotlib.pyplot as plt

from siphon.simplewebservice.ndbc import NDBC

#####################################################
#Get a pandas data frame of all of the observations, meteorological data is the default
#observation set to query.
df = NDBC.realtime_observations('NWPR1') #Station ID
df.head()

#####################################################
#Let's make a simple time plot to checkout what the data Look Like,
fig, (ax1, ax2, ax3) = plt.subplots(3, 1, figsize=(12, 10))
ax2b = ax2.twinx()

# Pressure 
ax1.plot(df['time'], df['pressure'], color='black')
ax1.set_ylabel('Pressure [hPa]')
fig.suptitle('Rendy Zandika_26050120130057_A', fontsize=18)

# Wind speed , gust, directionn
ax2.plot(df['time'], df['wind_speed'], color='tab:orange')
ax2.plot(df['time'], df['wind_gust'], color='tab:olive', linestyle='--')
ax2b.plot(df['time'], df['wind_direction'], color='tab:blue', linestyle='-')
ax2.set_ylabel('Wind Speed [m/s]')
ax2b.set_ylabel('Wind Direction')

# Water temperature
ax3.plot(df['time'], df['water_temperature'], color='tab:brown')
ax3.set_ylabel('Water Temperature [degC]')

plt.show()
```

### 3.4.3 Hasil Permodelan Hidrodinamika 2
![Pressure, Wind Speed, Wind Direction, Water Temperature](https://user-images.githubusercontent.com/105728766/169687474-a6c26811-8994-4fa1-8f9f-c8bc26c9083b.png)


## 4. Penutup 
Demikianlah tugas akhir praktikum pemodelan oseanografi ini kami buat. Seluruh authors memohon maaf apabila terdapat kesalahan dalam tugas akhir ini. Tim 2 selaku author dari repositori kali ini juga mengucapkan terimakasih kepada:

1. Prof. Dr. Denny Nugroho Sugianto, S.T., M.Si. selaku dosen pengampu mata kuliah Pemodelan Oseanografi
2. Dr. Aris Ismanto, S.Si., M.Si. selaku dosen pengampu mata kuliah Pemodelan Oseanografi
3. Rikha Widiaratih, S.Si., M.Si. selaku dosen pengampu mata kuliah Pemodelan Oseanografi
4. Dr. Elis Indrayanti, S.T., M.Si. selaku dosen pengampu mata kuliah Pemodelan Oseanografi
5. Tim asisten Praktikum Pemodelan Oseanografi 2022 yang selalu mendampingi dalam pengerjaan tugas akhir ini
6. Seluruh rekan-rekan Oseanografi 2020 yang turut mendukung tersusunnya repositori ini

Jika terdapat pertanyaan mengenai repository ini, silakan menghubungi:

Salsabila Auliya Putri: https://bit.ly/CP-RepositoryPemosTim2
