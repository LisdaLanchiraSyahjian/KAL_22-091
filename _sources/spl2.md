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
\documentclass{article}
\usepackage{amsmath, amssymb}
\begin{document}

\title{Penyelesaian Sistem Persamaan Linear dengan Operasi Baris Elementer}
\author{Menggunakan Eliminasi Gauss}
\date{\today}
\maketitle

\section*{Soal}
Diberikan sistem persamaan linear dalam bentuk matriks augmented:

\[
\begin{bmatrix}
1 & 2 & -1 & | & 3 \\
2 & 3 & 1 & | & 7 \\
1 & -1 & 2 & | & 2
\end{bmatrix}
\]

Gunakan operasi baris elementer untuk menyelesaikan sistem ini.

\section*{Penyelesaian}

\subsection*{Langkah 1: Membuat Elemen (1,1) menjadi 1}
Matriks awal sudah memiliki pivot 1 di posisi (1,1), sehingga tidak perlu perubahan:

\[
\begin{bmatrix}
1 & 2 & -1 & | & 3 \\
2 & 3 & 1 & | & 7 \\
1 & -1 & 2 & | & 2
\end{bmatrix}
\]

\subsection*{Langkah 2: Membuat Elemen di Bawah Pivot Menjadi 0}

Operasi baris:
\begin{align*}
R_2 &\leftarrow R_2 - 2R_1 \\
R_3 &\leftarrow R_3 - R_1
\end{align*}

Hasilnya:

\[
\begin{bmatrix}
1 & 2 & -1 & | & 3 \\
0 & -1 & 3 & | & 1 \\
0 & -3 & 3 & | & -1
\end{bmatrix}
\]

\subsection*{Langkah 3: Membuat Elemen (2,2) Menjadi 1}

Bagi baris kedua dengan -1:

\[
R_2 \leftarrow -R_2
\]

Sehingga diperoleh:

\[
\begin{bmatrix}
1 & 2 & -1 & | & 3 \\
0 & 1 & -3 & | & -1 \\
0 & -3 & 3 & | & -1
\end{bmatrix}
\]

\subsection*{Langkah 4: Membuat Elemen di Bawah Pivot (Kolom 2) Menjadi 0}

Operasi:
\[
R_3 \leftarrow R_3 + 3R_2
\]

Hasilnya:

\[
\begin{bmatrix}
1 & 2 & -1 & | & 3 \\
0 & 1 & -3 & | & -1 \\
0 & 0 & -6 & | & -4
\end{bmatrix}
\]

\subsection*{Langkah 5: Membuat Elemen (3,3) Menjadi 1}

Bagi baris ketiga dengan -6:

\[
R_3 \leftarrow \frac{R_3}{-6}
\]

Sehingga diperoleh:

\[
\begin{bmatrix}
1 & 2 & -1 & | & 3 \\
0 & 1 & -3 & | & -1 \\
0 & 0 & 1 & | & \frac{2}{3}
\end{bmatrix}
\]

\subsection*{Langkah 6: Substitusi Mundur}
Dari baris ketiga:
\[
z = \frac{2}{3}
\]

Dari baris kedua:
\[
y - 3z = -1
\]
\[
y - 3\left(\frac{2}{3}\right) = -1
\]
\[
y - 2 = -1 \Rightarrow y = 1
\]

Dari baris pertama:
\[
x + 2y - z = 3
\]
\[
x + 2(1) - \frac{2}{3} = 3
\]
\[
x = 3 - 2 + \frac{2}{3} = \frac{4}{3}
\]

\subsection*{Jawaban Akhir}
\[
\begin{cases}
x = \frac{4}{3} \\
y = 1 \\
z = \frac{2}{3}
\end{cases}
\]

\end{document}


