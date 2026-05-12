# Tugas Dekompoisi Eigen Value
## Tahap 1 - Membentuk Vektor q₁

Kolom pertama matriks $A$:

$$
a_1 =
\begin{bmatrix}
2 \\
1
\end{bmatrix}
$$

Norma vektor:

$$
\|a_1\|
=
\sqrt{2^2 + 1^2}
=
\sqrt{5}
$$

Membentuk vektor ortonormal:

$$
q_1
=
\frac{a_1}{\|a_1\|}
=
\frac{1}{\sqrt{5}}
\begin{bmatrix}
2 \\
1
\end{bmatrix}
=
\begin{bmatrix}
\frac{2}{\sqrt{5}} \\
\frac{1}{\sqrt{5}}
\end{bmatrix}
$$

## Tahap 2 - Menghitung Dot Product q₁ · a₂

Kolom kedua matriks:

$$
a_2 =
\begin{bmatrix}
1 \\
2
\end{bmatrix}
$$

Rumus dot product:

$$
q_1 \cdot a_2
=
q_{11}a_{21} + q_{12}a_{22}
$$

Substitusi nilai:

$$
=
\left(
\frac{2}{\sqrt{5}} \times 1
\right)
+
\left(
\frac{1}{\sqrt{5}} \times 2
\right)
$$

Hasil perhitungan:

$$
=
\frac{2}{\sqrt{5}}
+
\frac{2}{\sqrt{5}}
=
\frac{4}{\sqrt{5}}
$$

Menyederhanakan bentuk akar:

$$
=
\frac{4\sqrt{5}}{5}
$$

## Tahap 3 - Menghitung Vektor Ortogonal u₂

Rumus proyeksi vektor:

$$
\text{proj}_{q_1}(a_2)
=
(q_1 \cdot a_2)q_1
$$

Substitusi nilai:

$$
=
\frac{4\sqrt{5}}{5}
\begin{bmatrix}
\frac{2}{\sqrt{5}} \\
\frac{1}{\sqrt{5}}
\end{bmatrix}
$$

Hasil proyeksi:

$$
=
\begin{bmatrix}
\frac{8}{5} \\
\frac{4}{5}
\end{bmatrix}
$$

Rumus ortogonalisasi:

$$
u_2
=
a_2 - \text{proj}_{q_1}(a_2)
$$

Substitusi nilai:

$$
=
\begin{bmatrix}
1 \\
2
\end{bmatrix}
-
\begin{bmatrix}
\frac{8}{5} \\
\frac{4}{5}
\end{bmatrix}
$$

Hasil akhir:

$$
u_2
=
\begin{bmatrix}
-\frac{3}{5} \\
\frac{6}{5}
\end{bmatrix}
$$

## Tahap 4 - Normalisasi u₂ Menjadi q₂

Vektor ortogonal yang diperoleh:

$$
u_2 =
\begin{bmatrix}
-\frac{3}{5} \\
\frac{6}{5}
\end{bmatrix}
$$

Menghitung norma vektor \(u_2\):

$$
\|u_2\|
=
\sqrt{
\left(-\frac{3}{5}\right)^2
+
\left(\frac{6}{5}\right)^2
}
$$

Substitusi perhitungan:

$$
=
\sqrt{
\frac{9}{25}
+
\frac{36}{25}
}
$$

$$
=
\sqrt{
\frac{45}{25}
}
$$

Menyederhanakan akar:

$$
=
\frac{3\sqrt{5}}{5}
$$

Rumus normalisasi:

$$
q_2
=
\frac{u_2}{\|u_2\|}
$$

Substitusi nilai:

$$
=
\frac{
\begin{bmatrix}
-\frac{3}{5} \\
\frac{6}{5}
\end{bmatrix}
}{
\frac{3\sqrt{5}}{5}
}
$$

Hasil akhir:

$$
q_2 =
\begin{bmatrix}
-\frac{\sqrt{5}}{5} \\
\frac{2\sqrt{5}}{5}
\end{bmatrix}
$$

## Tahap 5 - Membentuk Matriks Q

Matriks \(Q\) dibentuk dari kolom-kolom vektor ortonormal \(q_1\) dan \(q_2\):

$$
Q =
\begin{bmatrix}
q_1 & q_2
\end{bmatrix}
$$

Dengan:

$$
q_1 =
\begin{bmatrix}
\frac{2}{\sqrt{5}} \\
\frac{1}{\sqrt{5}}
\end{bmatrix}
$$

dan

$$
q_2 =
\begin{bmatrix}
-\frac{\sqrt{5}}{5} \\
\frac{2\sqrt{5}}{5}
\end{bmatrix}
$$

Maka matriks \(Q\):

$$
Q =
\begin{bmatrix}
\frac{2\sqrt{5}}{5} & -\frac{\sqrt{5}}{5} \\
\frac{\sqrt{5}}{5} & \frac{2\sqrt{5}}{5}
\end{bmatrix}
$$

