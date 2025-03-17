---
title: spl2
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: '0.13'
    jupytext_version: '1.11.5'
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Penyelesaian Sistem Persamaan Linier
### Operasi Baris Elementer
Operasi baris elementer (OBE) adalah operasi yang dilakukan pada baris suatu matriks untuk mengubahnya menjadi bentuk yang lebih sederhana. OBE dapat digunakan untuk menyelesaikan sistem persamaan linear (SPL) dan menentukan invers matriks. 

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
#### Soal 1

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

#### Soal 3

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


# **Matriks**

Matriks adalah susunan bilangan berbentuk persegi panjang yang diatur dalam baris dan kolom. Matriks biasanya digunakan dalam berbagai bidang seperti matematika, fisika, dan ilmu komputer untuk merepresentasikan sistem persamaan linear, transformasi geometris, dan operasi lainnya.

## Operasi Matrik

### Penjumlahan

Dua matriks dapat dijumlahkan jika memiliki ukuran yang sama. Penjumlahan dilakukan dengan menjumlahkan elemen-elemen yang sesuai.

### Pengurangan

Pengurangan dilakukan dengan cara yang sama seperti penjumlahan, tetapi dengan mengurangi elemen-elemen yang sesuai.

### Perkalian

Perkalian matriks 
𝐴
A dan 
𝐵
B hanya dapat dilakukan jika jumlah kolom pada 
𝐴
A sama dengan jumlah baris pada 
𝐵
B.

#### Contoh Code Untuk Operasi Matriks

```{code-cell} python
import numpy as np

# Definisi matriks
A = np.array([[1, 2], 
              [3, 4]])

B = np.array([[5, 6], 
              [7, 8]])

# Penjumlahan Matriks
penjumlahan = A + B

# Pengurangan Matriks
pengurangan = A - B

# Perkalian Matriks
perkalian = np.dot(A, B)  # atau bisa juga menggunakan A @ B

# Menampilkan hasil
print("Matriks A:\n", A)
print("Matriks B:\n", B)
print("Hasil Penjumlahan:\n", penjumlahan)
print("Hasil Pengurangan:\n", pengurangan)
print("Hasil Perkalian:\n", perkalian)
```

## Penyelesaian Baris Elementer

**Soal 1**

Selesaikan sistem persamaan linear berikut:

$
\left[
\begin{array}{cc}
x_1 + x_2 & = 5 \\
x_1 + 2x_3 & = 6
\end{array}
\right]
$

**Penyelesaian**

Kita menyusun sistem ini dalam bentuk augmented matrix:

$
\left[
\begin{array}{ccc|c}
1 & 1 & 0 & 5 \\
1 & 0 & 2 & 6
\end{array}
\right]
$

Langkah 1: Eliminasi Baris Kedua

Gunakan operasi baris elementer:

$
\[
R_2 \to R_2 - 2R_1
\]
$

Maka matriks menjadi:

$
\left[
\begin{array}{ccc|c}
1 & 1 & 0 & 5 \\
0 & -1 & 2 & 1
\end{array}
\right]
$

Langkah 3: Normalisasi Baris Kedua

Kalikan baris kedua dengan -1

$
\begin{array}{cc}
R_2 → -R_2
\end{array}
$

sehingga diperoleh

$
\left[
\begin{array}{ccc|c}
1 & 1 & 0 & 5 \\
0 & 1 & -2 & -1
\end{array}
\right]
$

Langkah 4: Eliminasi Elemen di Atas Pivot Kedua

Kurangi baris pertama dengan baris kedua:

$
\begin{array}{cc}
R_1 → R_1 - R_2
\end{array}
$

HASILNYA

$
\left[
\begin{array}{ccc|c}
1 & 0 & 2 & 6 \\
0 & 1 & -2 & -1
\end{array}
\right]
$

Langkah 5: Menuliskan Solusi dalam Bentuk Parametrik
Dari matriks ini, kita memiliki:

$
\begin{array}{cc}
1. x_1+2x_3&=6 → x_1&=-2x_3+6\\
2. x_2-2x_3&=-1 → x_2&=2x_3-1\\
3. x_3&=t
\end{array}
$