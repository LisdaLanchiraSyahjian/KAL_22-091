---
title: determinan
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

# Determinan Matrik

Determinant (determinan) matriks adalah suatu nilai skalar yang dihitung dari elemen-elemen sebuah matriks persegi (matriks dengan jumlah baris dan kolom yang sama). Determinan memberikan informasi penting tentang sifat-sifat matriks tersebut, seperti apakah matriks tersebut memiliki invers atau tidak. Determinan memiliki sifat-sifat determinan yaitu matrik singular dan non singular. Matrik disebut singular jika tidak  meiliki invers, sedangkan matrik disebut nonsingular jika memiliki invers. Cara menghitung determinan ada berbagai metode, jika ordo matrik 2x2 dapoat dihitung dengan cara : 

contoh :

$
\left[
\begin{array}{ccc|c}
1 & 2  \\
2 & 4 
\end{array}
\right]
$

**det (A) = ad - bc**
det (A) = (1X4) - (2X4)
        = 4 - 8 
        = -4
**maka det (A) adalah -4**

sedangkan untuk matriks dengan ordo 3x3, 4x4, 5x5 bisa menggunakan metode minor matriks dan cofaktor matrik.


### Minor Matrik

Minor Matriks adalah determinan dari submatriks yang diperoleh dengan menghapus satu baris dan satu kolom tertentu dari matriks asli. Konsep ini digunakan dalam perhitungan determinan, kofaktor, dan invers matriks.


**Langkah-langkah mencari Minor Matriks**
1. Pilih elemen aij yang akan dihitung minornya
2. Hapus baris ke-i dan kolom ke j dari matriks
3. Hitung determinan dari submatriks yang tersisa

### Cofaktor Matrik

Cofaktor dalam matriks adalah bilangan yang diperoleh dari minor suatu elemen dalam matriks, dikalikan dengan tanda $(-1)^i+j$  dimana :
- i adalah indeks baris elemen tersebut
- j adalah indeks kolom elemen tersebut

**Langkah-langkah mencari kofaktor matriks**
1. Pilih elemen 𝑎𝑖𝑗 dalam matriks.
2. Hapus baris ke-𝑖 dan kolom ke-𝑗 dari matriks tersebut.
3. Hitung determinannya (ini disebut minor 𝑀𝑖𝑗).
4. Kalikan hasil minor dengan $(-1)^i^+j$ untuk mendapatkan kofaktor Cij.


### Mencari Determinan dengan Konsep Minor dan Cofaktor Matrik

**Contoh Soal dengan Matriks Ordo 3x3**

$
\left[
\begin{array}{ccc|c}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9 
\end{array}
\right]
$

**Menggunakan Minor Matriks:**
- Mencari minor *M*11 
- Menghapus baris ke-1 kolom ke-1
- makan submatrik yang tersisa adalah

$
\left[
\begin{array}{ccc|c}
5 & 6 \\
8 & 9 
\end{array}
\right]
$

- Hitung determinan submatrik tersebut dengan rumun ad - bc

*M*11 = (5×9)−(6×8)=45−48=−3

**Menggunakan Cofaktor Matriks:**
- Mencari cofaktor *C*11
- hapus baris ke-1 kolom ke-1
- maka submatrik yang tersisa adalah

$
\left[
\begin{array}{ccc|c}
5 & 6 \\
8 & 9 
\end{array}
\right]
$

- hitung determinan minor :

*M*11 =(5×9)−(6×8)=45−48=−3

- Kalikan dengan tanda $(-1)^1^+1$ = 1 :
*C*11 = 1 x (-3) = -3