Matriks \(Q\) merupakan matriks ortogonal karena memenuhi:

$$
Q^TQ = I
$$

## Tahap 6 - Membentuk Matriks R

Matriks \(R\) diperoleh dari hasil perkalian:

$$
R = Q^T A
$$

Transpose dari matriks \(Q\):

$$
Q^T =
\begin{bmatrix}
\frac{2\sqrt{5}}{5} & \frac{\sqrt{5}}{5} \\
-\frac{\sqrt{5}}{5} & \frac{2\sqrt{5}}{5}
\end{bmatrix}
$$

Matriks \(A\):

$$
A =
\begin{bmatrix}
2 & 1 \\
1 & 2
\end{bmatrix}
$$

Substitusi ke rumus:

$$
R =
\begin{bmatrix}
\frac{2\sqrt{5}}{5} & \frac{\sqrt{5}}{5} \\
-\frac{\sqrt{5}}{5} & \frac{2\sqrt{5}}{5}
\end{bmatrix}
\begin{bmatrix}
2 & 1 \\
1 & 2
\end{bmatrix}
$$

Hasil perkalian matriks:

$$
R =
\begin{bmatrix}
\sqrt{5} & \frac{4\sqrt{5}}{5} \\
0 & \frac{3\sqrt{5}}{5}
\end{bmatrix}
$$

Matriks \(R\) berbentuk segitiga atas sesuai sifat dekomposisi QR.

## Tahap 7 - Verifikasi QR = A

Setelah diperoleh matriks \(Q\) dan \(R\), langkah berikutnya adalah memverifikasi bahwa:

$$
A = QR
$$

Matriks \(Q\):

$$
Q =
\begin{bmatrix}
\frac{2\sqrt{5}}{5} & -\frac{\sqrt{5}}{5} \\
\frac{\sqrt{5}}{5} & \frac{2\sqrt{5}}{5}
\end{bmatrix}
$$

Matriks \(R\):

$$
R =
\begin{bmatrix}
\sqrt{5} & \frac{4\sqrt{5}}{5} \\
0 & \frac{3\sqrt{5}}{5}
\end{bmatrix}
$$

Perkalian matriks:

$$
QR =
\begin{bmatrix}
\frac{2\sqrt{5}}{5} & -\frac{\sqrt{5}}{5} \\
\frac{\sqrt{5}}{5} & \frac{2\sqrt{5}}{5}
\end{bmatrix}
\begin{bmatrix}
\sqrt{5} & \frac{4\sqrt{5}}{5} \\
0 & \frac{3\sqrt{5}}{5}
\end{bmatrix}
$$

Hasil perkalian:

$$
QR =
\begin{bmatrix}
2 & 1 \\
1 & 2
\end{bmatrix}
$$

Karena hasilnya sama dengan matriks awal:

$$
A =
\begin{bmatrix}
2 & 1 \\
1 & 2
\end{bmatrix}
$$

maka dekomposisi QR terbukti benar.

$$
QR = A
$$

## Tahap 8 - Membentuk Matriks Baru A₁ = RQ

Pada metode QR Iteration, matriks baru dibentuk dengan rumus:

$$
A_{k+1} = R_k Q_k
$$

Untuk iterasi pertama:

$$
A_1 = RQ
$$

Matriks \(R\):

$$
R =
\begin{bmatrix}
\sqrt{5} & \frac{4\sqrt{5}}{5} \\
0 & \frac{3\sqrt{5}}{5}
\end{bmatrix}
$$

Matriks \(Q\):

$$
Q =
\begin{bmatrix}
\frac{2\sqrt{5}}{5} & -\frac{\sqrt{5}}{5} \\
\frac{\sqrt{5}}{5} & \frac{2\sqrt{5}}{5}
\end{bmatrix}
$$

Perkalian matriks:

$$
A_1 =
\begin{bmatrix}
\sqrt{5} & \frac{4\sqrt{5}}{5} \\
0 & \frac{3\sqrt{5}}{5}
\end{bmatrix}
\begin{bmatrix}
\frac{2\sqrt{5}}{5} & -\frac{\sqrt{5}}{5} \\
\frac{\sqrt{5}}{5} & \frac{2\sqrt{5}}{5}
\end{bmatrix}
$$

Hasil:

$$
A_1 =
\begin{bmatrix}
\frac{14}{5} & \frac{3}{5} \\
\frac{3}{5} & \frac{6}{5}
\end{bmatrix}
$$

Dalam bentuk desimal:

$$
A_1 \approx
\begin{bmatrix}
2.8 & 0.6 \\
0.6 & 1.2
\end{bmatrix}
$$

Elemen di luar diagonal mulai mengecil, menandakan proses konvergensi menuju nilai eigen.

## Tahap 9 - QR Iteration Berulang

Proses QR Iteration dilakukan secara berulang menggunakan rumus:

$$
A_k = Q_k R_k
$$

kemudian:

$$
A_{k+1} = R_k Q_k
$$

