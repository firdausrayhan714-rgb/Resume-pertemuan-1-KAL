# 📊 Implementasi Singular Value Decomposition (SVD) pada Kompresi Citra

## Hasil Output Program

Pada program:

```python
U, S, Vt = np.linalg.svd(gambar_asli, full_matrices=False)
```

diperoleh output:

```text
Ukuran Matriks U  : (200, 200)
Ukuran Vektor S   : (200,)
Ukuran Matriks Vt : (200, 252)
```

Artinya sistem berhasil memecah gambar menjadi tiga komponen utama menggunakan metode Singular Value Decomposition (SVD).

Tujuan utama SVD pada citra adalah:

- memisahkan pola penting gambar,
- mengurangi ukuran data,
- mempertahankan kualitas visual gambar.

---

## 1. Menentukan Matriks Awal Gambar A

Saat gambar dibaca:

```python
gambar = Image.open(nama_file)
```

gambar masih berupa citra RGB.

Setelah itu dilakukan konversi grayscale:

```python
gambar_gray = np.mean(gambar[:, :, :3], axis=2)
```

### Penjelasan

Proses grayscale dilakukan agar:

- gambar hanya memiliki 1 kanal warna,
- perhitungan matematika menjadi lebih sederhana,
- proses SVD menjadi lebih cepat.

Pada grayscale:

```text
0   = hitam
255 = putih
```

Setelah proses ini, gambar berubah menjadi matriks numerik.

Karena hasil ukuran gambar dari program adalah:

```text
200 × 252
```

maka matriks gambar:

$$
A_{200 \times 252}
$$

Artinya:

- 200 baris piksel
- 252 kolom piksel

Jumlah total piksel:

$$
200 \times 252 = 50400
$$

Jadi gambar direpresentasikan sebagai:

```text
50.400 nilai intensitas piksel grayscale
```

Contoh sederhana matriks gambar:

```text
A =
[120 130 140]
[100 110 125]
[ 90 100 105]
```

Setiap angka menunjukkan tingkat terang suatu piksel.

---

## 2. Tujuan Dilakukan SVD

Metode SVD memecah matriks gambar:

$$
A = U\Sigma V^T
$$

menjadi tiga bagian utama.

### Penjelasan Komponen

| Matriks | Fungsi |
|---|---|
| U | menyimpan pola vertikal gambar |
| Σ | menyimpan energi/informasi penting |
| Vᵀ | menyimpan pola horizontal gambar |

Secara sederhana:

- U = arah fitur gambar
- Σ = tingkat kepentingan fitur
- Vᵀ = kombinasi pola pembentuk gambar

Dengan memecah gambar menjadi bagian-bagian ini, sistem dapat mengetahui:

- fitur penting,
- fitur kurang penting,
- bagian yang bisa dibuang saat kompresi.

---

## 3. Mencari Matriks AAᵀ

Langkah pertama dalam proses SVD adalah menghitung:

$$
AA^T
$$

Pada program:

```python
AAT = gambar_asli @ gambar_asli.T
```

### Penjelasan

Transpose `(T)` berarti:

- baris menjadi kolom,
- kolom menjadi baris.

Karena ukuran gambar:

$$
A = (200 \times 252)
$$

maka:

$$
(200 \times 252)(252 \times 200) = 200 \times 200
$$

hasil:

```text
AAᵀ = (200 × 200)
```

### Mengapa Harus Menghitung AAᵀ?

Karena:

- eigenvector dari AAᵀ digunakan membentuk matriks U,
- eigenvalue dari AAᵀ digunakan mencari singular value.

AAᵀ dipakai untuk mengetahui:

- pola dominan,
- arah variasi terbesar,
- struktur utama gambar.

---

## 4. Mencari Eigenvalue dan Eigenvector

Setelah mendapatkan AAᵀ, langkah berikutnya adalah mencari:

- eigenvalue
- eigenvector

Secara matematis:

$$
(AA^T - \lambda I)x = 0
$$

dengan:

- $\lambda$ = eigenvalue
- $x$ = eigenvector
- $I$ = matriks identitas

Pada Python:

```python
eigenvalue, eigenvector = np.linalg.eig(AAT)
```

### Penjelasan Eigenvalue

Eigenvalue menunjukkan:

- seberapa besar pengaruh suatu fitur pada gambar.

Nilai besar:

- fitur sangat penting.

Nilai kecil:

- fitur kurang penting/noise.

### Penjelasan Eigenvector

Eigenvector menunjukkan:

- arah pola utama pada gambar.

Misalnya:

- pola wajah,
- pencahayaan,
- kontur objek,
- bentuk struktur gambar.

---

## 5. Mendapatkan Singular Value

Singular value diperoleh dari akar eigenvalue:

$$
\sigma_i = \sqrt{\lambda_i}
$$

Pada program sebenarnya proses ini dihitung otomatis oleh:

```python
np.linalg.svd()
```

Makanya muncul:

```text
Ukuran Vektor S : (200,)
```

Artinya:

```text
Terdapat 200 singular value
```

### Penjelasan Singular Value

Singular value adalah:

- ukuran kekuatan informasi suatu komponen gambar.

Nilai singular terbesar:

- menyimpan struktur utama gambar.

Nilai singular kecil:

- biasanya hanya detail kecil/noise.

Karena itu:

- beberapa singular value pertama saja sudah cukup membentuk gambar.

