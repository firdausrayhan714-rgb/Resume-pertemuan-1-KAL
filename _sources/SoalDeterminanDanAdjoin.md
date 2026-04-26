# Soal Determinan Matriks Dan Adjoin

### A. Hitunglah determinan matrik berikut dengan menggunakan rumus expansi baris

$$
\det(A)=\sum_{k=1}^{n}(-1)^{i+k}a_{ik}M_{ik}
$$

dengan \( M_{ij} \) adalah minor dari matriks \( A \), dan

$$
M_{ij}=\det(A_{ij})
$$

dengan \( A_{ij} \) adalah submatriks yang diperoleh dengan menghapus baris ke-\(i\) dan kolom ke-\(j\) dari matriks \( A_{m \times n} \), untuk

$$
1 \le i,j \le n
$$

#### 1.
$$
A=
\begin{bmatrix}
-7 & -5\\
1 & 4
\end{bmatrix}
$$

#### 2.
$$
A=
\begin{bmatrix}
0 & 2 & -3\\
1 & -2 & -1\\
0 & 0 & 1
\end{bmatrix}
$$

#### 3.
$$
A=
\begin{bmatrix}
1 & -3 & 1 & 1\\
-3 & 1 & 1 & 1\\
1 & 1 & -3 & 1\\
1 & 1 & 1 & -3
\end{bmatrix}
$$

---

### B. Gunakan rumus matriks adjoin untuk menghitung invers dari matriks berikut

$$
(\operatorname{adj}A)_{ij}=(-1)^{i+j}M_{ji}
$$

dan

$$
A^{-1}=\frac{1}{\det(A)}\operatorname{adj}(A)
$$

#### 4.
$$
A=
\begin{bmatrix}
-7 & -5\\
1 & 4
\end{bmatrix}
$$

#### 5.
$$
A=
\begin{bmatrix}
0 & 2 & -3\\
1 & -2 & -1\\
0 & 0 & 1
\end{bmatrix}
$$

#### 6.
$$
A=
\begin{bmatrix}
1 & -3 & 1 & 1\\
-3 & 1 & 1 & 1\\
1 & 1 & -3 & 1\\
1 & 1 & 1 & -3
\end{bmatrix}
$$

### Jawaban
### Penyelesaian Soal Nomor A1

$$
A=
\begin{bmatrix}
-7 & -5\\
1 & 4
\end{bmatrix}
$$

Determinan matriks 2×2:

$$
\det(A)=ad-bc
$$

$$
\det(A)=(-7)(4)-(-5)(1)
$$

$$
=-28+5
$$

$$
=-23
$$

Jadi,

$$
\boxed{\det(A)=-23}
$$

### Penyelesaian Soal Nomor A2

Diketahui matriks:
$$A = \begin{bmatrix} 0 & 2 & -3 \\ 1 & -2 & -1 \\ 0 & 0 & 1 \end{bmatrix}$$

**Langkah-langkah Penyelesaian (Ekspansi Baris Ketiga):**

$$
A=
\begin{bmatrix}
0 & 2 & -3\\
1 & -2 & -1\\
0 & 0 & 1
\end{bmatrix}
$$

Ekspansi baris pertama:

$$
\det(A)=0\cdot M_{11}-2\cdot M_{12}+(-3)\cdot M_{13}
$$

Karena elemen pertama bernilai nol, maka:

$$
\det(A)=-2M_{12}-3M_{13}
$$

Minor \(M_{12}\)

$$
M_{12}=
\begin{vmatrix}
1 & -1\\
0 & 1
\end{vmatrix}
$$

$$
=(1)(1)-(-1)(0)
$$

$$
=1
$$

Minor \(M_{13}\)

$$
M_{13}=
\begin{vmatrix}
1 & -2\\
0 & 0
\end{vmatrix}
$$

$$
=(1)(0)-(-2)(0)
$$

$$
=0
$$

Substitusi:

$$
\det(A)=-2(1)-3(0)
$$

$$
=-2
$$

Jadi,

$$
\boxed{\det(A)=-2}
$$

### Penyelesaian Nomor A3: Determinan Matriks 4x4

$$
A=
\begin{bmatrix}
1 & -3 & 1 & 1\\
-3 & 1 & 1 & 1\\
1 & 1 & -3 & 1\\
1 & 1 & 1 & -3
\end{bmatrix}
$$

Ekspansi baris pertama:

$$
\det(A)=1M_{11}-(-3)M_{12}+1M_{13}-1M_{14}
$$

Minor \(M_{11}\)

