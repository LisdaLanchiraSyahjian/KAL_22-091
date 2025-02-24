---
title: spl2

---

## Penyelesaian Sistem Persamaan Linier
### Operasi Baris Elementer
### Eliminasi Gaus
Eliminasi Gauss adalah algoritma yang digunakan untuk menyelesaikan sistem persamaan linear (SPL). Algoritma ini mengubah matriks koefisien SPL menjadi matriks segitiga atas. 

#### Contoh Soal
contoh soal 1

$
\begin{array}{cc}
x_1+2x_2+3x_3&=6\\
2x_1+4x_2+6x_3&=12\\
x_2+x_3&=2
\end{array}
$

contoh soal 2

$
\begin{array}{cc}
x_1+x_2+x_3&=3\\
2x_2+x_3&=5\\
x_2+2x_3&=3
\end{array}
$

contoh soal 3

$
\begin{array}{cc}
2x_1+2x_2&=4\\
x_1+x_2&=2
\end{array}
$

contoh soal 4

$
\begin{array}{cc}
x_1+x_2&=5\\
x_1+2x_3&=6
\end{array}
$

#### Penyelesaian
##### Soal 1

$
\left[
\begin{array}{ccc|c}
1 & 2 & 3 & 6 \\
2 & 4 & 6 & 12 \\
0 & 1 & 1 & 2
\end{array}
\right]
$

hitung baris kedua

$
\begin{array}{cc}
R_2 → R_2-2R_1
\end{array}
$

maka akan menghasilkan

$
\left[
\begin{array}{ccc|c}
1 & 2 & 3 & 6 \\
0 & 0 & 0 & 0 \\
0 & 1 & 1 & 2
\end{array}
\right]
$

##### Soal 3

$
\left[
\begin{array}{cc|c}
2 & 2 & 4 \\
1 & 1 & 2
\end{array}
\right]
$

hitung baris pertama

$
\begin{array}{cc}
R_1 → R_1-2R_2
\end{array}
$

maka akan menghasilkan

$
\left[
\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 0 & 0
\end{array}
\right]
$