---

## 6. Membentuk Matriks U

Eigenvector dari:

$$
AA^T
$$

dikumpulkan menjadi:

$$
U = [u_1 \ u_2 \ u_3 \ ... \ u_{200}]
$$

Ukurannya:

```text
U = (200 × 200)
```

### Penjelasan Matriks U

Matriks U berisi:

- pola vertikal utama gambar.

Setiap kolom U:

- mewakili satu arah fitur penting.

Karena jumlah piksel vertikal = 200,
maka jumlah vektor pada U juga 200.

---

## 7. Mencari Matriks AᵀA

Langkah berikutnya:

```python
ATA = gambar_asli.T @ gambar_asli
```

Secara matematis:

$$
A^TA
$$

### Penjelasan

AᵀA digunakan untuk:

- mencari pola horizontal gambar.

Karena:

$$
A^T = (252 \times 200)
$$

$$
A = (200 \times 252)
$$

maka:

$$
(252 \times 200)(200 \times 252) = 252 \times 252
$$

hasil:

```text
AᵀA = (252 × 252)
```

---

## 8. Membentuk Matriks Vᵀ

Eigenvector dari:

$$
A^TA
$$

membentuk matriks:

$$
V
$$

kemudian ditranspose menjadi:

$$
V^T
$$

Sehingga:

```text
Vᵀ = (200 × 252)
```

### Penjelasan Matriks Vᵀ

Vᵀ menyimpan:

- pola horizontal gambar.

Jika U membaca pola vertikal,
maka Vᵀ membaca:

- pola mendatar,
- struktur horizontal,
- kombinasi fitur antar kolom piksel.

Karena menggunakan:

```python
full_matrices=False
```

maka NumPy menggunakan thin SVD sehingga ukuran Vᵀ menjadi:

```text
(200 × 252)
```

bukan:

```text
(252 × 252)
```

Tujuannya agar:

- komputasi lebih cepat,
- memori lebih hemat,
- hanya komponen penting yang disimpan.

---

## 9. Membentuk Matriks Sigma Σ

Vector singular:

$$
S = [\sigma_1, \sigma_2, \sigma_3, ..., \sigma_{200}]
$$

diubah menjadi matriks diagonal:

```python
Sigma = np.diag(S)
```

Menjadi:

$$
\Sigma =
\begin{bmatrix}
\sigma_1 & 0 & 0 \\
0 & \sigma_2 & 0 \\
0 & 0 & \sigma_3
\end{bmatrix}
$$

### Penjelasan Sigma

Sigma menunjukkan:

- tingkat kepentingan tiap fitur gambar.

Semakin besar nilai sigma:

- semakin penting fitur tersebut.

Karena hanya diagonal yang berisi angka:

- tiap fitur berdiri sendiri,
- tidak saling bercampur.

---

## 10. Rekonstruksi Gambar

Pada program:

```python
gambar_rekonstruksi = U_k @ S_k @ Vt_k
```

Secara matematis:

$$
A_k = U_k\Sigma_kV_k^T
$$

### Penjelasan

Rekonstruksi berarti:

- membangun kembali gambar dari hasil SVD.

Tetapi:

- tidak semua komponen dipakai,
- hanya komponen paling penting saja.

Karena itu:

- ukuran data menjadi lebih kecil,
- gambar masih terlihat mirip.

---

## 11. Penjelasan Nilai k

Pada program:

```python
pilihan_k = [2, 10, 30, 60, 90]
```

### Penjelasan

k menunjukkan:

- jumlah singular value yang dipakai.

| k | Makna |
|---|---|
| 2 | hanya fitur utama |
| 10 | detail mulai muncul |
| 30 | gambar mulai jelas |
| 60 | hampir menyerupai asli |
| 90 | kualitas semakin mendekati gambar asli |

Semakin besar k:

- kualitas semakin baik,
- ukuran penyimpanan semakin besar.

---

## 12. Mengapa Gambar Tetap Mirip Setelah Dikompresi?

Karena singular value terbesar menyimpan sebagian besar informasi gambar.

Pada grafik:

```python
plt.plot(S)
```

biasanya:

- nilai awal sangat besar,
- lalu turun drastis.

Artinya:

- sebagian besar informasi penting hanya berada pada beberapa komponen awal.

Komponen akhir:

- hanya detail kecil,
- bahkan sering berupa noise.

---

## 13. Alur Lengkap Proses SVD pada Program

## STEP 1

Baca gambar grayscale

$$
A (200 \times 252)
$$

↓

### STEP 2

Hitung:

$$
AA^T
$$

untuk mencari pola vertikal.

↓

### STEP 3

Cari:

- eigenvalue
- eigenvector

↓

### STEP 4

Bentuk:

```text
U (200 × 200)
```

↓

### STEP 5

Hitung:

$$
A^TA
$$

untuk mencari pola horizontal.

↓

### STEP 6

Cari eigenvector

↓

### STEP 7

Bentuk:

```text
Vᵀ (200 × 252)
```

↓

### STEP 8

Hitung singular value:

$$
\sigma_i = \sqrt{\lambda_i}
$$

↓

### STEP 9

Bentuk:

```text
Σ (200 × 200)
```

↓

### STEP 10

Rekonstruksi:

$$
A = U\Sigma V^T
$$

untuk menghasilkan kembali gambar hasil kompresi.