## Enteros

### Axiomas

> Axioma: propiedad que no se demuestra y que se utiliza para demostrar otras.

1. \\(a + b, a \times b \in \mathbb{Z}\\)
2. \\(a + b = b + a \land a \times b = b \times a\\)
3. \\(a + (b + c) = (a + b) + c \land a \times (b \times c) = (a \times b) \times c \\)
4. \\(\exists\\ 0, 1 \colon a + 0 = a \land a \times 1 = a\\)
5. \\(a \times (b + c) = ac + bc\\)
6. \\(\forall a \in \mathbb{Z}, \exists!\\ (-a) \in \mathbb{Z} \colon\\ a + (-a) = 0\\)
7. \\(a \neq 0 \land ab = bc \implies b = c\\)
8. \\(a < b \lor a = b \lor b > a \longrightarrow\\) **Tricotomía**
9. \\(a < b \land b < c \implies a < c \longrightarrow\\) **Transitividad**
10. \\(a < b \implies a + c < b + c\\)
11. \\(a < b \land c > 0 \implies ac < bc\\)
12. \\(\forall\\ X \subseteq \mathbb{Z},\\ \exists\\ b \in \mathbb{X} \colon\\ b \leq a,\\ \forall a \in \mathbb{X} \\)

Entendemos las propiedades de \\(\leq\\)
- \\(a \leq a \implies a = a \longrightarrow\\) **Reflexividad**
- \\(a \leq b \land b \leq a \implies a = b \longrightarrow\\) **Antisimetría**
- \\(a \leq b \land b \leq c = a \leq c \longrightarrow\\) **Transitividad**

Y observamos que
- \\(<\\) **no** es una relación de orden.
- \\(=\\) es una relación de equivalencia pues es **simétrica**.
- Para negar \\(\leq\\) ó \\(=\\), entendemos que \\(a \ne b \implies a > b \lor a < b\\) y \\(a \nless b \implies a > b \lor a = b\\)

### Cotas

Un conjunto \\(\mathbb{X}\\) tiene cota inferior cuando \\(\exists\\ b \in \mathbb{Z} \colon\\ b \leq a,\\ \forall a\in \mathbb{X}\\). Un conjunto tiene **mínimo** cuando ese \\(b \in \mathbb{X}\\). Por ejemplo, para \\(\mathbb{X} = \\{ 1, 2, 3 \\}\\), el mínimo es \\(1\\) puesto que cumple que sea menor o igual a cada elemento del conjunto y pertenece al mismo.

## Recursión e inducción

Una función está definida cuando su valor está **unívocamente determinado**, es decir, está definido.

Para definir propiedadades \\(\forall\\ n \in \mathbb{N}\\):

- Explítcitas \\(\longrightarrow U_n = 2n + 1\\)
- Recursivas:
\\[
\begin{align}
& U_1 = 1 \\\\
& U_2 = 2 \\\\
& U_n = U_{n - 1} + U_{n - 2}
\end{align}
\\]

### Sumatoria

Estas expresiones son equivalentes:

\\[
1 + 2 + 3 + \cdots + n = \sum_{i = 1}^{n}i
\\]

Por lo que definimos la sumatoria como:

\\[
a_1 + a_2 + \cdots + a_n = \sum_{i = 1}^{n}a_i
\\]

Y podemos ver que la sumatoria se reutiliza en sí misma:

\\[
\sum_{i = 1}^{n}a_i = \sum_{i = 1}^{n - 1}a_i + a_n
\\]

Pero podemos sustituirla por otra expresión equivalente:

\\[
\sum_{i = 1}^{n}i = \frac{n(n + 1)}{2}
\\]

### Productoria

Al igual que con la sumatoria, la productoria equivale de manera general a:

\\[
a_1 \times a_2 \times a_3 \times \cdots \times a_n = \prod_{i = 1}^{n}i
\\]

Y que, a su vez, podemos reemplazarla por una expresión equivalente, como es el caso del **factorial**:

\\[
\prod_{i = 1}^{n}i = i!
\\]

Definido recursivamente por:

\\[
\prod_{i = 1}^{n}i = \prod_{i = 1}^{n - 1}i \times n
\\]

Por ejemplo:

\\[
\begin{align}
\prod_{i = 1}^{3}i &= \prod_{i = 1}^{2}i \times 3 \\\\
\prod_{i = 1}^{3}i &= \prod_{i = 1}^{1}i \times 2 \times 3 \\\\
\prod_{i = 1}^{3}i &= 1 \times 2 \times 3 \\\\
\prod_{i = 1}^{3}i &= 6 = 3! \\\\
\end{align}
\\]

### Inducción

Sea \\(P(n)\\) una propiedad para \\(n \in \mathbb{N}\\), entonces:

- \\(P(1)\\) es verdadera **(Caso base)**
- \\(P(k)\\) es verdadera \\(\implies P(k + 1)\\) es verdadera para \\(k \in \mathbb{N}\\) **(Caso inductivo)**