$$
M_{11}=
\begin{vmatrix}
1 & 1 & 1\\
1 & -3 & 1\\
1 & 1 & -3
\end{vmatrix}
$$

$$
=1
\begin{vmatrix}
-3 & 1\\
1 & -3
\end{vmatrix}
-1
\begin{vmatrix}
1 & 1\\
1 & -3
\end{vmatrix}
+1
\begin{vmatrix}
1 & -3\\
1 & 1
\end{vmatrix}
$$

$$
=1(9-1)-1(-3-1)+1(1+3)
$$

$$
=8+4+4=16
$$

Minor \(M_{12}\)

$$
M_{12}=
\begin{vmatrix}
-3 & 1 & 1\\
1 & -3 & 1\\
1 & 1 & -3
\end{vmatrix}
$$

$$
=(-3)
\begin{vmatrix}
-3 & 1\\
1 & -3
\end{vmatrix}
-1
\begin{vmatrix}
1 & 1\\
1 & -3
\end{vmatrix}
+1
\begin{vmatrix}
1 & -3\\
1 & 1
\end{vmatrix}
$$

$$
=(-3)(9-1)-1(-3-1)+1(1+3)
$$

$$
=-24+4+4=-16
$$

Minor \(M_{13}\)

$$
M_{13}=
\begin{vmatrix}
-3 & 1 & 1\\
1 & 1 & 1\\
1 & 1 & -3
\end{vmatrix}
$$

$$
=(-3)
\begin{vmatrix}
1 & 1\\
1 & -3
\end{vmatrix}
-1
\begin{vmatrix}
1 & 1\\
1 & -3
\end{vmatrix}
+1
\begin{vmatrix}
1 & 1\\
1 & 1
\end{vmatrix}
$$

$$
=(-3)(-4)-1(-4)+1(0)
$$

$$
=12+4=16
$$

Minor \(M_{14}\)

$$
M_{14}=
\begin{vmatrix}
-3 & 1 & 1\\
1 & 1 & -3\\
1 & 1 & 1
\end{vmatrix}
$$

$$
=(-3)
\begin{vmatrix}
1 & -3\\
1 & 1
\end{vmatrix}
-1
\begin{vmatrix}
1 & -3\\
1 & 1
\end{vmatrix}
+1
\begin{vmatrix}
1 & 1\\
1 & 1
\end{vmatrix}
$$

$$
=(-3)(4)-1(4)+0
$$

$$
=-12-4=-16
$$

Substitusi:

$$
\det(A)=1(16)-(-3)(-16)+1(16)-1(-16)
$$

$$
=16-48+16+16
$$

$$
=0
$$

Jadi,

$$
\boxed{\det(A)=0}
$$

### Penyelesaian Soal Nomor B4 

$$
A=
\begin{bmatrix}
-7 & -5\\
1 & 4
\end{bmatrix}
$$

Determinan matriks:

$$
\det(A)=(-7)(4)-(-5)(1)
$$

$$
=-28+5=-23
$$

Rumus invers matriks:

$$
A^{-1}=\frac{1}{\det(A)}\operatorname{adj}(A)
$$

---

 1. Mencari adjoin matriks

Untuk matriks 2×2:

$$
A=
\begin{bmatrix}
a & b\\
c & d
\end{bmatrix}
$$

maka:

$$
\operatorname{adj}(A)=
\begin{bmatrix}
d & -b\\
-c & a
\end{bmatrix}
$$

Sehingga:

$$
\operatorname{adj}(A)=
\begin{bmatrix}
4 & 5\\
-1 & -7
\end{bmatrix}
$$

---

2. Mencari invers matriks

$$
A^{-1}=\frac{1}{-23}
\begin{bmatrix}
4 & 5\\
-1 & -7
\end{bmatrix}
$$

$$
A^{-1}=
\begin{bmatrix}
-\frac{4}{23} & -\frac{5}{23}\\
\frac{1}{23} & \frac{7}{23}
\end{bmatrix}
$$

Jadi,

$$
\boxed{
A^{-1}=
\begin{bmatrix}
-\frac{4}{23} & -\frac{5}{23}\\
\frac{1}{23} & \frac{7}{23}
\end{bmatrix}
}
$$

### Penyelesaian Soal Nomor B5 

$$
A=
\begin{bmatrix}
0 & 2 & -3\\
1 & -2 & -1\\
0 & 0 & 1
\end{bmatrix}
$$

Dari hasil sebelumnya diperoleh:

$$
\det(A)=-2
$$

Rumus invers matriks:

$$
A^{-1}=\frac{1}{\det(A)}\operatorname{adj}(A)
$$

---

