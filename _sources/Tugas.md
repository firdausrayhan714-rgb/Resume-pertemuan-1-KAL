# Tugas Determinan Matriks

Matriks 5x5

Determinan didefinisikan sebagai berikut


$$
\det(A) = \sum_{j=1}^{5} (-1)^{1+j} \, a_{1j} \, \det(A_{1j})
$$

**membuat matriks 5x5**
$$
A =
\begin{bmatrix}
a & b & c & d & e \\
f & g & h & i & j \\
k & l & m & n & o \\
p & q & r & s & t \\
u & v & w & x & y
\end{bmatrix}
$$

### Operasi Determinan

$$
\det(A) =
(-1)^{1+1} a \det(A_{11})
+ (-1)^{1+2} b \det(A_{12})
+ (-1)^{1+3} c \det(A_{13})
+ (-1)^{1+4} d \det(A_{14})
+ (-1)^{1+5} e \det(A_{15})
$$

$$
\det(A) =
a \det(A_{11})
- b \det(A_{12})
+ c \det(A_{13})
- d \det(A_{14})
+ e \det(A_{15})
$$

$$
\det(A) =
a \cdot
\begin{vmatrix}
g & h & i & j \\
l & m & n & o \\
q & r & s & t \\
v & w & x & y
\end{vmatrix}
-
b \cdot
\begin{vmatrix}
f & h & i & j \\
k & m & n & o \\
p & r & s & t \\
u & w & x & y
\end{vmatrix}
+
c \cdot
\begin{vmatrix}
f & g & i & j \\
k & l & n & o \\
p & q & s & t \\
u & v & x & y
\end{vmatrix}
-
d \cdot
\begin{vmatrix}
f & g & h & j \\
k & l & m & o \\
p & q & r & t \\
u & v & w & y
\end{vmatrix}
+
e \cdot
\begin{vmatrix}
f & g & h & i \\
k & l & m & n \\
p & q & r & s \\
u & v & w & x
\end{vmatrix}
$$
### Bagian a det(A11)

$$
a \cdot \det(A_{11}) =
a \cdot
\begin{vmatrix}
g & h & i & j \\
l & m & n & o \\
q & r & s & t \\
v & w & x & y
\end{vmatrix}
$$

---

#### Ekspansi ke 3x3

$$
= a \left[
g \cdot
\begin{vmatrix}
m & n & o \\
r & s & t \\
w & x & y
\end{vmatrix}
-
h \cdot
\begin{vmatrix}
l & n & o \\
q & s & t \\
v & x & y
\end{vmatrix}
+
i \cdot
\begin{vmatrix}
l & m & o \\
q & r & t \\
v & w & y
\end{vmatrix}
-
j \cdot
\begin{vmatrix}
l & m & n \\
q & r & s \\
v & w & x
\end{vmatrix}
\right]
$$

---

#### Ekspansi ke 2x2

$$
= a \left[
g \left(
m \cdot
\begin{vmatrix} s & t \\ x & y \end{vmatrix}
-
n \cdot
\begin{vmatrix} r & t \\ w & y \end{vmatrix}
+
o \cdot
\begin{vmatrix} r & s \\ w & x \end{vmatrix}
\right)
-
h \left(
l \cdot
\begin{vmatrix} s & t \\ x & y \end{vmatrix}
-
n \cdot
\begin{vmatrix} q & t \\ v & y \end{vmatrix}
+
o \cdot
\begin{vmatrix} q & s \\ v & x \end{vmatrix}
\right)
+
i \left(
l \cdot
\begin{vmatrix} r & t \\ w & y \end{vmatrix}
-
m \cdot
\begin{vmatrix} q & t \\ v & y \end{vmatrix}
+
o \cdot
\begin{vmatrix} q & r \\ v & w \end{vmatrix}
\right)
-
j \left(
l \cdot
\begin{vmatrix} r & s \\ w & x \end{vmatrix}
-
m \cdot
\begin{vmatrix} q & s \\ v & x \end{vmatrix}
+
n \cdot
\begin{vmatrix} q & r \\ v & w \end{vmatrix}
\right)
\right]
$$

---

#### Hasil Determinan 2x2

