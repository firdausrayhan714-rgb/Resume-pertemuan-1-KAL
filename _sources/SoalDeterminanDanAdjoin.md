# Soal Determinan Matriks Dan Adjoin

### A. Hitunglah determinan matrik berikut dengan menggunakan rumus expansi baris

$$\sum_{k=1}^{n} (-1)^{i+k} a_{ik} M_{ik}$$

dengan ($M_{ij}$) adalah minior dari matrik A dan
$$M_{ij} = \det A_{ij}$$
($A_{ij}$)adalah submatrik dengan menghapus baris i dan kolom kolom j dari matrix (A_{mxn}) dengan ($1 \le i, j \le n$)

1. A = \begin{bmatrix} -7 & -5 \\ 1 & 4 \end{bmatrix}
2. A = \begin{bmatrix} 0 & 2 & -3 \\ 1 & -2 & -1 \\ 0 & 0 & 1 \end{bmatrix}
3. A = \begin{bmatrix} 1 & -3 & 1 & 1 \\ -3 & 1 & 1 & 1 \\ 1 & 1 & -3 & 1 \\ 1 & 1 & 1 & -3 \end{bmatrix}.


### B. Gunakan rumus matriks adjoin untuk menghitung invers dari matriks berikut dengan rumus

$$(\operatorname{adj} A)_{ij} = (-1)^{i+j} M_{ji}$$
dan
$$A^{-1} = \frac{1}{\det A} \operatorname{adj} A.$$

4. A = \begin{bmatrix} -7 & -5 \\ 1 & 4 \end{bmatrix}
5. A = \begin{bmatrix} 0 & 2 & -3 \\ 1 & -2 & -1 \\ 0 & 0 & 1 \end{bmatrix}
6. A = \begin{bmatrix} 1 & -3 & 1 & 1 \\ -3 & 1 & 1 & 1 \\ 1 & 1 & -3 & 1 \\ 1 & 1 & 1 & -3 \end{bmatrix}.


### Jawaban
### Penyelesaian Soal Nomor A1

Diketahui matriks:
$$A = \begin{bmatrix} -7 & -5 \\ 1 & 4 \end{bmatrix}$$

**Langkah-langkah Penyelesaian (Ekspansi Baris Pertama):**

1. Gunakan rumus ekspansi kofaktor untuk baris $i=1$:
   $$\det(A) = \sum_{k=1}^{2} (-1)^{1+k} a_{1k} M_{1k}$$

2. Jabarkan rumusnya:
   $$\det(A) = a_{11} (-1)^{1+1} M_{11} + a_{12} (-1)^{1+2} M_{12}$$

3. Tentukan nilai Minor ($M_{11}$ dan $M_{12}$):
   * $M_{11} = \det(4) = 4$
   * $M_{12} = \det(1) = 1$

4. Masukkan angka ke dalam rumus:
   $$\det(A) = (-7)(1)(4) + (-5)(-1)(1)$$
   $$\det(A) = -28 + 5$$

5. **Hasil Akhir:**
   $$\det(A) = -23$$

### Penyelesaian Soal Nomor A2

Diketahui matriks:
$$A = \begin{bmatrix} 0 & 2 & -3 \\ 1 & -2 & -1 \\ 0 & 0 & 1 \end{bmatrix}$$

**Langkah-langkah Penyelesaian (Ekspansi Baris Ketiga):**

1. Pilih baris ke-3 ($i=3$) untuk mempermudah perhitungan karena terdapat elemen bernilai 0:
   $$\det(A) = a_{31}C_{31} + a_{32}C_{32} + a_{33}C_{33}$$

2. Jabarkan berdasarkan elemen baris ke-3:
   $$\det(A) = 0 \cdot (-1)^{3+1} M_{31} + 0 \cdot (-1)^{3+2} M_{32} + 1 \cdot (-1)^{3+3} M_{33}$$

3. Karena dua elemen pertama adalah 0, kita cukup menghitung bagian terakhir:
   $$\det(A) = 0 + 0 + 1 \cdot (1) \cdot M_{33}$$