1. Mencari matriks kofaktor

Kofaktor \(C_{11}\)

$$
C_{11}=(-1)^{1+1}
\begin{vmatrix}
-2 & -1\\
0 & 1
\end{vmatrix}
=-2
$$

Kofaktor \(C_{12}\)

$$
C_{12}=(-1)^{1+2}
\begin{vmatrix}
1 & -1\\
0 & 1
\end{vmatrix}
=-1
$$

Kofaktor \(C_{13}\)

$$
C_{13}=(-1)^{1+3}
\begin{vmatrix}
1 & -2\\
0 & 0
\end{vmatrix}
=0
$$

Kofaktor \(C_{21}\)

$$
C_{21}=(-1)^{2+1}
\begin{vmatrix}
2 & -3\\
0 & 1
\end{vmatrix}
=-2
$$

Kofaktor \(C_{22}\)

$$
C_{22}=(-1)^{2+2}
\begin{vmatrix}
0 & -3\\
0 & 1
\end{vmatrix}
=0
$$

Kofaktor \(C_{23}\)

$$
C_{23}=(-1)^{2+3}
\begin{vmatrix}
0 & 2\\
0 & 0
\end{vmatrix}
=0
$$

Kofaktor \(C_{31}\)

$$
C_{31}=(-1)^{3+1}
\begin{vmatrix}
2 & -3\\
-2 & -1
\end{vmatrix}
=-8
$$

Kofaktor \(C_{32}\)

$$
C_{32}=(-1)^{3+2}
\begin{vmatrix}
0 & -3\\
1 & -1
\end{vmatrix}
=-3
$$

Kofaktor \(C_{33}\)

$$
C_{33}=(-1)^{3+3}
\begin{vmatrix}
0 & 2\\
1 & -2
\end{vmatrix}
=-2
$$

Maka matriks kofaktor:

$$
C=
\begin{bmatrix}
-2 & -1 & 0\\
-2 & 0 & 0\\
-8 & -3 & -2
\end{bmatrix}
$$

---

2. Mencari adjoin

Transpose matriks kofaktor:

$$
\operatorname{adj}(A)=C^T=
\begin{bmatrix}
-2 & -2 & -8\\
-1 & 0 & -3\\
0 & 0 & -2
\end{bmatrix}
$$

---

3. Mencari invers matriks

$$
A^{-1}=\frac{1}{-2}
\begin{bmatrix}
-2 & -2 & -8\\
-1 & 0 & -3\\
0 & 0 & -2
\end{bmatrix}
$$

$$
A^{-1}=
\begin{bmatrix}
1 & 1 & 4\\
\frac{1}{2} & 0 & \frac{3}{2}\\
0 & 0 & 1
\end{bmatrix}
$$

Jadi,

$$
\boxed{
A^{-1}=
\begin{bmatrix}
1 & 1 & 4\\
\frac{1}{2} & 0 & \frac{3}{2}\\
0 & 0 & 1
\end{bmatrix}
}
$$

Penyelesaian Detail Nomor 6: Invers Matriks 4x4

$$
A=
\begin{bmatrix}
1 & -3 & 1 & 1\\
-3 & 1 & 1 & 1\\
1 & 1 & -3 & 1\\
1 & 1 & 1 & -3
\end{bmatrix}
$$

Dari hasil sebelumnya diperoleh:

$$
\det(A)=0
$$

Rumus invers matriks dengan adjoin:

$$
A^{-1}=\frac{1}{\det(A)}\operatorname{adj}(A)
$$

Substitusi:

$$
A^{-1}=\frac{1}{0}\operatorname{adj}(A)
$$

Karena pembagian dengan nol tidak terdefinisi, maka matriks \(A\) tidak memiliki invers.

$$
\boxed{A^{-1}\text{ tidak ada}}
$$

### Penyelesaian Soal Nomor B6

$$
A=
\begin{bmatrix}
1 & -3 & 1 & 1\\
-3 & 1 & 1 & 1\\
1 & 1 & -3 & 1\\
1 & 1 & 1 & -3
\end{bmatrix}
$$

Dari hasil perhitungan determinan sebelumnya diperoleh:

$$
\det(A)=0
$$

Rumus invers matriks:

$$
A^{-1}=\frac{1}{\det(A)}\operatorname{adj}(A)
$$

Substitusi:

$$
A^{-1}=\frac{1}{0}\operatorname{adj}(A)
$$

Karena pembagian dengan nol tidak terdefinisi, maka matriks \(A\) tidak memiliki invers.

$$
\boxed{A^{-1}\text{ tidak ada}}
$$