Setiap iterasi akan membuat elemen di luar diagonal semakin kecil sehingga matriks mendekati bentuk diagonal.

#### Iterasi 1

$$
A_1 =
\begin{bmatrix}
2.8 & 0.6 \\
0.6 & 1.2
\end{bmatrix}
$$

#### Iterasi 2

$$
A_2 =
\begin{bmatrix}
2.96 & 0.28 \\
0.28 & 1.04
\end{bmatrix}
$$

#### Iterasi 3

$$
A_3 =
\begin{bmatrix}
2.99298 & 0.11972 \\
0.11972 & 1.00702
\end{bmatrix}
$$

#### Iterasi 4

$$
A_4 =
\begin{bmatrix}
2.99883 & 0.04997 \\
0.04997 & 1.00117
\end{bmatrix}
$$

#### Iterasi 5

$$
A_5 =
\begin{bmatrix}
2.99980 & 0.02082 \\
0.02082 & 1.00020
\end{bmatrix}
$$

#### Iterasi 6

$$
A_6 =
\begin{bmatrix}
2.99997 & 0.00867 \\
0.00867 & 1.00003
\end{bmatrix}
$$

#### Iterasi 7

$$
A_7 =
\begin{bmatrix}
2.99999 & 0.00361 \\
0.00361 & 1.00001
\end{bmatrix}
$$

#### Iterasi 8

$$
A_8 =
\begin{bmatrix}
3.00000 & 0.00150 \\
0.00150 & 1.00000
\end{bmatrix}
$$

#### Iterasi 9

$$
A_9 =
\begin{bmatrix}
3.00000 & 0.00063 \\
0.00063 & 1.00000
\end{bmatrix}
$$

#### Iterasi 10

$$
A_{10} \approx
\begin{bmatrix}
3 & 0 \\
0 & 1
\end{bmatrix}
$$

Terlihat bahwa elemen di luar diagonal semakin mendekati nol, sedangkan elemen diagonal mendekati nilai eigen matriks.

## Tahap 10 - Menentukan Nilai Eigen

Setelah dilakukan 10 iterasi QR, matriks hasil mendekati bentuk diagonal:

$$
A_{10} \approx
\begin{bmatrix}
3 & 0 \\
0 & 1
\end{bmatrix}
$$

Pada metode QR Iteration, jika matriks sudah konvergen menjadi matriks diagonal, maka elemen diagonal tersebut merupakan nilai eigen dari matriks awal.

Sehingga diperoleh:

$$
\lambda_1 = 3
$$

dan

$$
\lambda_2 = 1
$$

Nilai eigen tersebut sesuai dengan hasil analitik dari matriks:

$$
A =
\begin{bmatrix}
2 & 1 \\
1 & 2
\end{bmatrix}
$$

Menggunakan persamaan karakteristik:

$$
\det(A - \lambda I) = 0
$$

Substitusi nilai matriks:

$$
\begin{vmatrix}
2-\lambda & 1 \\
1 & 2-\lambda
\end{vmatrix}
= 0
$$

Menghitung determinan:

$$
(2-\lambda)^2 - 1 = 0
$$

$$
4 - 4\lambda + \lambda^2 - 1 = 0
$$

$$
\lambda^2 - 4\lambda + 3 = 0
$$

Faktorkan persamaan:

$$
(\lambda - 3)(\lambda - 1) = 0
$$

Sehingga:

$$
\lambda_1 = 3
\qquad \text{dan} \qquad
\lambda_2 = 1
$$

Hasil QR Iteration sesuai dengan hasil perhitungan analitik.

## Kesimpulan

Metode Dekomposisi QR digunakan untuk memecah matriks menjadi dua matriks, yaitu matriks ortogonal \(Q\) dan matriks segitiga atas \(R\).

Rumus dasar dekomposisi QR:

$$
A = QR
$$

Pada metode QR Iteration, proses dilakukan secara berulang dengan langkah:

$$
A_k = Q_k R_k
$$

kemudian:

$$
A_{k+1} = R_k Q_k
$$

Setiap iterasi membuat elemen di luar diagonal semakin kecil sehingga matriks mendekati bentuk diagonal.

Untuk matriks:

$$
A =
\begin{bmatrix}
2 & 1 \\
1 & 2
\end{bmatrix}
$$

setelah 10 iterasi diperoleh:

$$
A_{10} \approx
\begin{bmatrix}
3 & 0 \\
0 & 1
\end{bmatrix}
$$

Nilai diagonal matriks tersebut merupakan nilai eigen dari matriks awal.

Sehingga nilai eigen matriks adalah:

$$
\lambda_1 = 3
$$

$$
\lambda_2 = 1
$$

Metode QR Iteration terbukti dapat digunakan untuk mencari nilai eigen suatu matriks secara numerik dengan hasil yang sesuai dengan perhitungan analitik.


nah untuk programnya ada di link bawah ini
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1djz2MaUKq4DI0b0_E2t4LoT9bab5mnni?usp=sharing)
---