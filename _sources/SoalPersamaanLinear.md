# Contoh soal 5 persamaan 5 variabel
Contoh soal 5 persamaan 5 variabel

$$
\begin{bmatrix}
x_1 + x_2 + x_3 + x_4 + x_5 = 15 \\
2x_1 + 3x_2 + x_3 + x_4 + x_5 = 20 \\
x_1 + x_2 + 2x_3 + 3x_4 + x_5 = 24 \\
3x_1 + x_2 + x_3 + 2x_4 + x_5 = 18 \\
x_1 + 2x_2 + x_3 + x_4 + 3x_5 = 26
\end{bmatrix}
$$

Ini dalam bentuk Matriks Augmanted

$$
\begin{bmatrix}
1 & 1 & 1 & 1 & 1 & 15 \\
2 & 3 & 1 & 1 & 1 & 20 \\
1 & 1 & 2 & 3 & 1 & 24 \\
3 & 1 & 1 & 2 & 1 & 18 \\
1 & 2 & 1 & 1 & 3 & 26
\end{bmatrix}
$$


# **cara penyelesaiannya**
## langkah 1 Menghilangkan $x$1

$$
R_2 = R_2-2R_1\\
R_3 = R_3-R_1\\
R_4 = R_4-3R_1\\
R_5 = R_5-R_1
$$

### Hasil Eliminasi 
$$
\begin{bmatrix}
1 & 1 & 1 & 1 & 1 & 15 \\
0 & 1 & -1 & -1 & -1 & -10 \\
0 & 0 & 1 & 2 & 0 & 9 \\
0 & -2 & -2 & -1 & -2 & -27 \\
0 & 1 & 0 & 0 & 2 & 11
\end{bmatrix}
$$

## langkah 2 menghilangkan $x$2

$$
R_4 = R_4+2R_2\\
R_5 = R_5-R_2
$$

### Hasil Eliminasi 

$$
\begin{bmatrix}
1 & 1 & 1 & 1 & 1 & 15 \\
0 & 1 & -1 & -1 & -1 & -10 \\
0 & 0 & 1 & 2 & 0 & 9 \\
0 & 0 & -4 & -3 & -4 & -47 \\
0 & 0 & 1 & 1 & 3 & 21
\end{bmatrix}
$$

## Langkah 3 Menghilangkan $x$3

$$
R_4 = R_4+4R_3\\
R_5 = R_5-R_3
$$

### Hasil Eliminasi

$$
\begin{bmatrix}
1 & 1 & 1 & 1 & 1 & 15 \\
0 & 1 & -1 & -1 & -1 & -10 \\
0 & 0 & 1 & 2 & 0 & 9 \\
0 & 0 & 0 & 5 & -4 & -11 \\
0 & 0 & 0 & -1 & 3 & 12
\end{bmatrix}
$$

## Langkah 4 Menghilangkan $x$4

$$
R_5 = R_5+\frac{1}{5}R_4\\
$$

### Hasil Eliminasi

$$
\begin{bmatrix}
1 & 1 & 1 & 1 & 1 & 15 \\
0 & 1 & -1 & -1 & -1 & -10 \\
0 & 0 & 1 & 2 & 0 & 9 \\
0 & 0 & 0 & 5 & -4 & -11 \\
0 & 0 & 0 & 0 & 11 & 55
\end{bmatrix}
$$

## Langkah 5
Menentukan $x$5

$$
11x_5 = 55\\
x_5 = \frac{55}{11} = 5\\
x_5 = 5\\
$$

Menentukan $x$4

$$
5x_4-4x_5 = -11\\
disubtitusi\\
5x_4-4(5) = -11\\
5x_4-20 = -11\\
5x_4 = 9
x_4 = 4
$$

Menentukan $x$3

$$
x_3 + 2x_4=9\\
disubstitusi\\
x_3 + 2(4) = 9\\
x_3 + 8 = 9\\
x_3 = 3
$$

Menentukan $x$2

$$
x_2​−x_3​−x_4​−x_5​=−10\\
disubtitusi\\
x_2​−3−4−5=−10\\
x_2​−12=−10\\
x_2​=2
$$

Menentukan $x$1

$$
x_1​+x_2​+x_3​+x_4​+x_5​=15\\
Disubtitusi\\
x_1​+2+3+4+5=15\\
x_1​+14=15\\
x1​=1
$$

Hasil Persamaan

$$
\begin{bmatrix}
1 & 0 & 0 & 0 & 0 & 1 \\
0 & 1 & 0 & 0 & 0 & 2 \\
0 & 0 & 1 & 0 & 0 & 3 \\
0 & 0 & 0 & 1 & 0 & 4 \\
0 & 0 & 0 & 0 & 1 & 5
\end{bmatrix}
$$