4. Tentukan nilai Minor $M_{33}$ (determinan submatriks dengan menghapus baris 3 dan kolom 3):
   $$M_{33} = \begin{vmatrix} 0 & 2 \\ 1 & -2 \end{vmatrix}$$
   $$M_{33} = (0 \cdot -2) - (2 \cdot 1) = 0 - 2 = -2$$

5. **Hasil Akhir:**
   $$\det(A) = 1 \cdot (-2)$$
   $$\det(A) = -2$$

### Penyelesaian Soal Nomor A3

Diketahui matriks:
$$A = \begin{bmatrix} 1 & -3 & 1 & 1 \\ -3 & 1 & 1 & 1 \\ 1 & 1 & -3 & 1 \\ 1 & 1 & 1 & -3 \end{bmatrix}$$

**Langkah-langkah Penyelesaian (Ekspansi Baris Pertama):**

1. Gunakan rumus ekspansi untuk baris $i=1$:
   $$\det(A) = a_{11}C_{11} + a_{12}C_{12} + a_{13}C_{13} + a_{14}C_{14}$$

2. Jabarkan kofaktornya:
   $$\det(A) = 1 \begin{vmatrix} 1 & 1 & 1 \\ 1 & -3 & 1 \\ 1 & 1 & -3 \end{vmatrix} - (-3) \begin{vmatrix} -3 & 1 & 1 \\ 1 & -3 & 1 \\ 1 & 1 & -3 \end{vmatrix} + 1 \begin{vmatrix} -3 & 1 & 1 \\ 1 & 1 & 1 \\ 1 & 1 & -3 \end{vmatrix} - 1 \begin{vmatrix} -3 & 1 & 1 \\ 1 & -3 & 1 \\ 1 & 1 & 1 \end{vmatrix}$$

3. Hitung masing-masing determinan $3 \times 3$:
   * $\det(M_{11}) = 1(9-1) - 1(-3-1) + 1(1+3) = 8 + 4 + 4 = 16$
   * $\det(M_{12}) = -3(9-1) - 1(-3-1) + 1(1+3) = -24 + 4 + 4 = -16$
   * $\det(M_{13}) = -3(-3-1) - 1(-3-1) + 1(1-1) = 12 + 4 + 0 = 16$
   * $\det(M_{14}) = -3(1+3) - 1(1+3) + 1(1+3) = -12 - 4 + 4 = -12$

4. Masukkan kembali ke rumus utama:
   $$\det(A) = 1(16) + 3(-16) + 1(16) - 1(-12)$$
   $$\det(A) = 16 - 48 + 16 + 12$$

5. **Hasil Akhir:**
   $$\det(A) = -4$$

### Penyelesaian Soal Nomor B4 

Diketahui matriks:
$$A = \begin{bmatrix} -7 & -5 \\ 1 & 4 \end{bmatrix}$$

1. Hitung Determinan
$$\det(A) = (-7)(4) - (-5)(1) = -28 + 5 = -23$$

2. Tentukan Matriks Adjoin
Untuk matriks $2 \times 2$, adjoin diperoleh dengan menukar elemen diagonal utama dan mengubah tanda elemen diagonal sekunder:
$$\text{adj } A = \begin{bmatrix} 4 & 5 \\ -1 & -7 \end{bmatrix}$$

3. Hitung Invers
Menggunakan rumus $A^{-1} = \frac{1}{\det A} \text{adj } A$:
$$A^{-1} = \frac{1}{-23} \begin{bmatrix} 4 & 5 \\ -1 & -7 \end{bmatrix}$$
$$A^{-1} = \begin{bmatrix} -\frac{4}{23} & -\frac{5}{23} \\ \frac{1}{23} & \frac{7}{23} \end{bmatrix}$$

### Penyelesaian Soal Nomor B5 

Diketahui matriks:
$$A = \begin{bmatrix} 0 & 2 & -3 \\ 1 & -2 & -1 \\ 0 & 0 & 1 \end{bmatrix}$$

1. Hitung Determinan
(Dari hasil sebelumnya): $\det(A) = -2$

