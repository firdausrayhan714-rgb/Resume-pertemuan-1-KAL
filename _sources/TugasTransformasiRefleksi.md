# Analisis Transformasi Geometri: Refleksi Sumbu Y

Transformasi geometri menggunakan matriks adalah cara efisien untuk menghitung perubahan posisi titik atau objek dalam koordinat Kartesius. Berikut adalah penjelasan mendalam mengenai konsep refleksi menggunakan operator matriks $2 \times 2$.

---

### 1. Landasan Teoretis

**Representasi Titik**
Setiap titik dalam ruang 2D direpresentasikan sebagai vektor kolom:
$$
P = \begin{bmatrix} x \\ y \end{bmatrix}
$$

**Matriks Operator Refleksi Sumbu Y**
Refleksi terhadap sumbu Y adalah transformasi yang memetakan titik $(x, y)$ ke $(-x, y)$. Matriks yang bertanggung jawab atas operasi ini adalah:
$$
M_y = \begin{bmatrix} -1 & 0 \\ 0 & 1 \end{bmatrix}
$$
*   Elemen $-1$ pada baris pertama kolom pertama berfungsi untuk membalikkan tanda nilai $x$.
*   Elemen $1$ pada baris kedua kolom kedua berfungsi untuk mempertahankan nilai $y$.

---

### 2. Contoh Perhitungan Detil

Misalkan kita memiliki titik awal **$A(9, 4)$**. Kita akan mencari koordinat bayangan **$A'$** setelah dicerminkan terhadap sumbu Y.

**Persamaan Matriks:**
$$
\begin{bmatrix} x' \\ y' \end{bmatrix} = \begin{bmatrix} -1 & 0 \\ 0 & 1 \end{bmatrix} \begin{bmatrix} 9 \\ 4 \end{bmatrix}
$$

**Langkah Penyelesaian (Perkalian Baris x Kolom):**
1.  **Mencari $x'$ (Baris 1):**
    Kalikan elemen baris pertama matriks dengan elemen vektor kolom:
    $$x' = (-1 \times 9) + (0 \times 4)$$
    $$x' = -9 + 0 = \mathbf{-9}$$

2.  **Mencari $y'$ (Baris 2):**
    Kalikan elemen baris kedua matriks dengan elemen vektor kolom:
    $$y' = (0 \times 9) + (1 \times 4)$$
    $$y' = 0 + 4 = \mathbf{4}$$

**Hasil Koordinat:**
Bayangan dari titik $A(9, 4)$ adalah **$A'(-9, 4)$**.

---

### 3. Implementasi pada Objek Kompleks
Jika kita memiliki objek (seperti pada kode program), transformasi ini diterapkan pada setiap titik pembentuk objek tersebut secara simultan. Jika objek memiliki titik-titik $P_1, P_2, \dots, P_n$, maka:
$$
[P'_1, P'_2, \dots, P'_n] = M_y \times [P_1, P_2, \dots, P_n]
$$
Hal inilah yang menyebabkan objek di sisi kanan sumbu Y akan muncul secara simetris di sisi kiri dengan bentuk yang sama namun arah yang terbalik.

---

### 4. Kesimpulan
Berdasarkan analisis di atas, dapat disimpulkan bahwa:
1.  **Refleksi Sumbu Y** secara matematis hanya mengubah tanda (posisi horizontal) pada sumbu X, sementara posisi vertikal (sumbu Y) tetap konsisten.
2.  **Penggunaan Matriks $2 \times 2$** memberikan efisiensi komputasi, di mana satu operator matriks dapat diterapkan ke ribuan titik sekaligus menggunakan library seperti *NumPy*.
3.  **Visualisasi:** Dalam simulasi komputer, refleksi menciptakan efek "cermin" di mana pergerakan objek menjauhi sumbu Y di sisi positif akan diikuti secara otomatis oleh bayangannya yang menjauhi sumbu Y di sisi negatif.


implementasi program di colab:https://colab.research.google.com/drive/1XP12oG-1Xb1jq9peWpehYrkq6__OP6oe?usp=sharing