$$
= a \left(
g \left(
m(sy - tx)
- n(ry - tw)
+ o(rx - sw)
\right)
-
h \left(
l(sy - tx)
- n(qy - tv)
+ o(qx - sv)
\right)
+
i \left(
l(ry - tw)
- m(qy - tv)
+ o(qw - rv)
\right)
-
j \left(
l(rx - sw)
- m(qx - sv)
+ n(qw - rv)
\right)
\right)
$$

### Bagian -b det(A12)

$$
- b \det(A_{12}) =
- b \begin{vmatrix}
f & h & i & j \\
k & m & n & o \\
p & r & s & t \\
u & w & x & y
\end{vmatrix}
$$

### Ekspansi kofaktor (3x3)

$$
= - b \left[
f \begin{vmatrix}
m & n & o \\
r & s & t \\
w & x & y
\end{vmatrix}
- h \begin{vmatrix}
k & n & o \\
p & s & t \\
u & x & y
\end{vmatrix}
+ i \begin{vmatrix}
k & m & o \\
p & r & t \\
u & w & y
\end{vmatrix}
- j \begin{vmatrix}
k & m & n \\
p & r & s \\
u & w & x
\end{vmatrix}
\right]
$$

### Ekspansi kofaktor (2x2)

$$
= - b \left[
f \left(
m \begin{vmatrix} s & t \\ x & y \end{vmatrix}
- n \begin{vmatrix} r & t \\ w & y \end{vmatrix}
+ o \begin{vmatrix} r & s \\ w & x \end{vmatrix}
\right)
- h \left(
k \begin{vmatrix} s & t \\ x & y \end{vmatrix}
- n \begin{vmatrix} p & t \\ u & y \end{vmatrix}
+ o \begin{vmatrix} p & s \\ u & x \end{vmatrix}
\right)
+ i \left(
k \begin{vmatrix} r & t \\ w & y \end{vmatrix}
- m \begin{vmatrix} p & t \\ u & y \end{vmatrix}
+ o \begin{vmatrix} p & r \\ u & w \end{vmatrix}
\right)
- j \left(
k \begin{vmatrix} r & s \\ w & x \end{vmatrix}
- m \begin{vmatrix} p & s \\ u & x \end{vmatrix}
+ n \begin{vmatrix} p & r \\ u & w \end{vmatrix}
\right)
\right]
$$

### Determinan 2x2

$$
= - b \Big(
f \big(
m(sy - tx)
- n(ry - tw)
+ o(rx - sw)
\big)
- h \big(
k(sy - tx)
- n(py - tu)
+ o(px - su)
\big)
+ i \big(
k(ry - tw)
- m(py - tu)
+ o(pw - ru)
\big)
- j \big(
k(rx - sw)
- m(px - su)
+ n(pw - ru)
\big)
\Big)
$$

### Bagian c det(A13)

$$
c \det(A_{13}) =
c \begin{vmatrix}
f & g & i & j \\
k & l & n & o \\
p & q & s & t \\
u & v & x & y
\end{vmatrix}
$$

### Ekspansi kofaktor (3x3)

$$
= c \left[
f \begin{vmatrix}
l & n & o \\
q & s & t \\
v & x & y
\end{vmatrix}
- g \begin{vmatrix}
k & n & o \\
p & s & t \\
u & x & y
\end{vmatrix}
+ i \begin{vmatrix}
k & l & o \\
p & q & t \\
u & v & y
\end{vmatrix}
- j \begin{vmatrix}
k & l & n \\
p & q & s \\
u & v & x
\end{vmatrix}
\right]
$$

### Ekspansi kofaktor (2x2)

$$
= c \left[
f \left(
l \begin{vmatrix} s & t \\ x & y \end{vmatrix}
- n \begin{vmatrix} q & t \\ v & y \end{vmatrix}
+ o \begin{vmatrix} q & s \\ v & x \end{vmatrix}
\right)
- g \left(
k \begin{vmatrix} s & t \\ x & y \end{vmatrix}
- n \begin{vmatrix} p & t \\ u & y \end{vmatrix}
+ o \begin{vmatrix} p & s \\ u & x \end{vmatrix}
\right)
+ i \left(
k \begin{vmatrix} q & t \\ v & y \end{vmatrix}
- l \begin{vmatrix} p & t \\ u & y \end{vmatrix}
+ o \begin{vmatrix} p & q \\ u & v \end{vmatrix}
\right)
- j \left(
k \begin{vmatrix} q & s \\ v & x \end{vmatrix}
- l \begin{vmatrix} p & s \\ u & x \end{vmatrix}
+ n \begin{vmatrix} p & q \\ u & v \end{vmatrix}
\right)
\right]
$$