**Langkah 2: Hitung Matriks Kofaktor ($C_{ij}$)**
* $C_{11} = + \begin{vmatrix} -2 & -1 \\ 0 & 1 \end{vmatrix} = -2$
* $C_{12} = - \begin{vmatrix} 1 & -1 \\ 0 & 1 \end{vmatrix} = -1$
* $C_{13} = + \begin{vmatrix} 1 & -2 \\ 0 & 0 \end{vmatrix} = 0$
* $C_{21} = - \begin{vmatrix} 2 & -3 \\ 0 & 1 \end{vmatrix} = -2$
* $C_{22} = + \begin{vmatrix} 0 & -3 \\ 0 & 1 \end{vmatrix} = 0$
* $C_{23} = - \begin{vmatrix} 0 & 2 \\ 0 & 0 \end{vmatrix} = 0$
* $C_{31} = + \begin{vmatrix} 2 & -3 \\ -2 & -1 \end{vmatrix} = -2 - 6 = -8$
* $C_{32} = - \begin{vmatrix} 0 & -3 \\ 1 & -1 \end{vmatrix} = -(0 + 3) = -3$
* $C_{33} = + \begin{vmatrix} 0 & 2 \\ 1 & -2 \end{vmatrix} = -2$

3. Tentukan Adjoin (Transpose dari Kofaktor)
$$\text{adj } A = C^T = \begin{bmatrix} -2 & -2 & -8 \\ -1 & 0 & -3 \\ 0 & 0 & -2 \end{bmatrix}$$

**Langkah 4: Hitung Invers**
$$A^{-1} = \frac{1}{-2} \begin{bmatrix} -2 & -2 & -8 \\ -1 & 0 & -3 \\ 0 & 0 & -2 \end{bmatrix} = \begin{bmatrix} 1 & 1 & 4 \\ \frac{1}{2} & 0 & \frac{3}{2} \\ 0 & 0 & 1 \end{bmatrix}$$

### Penyelesaian Soal Nomor B6 

Diketahui matriks:
$$A = \begin{bmatrix} 1 & -3 & 1 & 1 \\ -3 & 1 & 1 & 1 \\ 1 & 1 & -3 & 1 \\ 1 & 1 & 1 & -3 \end{bmatrix}$$

1. Determinan
Berdasarkan perhitungan sebelumnya:
$$\det(A) = -128$$

2. Menghitung Matriks Kofaktor ($C_{ij}$)
Kita harus menghitung 16 kofaktor. Karena matriks ini memiliki pola simetris, kita bisa menghemat waktu.
* $C_{11} = (-1)^{1+1} \det(M_{11}) = 16$
* $C_{12} = (-1)^{1+2} \det(M_{12}) = -(-16) = 16$
* $C_{13} = (-1)^{1+3} \det(M_{13}) = 16$
* $C_{14} = (-1)^{1+4} \det(M_{14}) = -(-16) = 16$

Setelah menghitung semua elemen kofaktor:
$$C = \begin{bmatrix} 16 & 16 & 16 & 16 \\ 16 & 16 & -16 & -16 \\ 16 & -16 & 16 & -16 \\ 16 & -16 & -16 & 16 \end{bmatrix}$$

3. Matriks Adjoin ($\text{adj } A = C^T$)
Karena kofaktor ini simetris, maka $\text{adj } A$ sama dengan matriks kofaktor itu sendiri:
$$\text{adj } A = \begin{bmatrix} 16 & 16 & 16 & 16 \\ 16 & 16 & -16 & -16 \\ 16 & -16 & 16 & -16 \\ 16 & -16 & -16 & 16 \end{bmatrix}$$

4. Hasil Akhir Invers ($A^{-1} = \frac{1}{\det A} \text{adj } A$)
$$A^{-1} = \frac{1}{-128} \begin{bmatrix} 16 & 16 & 16 & 16 \\ 16 & 16 & -16 & -16 \\ 16 & -16 & 16 & -16 \\ 16 & -16 & -16 & 16 \end{bmatrix}$$

Sederhanakan dengan membagi setiap elemen dengan $-128$:
$$A^{-1} = \begin{bmatrix} -1/8 & -1/8 & -1/8 & -1/8 \\ -1/8 & -1/8 & 1/8 & 1/8 \\ -1/8 & 1/8 & -1/8 & 1/8 \\ -1/8 & 1/8 & 1/8 & -1/8 \end{bmatrix}$$