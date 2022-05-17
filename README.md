# Tugas-Akhir-Pemos-Tim-2
Repositori ini dibuat untuk memenuhi Tugas Akhir Praktikum Pemodelan Oseanografi Oseanografi 2022. Repositori ini memuat executable (.exe) file yang dapat memproses beberapa persamaan untuk penyelesaian perhitungan numerik. Pengerjaan untuk repositori kali ini menggunakan bahasa pemrograman python yang dapat dilakukan pada beberapa platform seperti Google Colaboratory, VS Code, dan Jupyter Notebook. Sedangkan untuk library yang digunakan kali ini adalah Numpy, Matplotlib, Python, Siphon. Seluruh script yang dibuat adalah hasil tim 2 Oseanografi 2020. Semoga dapat bermanfaat!








Modul 2 : Adveksi-Difusi 2 Dimensi 

Import Package
``` 
import matplotlib.pyplot as plt
import numpy as np
import sys 
```

Pendefenisian dan Memasukkan Parameter

``` 
def percentage(part, whole):
        percentage = 100 * float(part)/float(whole)
        return str(round(percentage,2)) + "X"

#Memasukkan Parameter Awal
C = 1.75    #Kecepatan Aliran
ad = 1.75   #KoSefisien Difusi
#Arah Arus (Berdasarkan Geographic Convention)
theta = 135  #Skenario I 
#Parameter Lanjutan
q = 0.95    #Kriteria Kestabilan
x = 500     #Jumlah Grid Horizontal (x)
y = 500     #Jumlah Grid Vertikal (y)
dx = 5      
dy = 5
Tend = 107   #Lama Simulasi
#Tend = 1
dt = 0.5
#Polutan
px = 250   #Polutan pada grid x
py = 237   #Polutan pada grid y
Ic = 1075   #Jumlah Polutan
``` 