### Determinan 2x2

$$
= c \Big(
f \big(
l(sy - tx)
- n(qy - tv)
+ o(qx - sv)
\big)
- g \big(
k(sy - tx)
- n(py - tu)
+ o(px - su)
\big)
+ i \big(
k(qy - tv)
- l(py - tu)
+ o(pv - qu)
\big)
- j \big(
k(qx - sv)
- l(px - su)
+ n(pv - qu)
\big)
\Big)
$$

$$
- d \, \det(A_{14}) =
- d \begin{vmatrix}
f & g & h & j \\
k & l & m & o \\
p & q & r & t \\
u & v & w & y
\end{vmatrix}
=
- d \Bigg[
f \begin{vmatrix}
l & m & o \\
q & r & t \\
v & w & y
\end{vmatrix}
- g \begin{vmatrix}
k & m & o \\
p & r & t \\
u & w & y
\end{vmatrix}
+ h \begin{vmatrix}
k & l & o \\
p & q & t \\
u & v & y
\end{vmatrix}
- j \begin{vmatrix}
k & l & m \\
p & q & r \\
u & v & w
\end{vmatrix}
\Bigg]
$$
$$
= -d \Bigg[
f \Big(
l(r y - t w)
- m(q y - t v)
+ o(q w - r v)
\Big)
- g \Big(
k(r y - t w)
- m(p y - t u)
+ o(p w - r u)
\Big)
$$
$$
+ h \Big(
k(q y - t v)
- l(p y - t u)
+ o(p v - q u)
\Big)
- j \Big(
k(q w - r v)
- l(p w - r u)
+ m(p v - q u)
\Big)
\Bigg)
$$

### Bagian e det(A15)

$
e \ \det(A_{15}) =
e \begin{vmatrix}
f & g & h & i \\
k & l & m & n \\
p & q & r & s \\
u & v & w & x
\end{vmatrix}
$

Ekspansi kofaktor menjadi matriks 3x3

$
=
e \left[
f \begin{vmatrix}
l & m & n \\
q & r & s \\
v & w & x
\end{vmatrix}
- g \begin{vmatrix}
k & m & n \\
p & r & s \\
u & w & x
\end{vmatrix}
+ h \begin{vmatrix}
k & l & n \\
p & q & s \\
u & v & x
\end{vmatrix}
- i \begin{vmatrix}
k & l & m \\
p & q & r \\
u & v & w
\end{vmatrix}
\right]
$

Ekspansi kofaktor menjadi matriks 2x2

$
=
e \left[
f \left(
l \begin{vmatrix} r & s \\ w & x \end{vmatrix}
- m \begin{vmatrix} q & s \\ v & x \end{vmatrix}
+ n \begin{vmatrix} q & r \\ v & w \end{vmatrix}
\right)
- g \left(
k \begin{vmatrix} r & s \\ w & x \end{vmatrix}
- m \begin{vmatrix} p & s \\ u & x \end{vmatrix}
+ n \begin{vmatrix} p & r \\ u & w \end{vmatrix}
\right)
+ h \left(
k \begin{vmatrix} q & s \\ v & x \end{vmatrix}
- l \begin{vmatrix} p & s \\ u & x \end{vmatrix}
+ n \begin{vmatrix} p & q \\ u & v \end{vmatrix}
\right)
- i \left(
k \begin{vmatrix} q & r \\ v & w \end{vmatrix}
- l \begin{vmatrix} p & r \\ u & w \end{vmatrix}
+ m \begin{vmatrix} p & q \\ u & v \end{vmatrix}
\right)
\right]
$

Determinan 2x2

