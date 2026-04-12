# Tugas Determinan Matriks 5x5

## Matriks

$$
A =
\begin{bmatrix}
1 & 0 & 0 & 2 & 0 \\
0 & 1 & 0 & 0 & 2 \\
2 & 0 & 1 & 0 & 0 \\
0 & 2 & 0 & 1 & 0 \\
0 & 0 & 2 & 0 & 1
\end{bmatrix}
$$

---

## Rumus Determinan

$$
\det(A)=a\det(A_{11})-b\det(A_{12})+c\det(A_{13})-d\det(A_{14})+e\det(A_{15})
$$

---

## Substitusi

$$
\det(A)=1[\cdots]-0[\cdots]+2[\cdots]-0[\cdots]+0[\cdots]
$$

---

## Penyederhanaan

$$
\det(A)=1(1)+2(16)
$$

$$
\det(A)=33
$$

---

## Adjoin (Konsep)

$$
\operatorname{adj}(A)_{ij}=(-1)^{i+j}M_{ji}
$$

---

## Contoh Perhitungan

$$
\operatorname{adj}(A)_{11}=
\begin{vmatrix}
1 & 0 & 2 & 0\\
0 & 1 & 0 & 2\\
0 & 0 & 1 & 0\\
2 & 0 & 0 & 1
\end{vmatrix}
=1
$$

$$
\operatorname{adj}(A)_{12}=
-\begin{vmatrix}
0 & 2 & 0 & 0\\
0 & 1 & 0 & 2\\
0 & 0 & 1 & 0\\
2 & 0 & 0 & 1
\end{vmatrix}
=0
$$

$$
\operatorname{adj}(A)_{13}=
\begin{vmatrix}
0 & 2 & 0 & 0\\
1 & 0 & 2 & 0\\
0 & 0 & 1 & 0\\
2 & 0 & 0 & 1
\end{vmatrix}
=16
$$

---

## Hasil Adjoin

$$
\operatorname{adj}(A)=
\begin{bmatrix}
1 & 0 & 16 & 0 & 0 \\
0 & 1 & 0 & 16 & 0 \\
0 & 0 & 1 & 0 & 16 \\
16 & 0 & 0 & 1 & 0 \\
0 & 16 & 0 & 0 & 1
\end{bmatrix}
$$

---

## Invers Matriks

$$
A^{-1}=\frac{1}{33}\operatorname{adj}(A)
$$

---

## Hasil Akhir Invers

$$
A^{-1}=
\begin{bmatrix}
\frac{1}{33} & 0 & \frac{16}{33} & 0 & 0 \\
0 & \frac{1}{33} & 0 & \frac{16}{33} & 0 \\
0 & 0 & \frac{1}{33} & 0 & \frac{16}{33} \\
\frac{16}{33} & 0 & 0 & \frac{1}{33} & 0 \\
0 & \frac{16}{33} & 0 & 0 & \frac{1}{33}
\end{bmatrix}
$$