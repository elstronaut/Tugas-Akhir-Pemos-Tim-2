# Tugas-Akhir-Pemos-Tim-2
Repositori ini dibuat untuk memenuhi Tugas Akhir Praktikum Pemodelan Oseanografi Oseanografi 2022. Repositori ini memuat IPYNB file yang dapat memproses beberapa persamaan untuk pemodelan oseanografi. Pengerjaan untuk repositori kali ini menggunakan bahasa pemrograman python yang dapat dilakukan pada beberapa platform seperti Google Colaboratory, VS Code, dan Jupyter Notebook. Sedangkan untuk library yang digunakan kali ini adalah Numpy, Matplotlib, Python, Siphon. Seluruh script yang dibuat adalah hasil tim 2 Oseanografi 2020. Semoga dapat bermanfaat!

# 1. Authors Tim 2
1. Aditya Yoga Pratama
2. Refaldi Rizky Maulana 26050120130048 Oseanografi A
3. Rendy Zandika 26050120130057 Oseanografi A
4. Salsabila Auliya Putri 26050120120025 Oseanografi A
5. Aqidatul Izzah 26050120140167 Oseanografi B 
6. Ahmad Nico Fitriadi 26050120140134 Osenografi B 
7. Michael Joshua Xavier 26050120140045 Osenografi B
8. Raza Izzuddien Q. R. 26050120170001 Oseanografi B

# 2. Metode Pengerjaan
- Modul 1: Adveksi 1D
- Modul 2: Adveksi-Difusi 2D
- Modul 3: Hidrodinamika 1D
- Modul 4: Hidrodinamika 2D

## 2.1 Modul 1: Adveksi 1D
Adveksi merupakan 

## 2.2 Modul 2: Adveksi-DIfusi 2D
Adveksi-difusi menggunakan 

- Diskretisasi adveksi:
- Diskretisasi difusi:

## 2.3 Modul 3: Hidrodinamika 1D

Untuk membuat Grafik digunakan script:
> def rand_col_hex_string():
>    return f'#{format(np.random.randint(0,16777215), "#08x")[2:]}'

> hasilu_np = np.array(hasilu)
> hasilz_np = np.array(hasilz)

> fig0, ax0 = plt.subplots(figsize=(12,8))
> for i in range(1, 16):
>    col0 = rand_col_hex_string()
>    line, = ax0.plot(hasilu_np[:,i-1], c=col0, label=f'n={i}')
>    ax0.legend()
    
>    ax0.set(xlabel='Waktu', ylabel='Kecepatan Arus',
>           title='''KELOMPOK 2_OSEANOGRAFI 2020_PRAKTIKUM PEMODELAN OSEANOGRAFI 2022
>           Perubahan Kecepatan Arus Dalam Grid Tertentu di Sepanjang Waktu''')
>    ax0.grid()
    
> fig1, ax1 = plt.subplots(figsize=(12,8))
> for i in range(1, 16):
>    col1 = rand_col_hex_string()
>    line, = ax1.plot(hasilz_np[:,i-1], c=col1, label=f'n={i}')
>    ax1.legend()
    
>    ax1.set(xlabel='Waktu', ylabel='Elevasi Muka Air',
>           title='''KELOMPOK 2_OSEANOGRAFI 2020_PRAKTIKUM PEMODELAN OSEANOGRAFI 2022
>           Perubahan Elevasi Permukaan Air Dalam Grid Tertentu di Sepanjang Waktu''')
>    ax1.grid()
    
> fig2, ax2 = plt.subplots(figsize=(12,8))
> for i in range(1, 16):
>    col2 = rand_col_hex_string()
>    line, = ax2.plot(hasilu_np[i-1], c=col2, label=f't={i}')
>    ax2.legend()
    
>    ax2.set(xlabel='Grid', ylabel='Kecepatan Arus',
>           title='''KELOMPOK 2_OSEANOGRAFI 2020_PRAKTIKUM PEMODELAN OSEANOGRAFI 2022
>           Perubahan Kecepatan Arus Dalam Waktu Tertentu di Sepanjang Grid''')
>    ax2.grid()
    
> fig3, ax3 = plt.subplots(figsize=(12,8))
> for i in range(1, 16):
>    col3 = rand_col_hex_string()
>    line, = ax3.plot(hasilz_np[i-1], c=col3, label=f't={i}')
>    ax3.legend()
    
>    ax3.set(xlabel='Grid', ylabel='Elevasi Muka Air',
>           title='''KELOMPOK 2_OSEANOGRAFI 2020_PRAKTIKUM PEMODELAN OSEANOGRAFI 2022
>           Perubahan Elevasi Permukaan Air Dalam Waktu Tertentu di Sepanjang Grid''')
>    ax3.grid()
    
> plt.show()

## 2.4 Modul 4: Hidrodinamika 2D