$
=
e \Big(
f \big(
l(rx - sw)
- m(qx - sv)
+ n(qw - rv)
\big)
- g \big(
k(rx - sw)
- m(px - su)
+ n(pw - ru)
\big)
+ h \big(
k(qx - sv)
- l(px - su)
+ n(pv - qu)
\big)
- i \big(
k(qw - rv)
- l(pw - ru)
+ m(pv - qu)
\big)
\Big)
$

Operasi selanjutnya

$
\det(A) =
a \Big[
g(m(sy - tx) - n(ry - tw) + o(rx - sw))
- h(l(sy - tx) - n(qy - tv) + o(qx - sv))
+ i(l(ry - tw) - m(qy - tv) + o(qw - rv))
- j(l(rx - sw) - m(qx - sv) + n(qw - rv))
\Big]
- b \Big[
f(m(sy - tx) - n(ry - tw) + o(rx - sw))
- h(k(sy - tx) - n(py - tu) + o(px - su))
+ i(k(ry - tw) - m(py - tu) + o(pw - ru))
- j(k(rx - sw) - m(px - su) + n(pw - ru))
\Big]
+ c \Big[
f(l(sy - tx) - n(qy - tv) + o(qx - sv))
- g(k(sy - tx) - n(py - tu) + o(px - su))
+ i(k(qy - tv) - l(py - tu) + o(pv - qu))
- j(k(qx - sv) - l(px - su) + n(pv - qu))
\Big]
- d \Big[
f(l(ry - tw) - m(qy - tv) + o(qw - rv))
- g(k(ry - tw) - m(py - tu) + o(pw - ru))
+ h(k(qy - tv) - l(py - tu) + o(pv - qu))
- j(k(qw - rv) - l(pw - ru) + m(pv - qu))
\Big]
+ e \Big[
f(l(rx - sw) - m(qx - sv) + n(qw - rv))
- g(k(rx - sw) - m(px - su) + n(pw - ru))
+ h(k(qx - sv) - l(px - su) + n(pv - qu))
- i(k(qw - rv) - l(pw - ru) + m(pv - qu))
\Big]
$

##Operasi Adjoin Matriks

$$
 \operatorname{adj}(A)_{ij} = (-1)^{i+j} M_{ji}
$$

$
A =
\begin{bmatrix}
a & b & c & d & e \\
f & g & h & i & j \\
k & l & m & n & o \\
p & q & r & s & t \\
u & v & w & x & y
\end{bmatrix}
$

$
\operatorname{adj}A =
\begin{bmatrix}
a & -b & c & -d & e \\
-f & g & -h & i & -j \\
k & -l & m & -n & o \\
-p & q & -r & s & -t \\
u & -v & w & -x & y
\end{bmatrix}
$

