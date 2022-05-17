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

Perhitungan u dan v
``` 
u = C * np.sin(theta*np.pi/180)
v = C * np.cos(theta*np.pi/180)
dt_count = 1/((abs(u)/(q*dx))+(abs(v)/(q*dy))+(2*ad/(q*dx*2))+(2*ad/(q*dy*2)))

Nx = int(x/dx)      #number of mesh in x direction
Ny = int(y/dy)      #number of mesh in y direction
Nt = int(Tend/dt)   #number of timesteps
``` 

Perhitungan Titik Polutan
``` 
px1 = int(px/dx)
py1 = int(py/dy)
``` 

Fungsi disederhanakan 
``` 
lx = u*dt/dx
ly = v*dt/dy
ax = ad*dt/dx**2
ay = ad*dt/dy**2
cfl = (2*ax + 2*ay + abs(lx) + abs(ly))
``` 

Perhitungan CFL
``` 
if cfl >= q:
    print('CFL Violated, Please use dt :'+str(round(dt_count,4)))
    sys.exit()
``` 

Pembuatan Grid
``` 
x_grid = np.linspace(0-dx, x+dx, Nx+2)      #Ghostnode pada boundary
y_grid = np.linspace(0-dx, y+dy, Ny+2)      #Ghostnode pada boundary
t = np.linspace(0, Tend, Nt+1)
x_mesh,y_mesh = np.meshgrid(x_grid,y_grid)
F = np.zeros((Nt+1, Ny+2, Nx+2))
#Kondisi Awal(Initial Condition)
F[0,py1,px1] = Ic
#%%
#Iterasi
for n in range (0, Nt):
    for i in range (1,Ny+1):
        for j in range(1,Nx+1):
            F[n+1,i,j]=((F[n,i,j]*(1-abs(lx)-abs(ly)))  + \
                        (0.5*(F[n,i-1,j]*(ly+abs(ly)))) + \
                        (0.5*(F[n,i+1,j]*(abs(ly)-ly))) + \
                        (0.5*(F[n,i,j-1]*(lx+abs(lx)))) + \
                        (0.5*(F[n,i,j+1]*(abs(lx)-lx))) + \
                        (ay*(F[n,i+1,j]-2*(F[n,i,j])+F[n,i-1,j])) + \
                        (ax*(F[n,i,j+1]-2*(F[n,i,j])+F[n,i,j-1]))) #Diskritisasi
    #Syarat Batas (Dirichlet Boundary Condition)
    F[n+1,0,:] = 0 #BC Bawah
    F[n+1,:,0] = 0 #BC Kiri
    F[n+1,Ny+1,:] = 0 #BC Atas
    F[n+1,:,Nx+1] = 0 #BC Kanan
``` 

Output Gambar
``` 
    plt.clf()
    plt.pcolor(x_mesh, y_mesh, F[n+1,:,:],cmap = 'jet',shading ='auto',edgecolors = 'k')
    cbar = plt.colorbar(orientation = 'vertical', shrink = 0.95, extend = 'both')
    cbar.set_label(label='Concentration', size = 8)
    #plt.clim(0,100)
    plt.title('Rendy Zandika_26050120130057 \n t='+str(round(dt*(n+1),3))+', Initial Condition='+str(Ic),fontsize=10)
    plt.xlabel('x_grid',fontsize=9)
    plt.ylabel('y_grid',fontsize=9)
    plt.axis([0, x, 0, y])
    #plt.pause(0.01)
    plt.savefig(str(n+1)+'.jpg', dpi = 300)
    plt.pause(0.01)
    plt.close()
    print('running timestep ke:' +str(n+1) + ' dari:' +str(Nt) + '('+ percentage(n+1,Nt)+')')
    #print('Nilai CFL:' +str(cfl) + ' dengan arah:' +str(theta))
``` 


   