Con la inducción buscamos generalizar una propiedad para todos los elementos de un conjunto, usualmente los naturales.

Por ejemplo, tomando en cuenta la sumatoria definida anteriormente por:

\\[\sum_{i = 1}^{n}i = \frac{n(n + 1)}{2} \quad n \in \mathbb{N} \\]

Veremos que se cumple el caso base para \\(i = 1\\)

\\[
\begin{align}
\sum_{i = 1}^{1}i &= \frac{1(1 + 1)}{2} \\\\
1 &= \frac{2}{2} \\\\
1 &= 1
\end{align}
\\]

Entonces, plantearemos nuestra **hipótesis inductiva** para \\(k \in \mathbb{N}\\), cumpliendo que \\(P(k) \implies P(k + 1)\\):

\\[
\left[ \sum_{i = 1}^{k}i = \frac{k(k + 1)}{2} \right] \space (H.I.)
\\]

Y, reemplazando \\(k\\) por \\(k + 1\\), obtendremos que queremos probar que:

\\[
\sum_{i = 1}^{k + 1}i = \frac{(k + 1)(k + 2)}{2}
\\]

Luego:

\\[
\begin{align}
\sum_{i = 1}^{k + 1}i &= \sum_{i = 1}^{k}i + (k + 1) \\\\
\sum_{i = 1}^{k + 1}i &= \frac{k(k + 1)}{2} + (k + 1) \quad (H.I.) \\\\
\sum_{i = 1}^{k + 1}i &= \frac{k(k + 1) + 2(k + 1)}{2} \\\\
\sum_{i = 1}^{k + 1}i &= \frac{(k + 1)(k + 2)}{2}
\end{align}
\\]

Por lo tanto, se demuestra \\(P(k + 1)\\) y se verifica la propiedad por inducción para \\(k \in \mathbb{N}\\).

También encontramos la **inducción corrida**, que involucra a \\(k \in \mathbb{N}_0\\) y comprueba que la propiedad vale para el anterior de un número en \\(\mathbb{N_0}\\). Por otro lado, la **inducción fuerte**, busca verificar la propiedad para cualquier entero, de la forma en que:

Dado un entero cualquiera \\(n_0\\) y sea \\(Z_{\geq n_0}\\) el conjunto de enteros tal que \\(n \geq n_0\\), (S\\) es un subconjunto de \\(Z_{\geq n_0}\\) que satisface:

- \\(n_0 \in S\\)
- \\(h \in S \implies \forall\\ h \in n_0 \leq h \leq k \implies k + 1 \in S \\)

Por lo que generalizamos para \\(n_0 \in \mathbb{N}\\) y una propiedad \\(P(n_0)\\) definida \\(\forall n \geq n_0\\):

- \\(P(n_0)\\) es verdadera.
- \\(P(k)\\) es verdadera \\(\forall n_0 \leq h \leq k \implies P(k + 1)\\) es verdadera.

Por ejemplo:

\\[
\begin{align}
U_1 &= 3 \\\\
U_2 &= 5 \\\\
U_n &= 3U_{n - 1} - 2U_{n - 2} \quad \forall \space n \geq 3
\end{align}
\\]

En este caso, deberemos probar \\(P(n)\\) para \\(n = 1\\) y para \\(n = 2\\), debido a que ambos conforman nuestros casos bases de los que depende la definición recursiva. Para dejar esto en claro, al encontrar nuestro supuesto que queremos probar, además de definir nuestra hipótesis inductiva para \\(k\\), deberemos hacerlo para \\(h\\) de modo que la propiedad se defina para el rango \\(n_0 \leq h \leq k\\):

\\[
n_0 = 1 \quad k \geq 1 \quad U_k = 2^k + 1 \quad U_h = 2^h + 1 \quad (n_0) \space 1 \leq h \leq k
\\]

## Conteo

Un conjunto \\(X\\) es finito cuando sus elementos se pueden **contar**, es decir, se pueden ordenar y hay uno final. Se define por:

\\[
\exists \space f \colon X \rightarrow \\{1, \dots, n\\} \space \text{biyectiva}
\\]

Y llamaremos **cardinal** a la cantidad de elementos de \\(X\\) denotada por \\(|X| = n\\)

### Principio de adición
Para \\(A, B\\) conjuntos finitos y disjuntos (es decir, \\(A \cap B = \emptyset \\)), entonces:

\\[
|A \cup B| = |A| + |B| \implies |A_1 \dots \cup A_n| = |A_1| + \dots + |A_n|
\\]

### Principio de multiplicación
Para \\(A, B\\) conjuntos finitos y disjuntos definimos el producto cartesiano de \\(A \space \text{por} \space B\\) como \\(A \times B\\) y generalizamos:

\\[
A \times B = \\{(a, b) \colon a \in A \land b \in B\\} \implies |A \times B| = |A| \times |B|
\\]