$
\operatorname{adj}A =
\begin{bmatrix}
+\begin{vmatrix}
g & h & i & j\\
l & m & n & o\\
q & r & s & t\\
v & w & x & y
\end{vmatrix}
&
-\begin{vmatrix}
b & c & d & e\\
l & m & n & o\\
q & r & s & t\\
v & w & x & y
\end{vmatrix}
&
+\begin{vmatrix}
b & c & d & e\\
g & h & i & j\\
q & r & s & t\\
v & w & x & y
\end{vmatrix}
&
-\begin{vmatrix}
b & c & d & e\\
g & h & i & j\\
l & m & n & o\\
v & w & x & y
\end{vmatrix}
&
+\begin{vmatrix}
b & c & d & e\\
g & h & i & j\\
l & m & n & o\\
q & r & s & t
\end{vmatrix}
\\
-\begin{vmatrix}
f & h & i & j\\
k & m & n & o\\
p & r & s & t\\
u & w & x & y
\end{vmatrix}
&
+\begin{vmatrix}
a & c & d & e\\
k & m & n & o\\
p & r & s & t\\
u & w & x & y
\end{vmatrix}
&
-\begin{vmatrix}
a & c & d & e\\
f & h & i & j\\
p & r & s & t\\
u & w & x & y
\end{vmatrix}
&
+\begin{vmatrix}
a & c & d & e\\
f & h & i & j\\
k & m & n & o\\
u & w & x & y
\end{vmatrix}
&
-\begin{vmatrix}
a & c & d & e\\
f & h & i & j\\
k & m & n & o\\
p & r & s & t
\end{vmatrix}
\\
+\begin{vmatrix}
f & g & i & j\\
k & l & n & o\\
p & q & s & t\\
u & v & x & y
\end{vmatrix}
&
-\begin{vmatrix}
a & b & d & e\\
k & l & n & o\\
p & q & s & t\\
u & v & x & y
\end{vmatrix}
&
+\begin{vmatrix}
a & b & d & e\\
f & g & i & j\\
p & q & s & t\\
u & v & x & y
\end{vmatrix}
&
-\begin{vmatrix}
a & b & d & e\\
f & g & i & j\\
k & l & n & o\\
u & v & x & y
\end{vmatrix}
&
+\begin{vmatrix}
a & b & d & e\\
f & g & i & j\\
k & l & n & o\\
p & q & s & t
\end{vmatrix}
\\
-\begin{vmatrix}
f & g & h & j\\
k & l & m & o\\
p & q & r & t\\
u & v & w & y
\end{vmatrix}
&
+\begin{vmatrix}
a & b & c & e\\
k & l & m & o\\
p & q & r & t\\
u & v & w & y
\end{vmatrix}
&
-\begin{vmatrix}
a & b & c & e\\
f & g & h & j\\
p & q & r & t\\
u & v & w & y
\end{vmatrix}
&
+\begin{vmatrix}
a & b & c & e\\
f & g & h & j\\
k & l & m & o\\
u & v & w & y
\end{vmatrix}
&
-\begin{vmatrix}
a & b & c & e\\
f & g & h & j\\
k & l & m & o\\
p & q & r & t
\end{vmatrix}
\\
+\begin{vmatrix}
f & g & h & i\\
k & l & m & n\\
p & q & r & s\\
u & v & w & x
\end{vmatrix}
&
-\begin{vmatrix}
a & b & c & d\\
k & l & m & n\\
p & q & r & s\\
u & v & w & x
\end{vmatrix}
&
+\begin{vmatrix}
a & b & c & d\\
f & g & h & i\\
p & q & r & s\\
u & v & w & x
\end{vmatrix}
&
-\begin{vmatrix}
a & b & c & d\\
f & g & h & i\\
k & l & m & n\\
u & v & w & x
\end{vmatrix}
&
+\begin{vmatrix}
a & b & c & d\\
f & g & h & i\\
k & l & m & n\\
p & q & r & s
\end{vmatrix}
\end{bmatrix}
$

##Operasi Invers Matriks
$$
A^{-1} = \frac{1}{\det(A)} \operatorname{Adj}(A)
$$

Contoh matriks 5X5
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

Mencari Determinan
$$
\det(A)=1[1(1(1\cdot1-0\cdot0)-0(0\cdot1-0\cdot0)+2(0\cdot0-1\cdot0))-0(0(1\cdot1-0\cdot0)-0(0\cdot1-2\cdot2)+2(0\cdot0-2\cdot2))+2(0(0\cdot1-0\cdot0)-1(0\cdot1-2\cdot2)+2(0\cdot0-0\cdot0))-0(0(0\cdot0-1\cdot0)-1(0\cdot0-0\cdot0)+0(0\cdot0-0\cdot0))]-0[0(1(1\cdot1-0\cdot0)-0(0\cdot1-0\cdot0)+2(0\cdot0-1\cdot0))-0(0(1\cdot1-0\cdot0)-0(0\cdot1-2\cdot2)+2(0\cdot0-2\cdot2))+2(0(0\cdot1-0\cdot0)-1(0\cdot1-2\cdot2)+2(0\cdot0-0\cdot0))-0(0(0\cdot0-1\cdot0)-1(0\cdot0-0\cdot0)+0(0\cdot0-0\cdot0))]+2[0(0(1\cdot1-0\cdot0)-0(0\cdot1-2\cdot2)+2(0\cdot0-2\cdot2))-1(0(1\cdot1-0\cdot0)-0(2\cdot1-0\cdot0)+2(2\cdot0-1\cdot0))+2(0(0\cdot1-2\cdot2)-0(2\cdot1-0\cdot0)+2(2\cdot2-0\cdot0))-0(0(0\cdot0-2\cdot0)-0(2\cdot0-0\cdot0)+0(2\cdot2-0\cdot0))]-0[0(0(0\cdot0-1\cdot0)-1(0\cdot0-0\cdot0)+0(0\cdot0-0\cdot0))-1(0(0\cdot0-1\cdot0)-0(2\cdot0-0\cdot0)+2(2\cdot0-1\cdot0))+0(0(0\cdot0-0\cdot0)-0(2\cdot0-0\cdot0)+2(2\cdot2-0\cdot0))-0(0(0\cdot0-2\cdot0)-0(2\cdot0-0\cdot0)+1(2\cdot2-0\cdot0))]+0[0(0(0\cdot0-1\cdot0)-1(0\cdot0-0\cdot0)+0(0\cdot0-0\cdot0))-1(0(0\cdot0-1\cdot0)-0(2\cdot0-0\cdot0)+0(2\cdot0-1\cdot0))+0(0(0\cdot0-0\cdot0)-0(2\cdot0-0\cdot0)+0(2\cdot2-0\cdot0))-2(0(0\cdot0-2\cdot0)-0(2\cdot0-0\cdot0)+1(2\cdot2-0\cdot0))]
$$

$$
\det(A)=1(1)+2(16)=33
$$

Mencari Adjoin
$$
\operatorname{adj}A =
\begin{bmatrix}
+\begin{vmatrix}
1 & 0 & 2 & 0\\
0 & 1 & 0 & 2\\
0 & 0 & 1 & 0\\
2 & 0 & 0 & 1
\end{vmatrix}
&
-\begin{vmatrix}
0 & 2 & 0 & 0\\
0 & 1 & 0 & 2\\
0 & 0 & 1 & 0\\
2 & 0 & 0 & 1
\end{vmatrix}
&
+\begin{vmatrix}
0 & 2 & 0 & 0\\
1 & 0 & 2 & 0\\
0 & 0 & 1 & 0\\
2 & 0 & 0 & 1
\end{vmatrix}
&
-\begin{vmatrix}
0 & 2 & 0 & 0\\
1 & 0 & 2 & 0\\
0 & 1 & 0 & 2\\
2 & 0 & 0 & 1
\end{vmatrix}
&
+\begin{vmatrix}
0 & 2 & 0 & 0\\
1 & 0 & 2 & 0\\
0 & 1 & 0 & 2\\
0 & 0 & 1 & 0
\end{vmatrix}
\\
-\begin{vmatrix}
0 & 0 & 2 & 0\\
0 & 1 & 0 & 2\\
2 & 0 & 1 & 0\\
0 & 0 & 0 & 1
\end{vmatrix}
&
+\begin{vmatrix}
1 & 2 & 0 & 0\\
0 & 1 & 0 & 2\\
2 & 0 & 1 & 0\\
0 & 0 & 0 & 1
\end{vmatrix}
&
-\begin{vmatrix}
1 & 2 & 0 & 0\\
0 & 0 & 2 & 0\\
2 & 0 & 1 & 0\\
0 & 0 & 0 & 1
\end{vmatrix}
&
+\begin{vmatrix}
1 & 2 & 0 & 0\\
0 & 0 & 2 & 0\\
0 & 1 & 0 & 2\\
0 & 0 & 0 & 1
\end{vmatrix}
&
-\begin{vmatrix}
1 & 2 & 0 & 0\\
0 & 0 & 2 & 0\\
0 & 1 & 0 & 2\\
2 & 0 & 1 & 0
\end{vmatrix}
\\
+\begin{vmatrix}
0 & 1 & 2 & 0\\
0 & 0 & 0 & 2\\
2 & 0 & 1 & 0\\
0 & 2 & 0 & 1
\end{vmatrix}
&
-\begin{vmatrix}
1 & 0 & 0 & 0\\
0 & 0 & 0 & 2\\
2 & 0 & 1 & 0\\
0 & 2 & 0 & 1
\end{vmatrix}
&
+\begin{vmatrix}
1 & 0 & 0 & 0\\
0 & 1 & 2 & 0\\
2 & 0 & 1 & 0\\
0 & 2 & 0 & 1
\end{vmatrix}
&
-\begin{vmatrix}
1 & 0 & 0 & 0\\
0 & 1 & 2 & 0\\
0 & 0 & 0 & 2\\
0 & 2 & 0 & 1
\end{vmatrix}
&
+\begin{vmatrix}
1 & 0 & 0 & 0\\
0 & 1 & 2 & 0\\
0 & 0 & 0 & 2\\
2 & 0 & 1 & 0
\end{vmatrix}
\\
-\begin{vmatrix}
0 & 1 & 0 & 0\\
0 & 0 & 1 & 2\\
2 & 0 & 0 & 0\\
0 & 2 & 0 & 1
\end{vmatrix}
&
+\begin{vmatrix}
1 & 0 & 2 & 0\\
0 & 0 & 1 & 2\\
2 & 0 & 0 & 0\\
0 & 2 & 0 & 1
\end{vmatrix}
&
-\begin{vmatrix}
1 & 0 & 2 & 0\\
0 & 1 & 0 & 0\\
2 & 0 & 0 & 0\\
0 & 2 & 0 & 1
\end{vmatrix}
&
+\begin{vmatrix}
1 & 0 & 2 & 0\\
0 & 1 & 0 & 0\\
0 & 0 & 1 & 2\\
0 & 2 & 0 & 1
\end{vmatrix}
&
-\begin{vmatrix}
1 & 0 & 2 & 0\\
0 & 1 & 0 & 0\\
0 & 0 & 1 & 2\\
2 & 0 & 0 & 0
\end{vmatrix}
\\
+\begin{vmatrix}
0 & 1 & 0 & 2\\
0 & 0 & 1 & 0\\
2 & 0 & 0 & 1\\
0 & 2 & 0 & 0
\end{vmatrix}
&
-\begin{vmatrix}
1 & 0 & 2 & 0\\
0 & 0 & 1 & 0\\
2 & 0 & 0 & 1\\
0 & 2 & 0 & 0
\end{vmatrix}
&
+\begin{vmatrix}
1 & 0 & 2 & 0\\
0 & 1 & 0 & 2\\
2 & 0 & 0 & 1\\
0 & 2 & 0 & 0
\end{vmatrix}
&
-\begin{vmatrix}
1 & 0 & 2 & 0\\
0 & 1 & 0 & 2\\
0 & 0 & 1 & 0\\
0 & 2 & 0 & 0
\end{vmatrix}
&
+\begin{vmatrix}
1 & 0 & 2 & 0\\
0 & 1 & 0 & 2\\
0 & 0 & 1 & 0\\
2 & 0 & 0 & 1
\end{vmatrix}
\end{bmatrix}
$$

$$
\operatorname{adj}(A)_{11}
=
\begin{vmatrix}
1 & 0 & 2 & 0\\
0 & 1 & 0 & 2\\
0 & 0 & 1 & 0\\
2 & 0 & 0 & 1
\end{vmatrix}
= 1
$$

$$
\operatorname{adj}(A)_{12}
=
-\begin{vmatrix}
0 & 2 & 0 & 0\\
0 & 1 & 0 & 2\\
0 & 0 & 1 & 0\\
2 & 0 & 0 & 1
\end{vmatrix}
= 0
$$

$$
\operatorname{adj}(A)_{13}
=
\begin{vmatrix}
0 & 2 & 0 & 0\\
1 & 0 & 2 & 0\\
0 & 0 & 1 & 0\\
2 & 0 & 0 & 1
\end{vmatrix}
= 16
$$

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

$$
\text{Determinan: }
\det(A)=33
$$

$$
\text{Adjoin: }
\operatorname{adj}(A)=
\begin{bmatrix}
1 & 0 & 16 & 0 & 0 \\
0 & 1 & 0 & 16 & 0 \\
0 & 0 & 1 & 0 & 16 \\
16 & 0 & 0 & 1 & 0 \\
0 & 16 & 0 & 0 & 1
\end{bmatrix}
$$

$$
\text{Invers: }
A^{-1}=\frac{1}{33}
\begin{bmatrix}
1 & 0 & 16 & 0 & 0 \\
0 & 1 & 0 & 16 & 0 \\
0 & 0 & 1 & 0 & 16 \\
16 & 0 & 0 & 1 & 0 \\
0 & 16 & 0 & 0 & 1
\end{bmatrix}
$$

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