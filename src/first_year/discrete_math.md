# Matemática discreta I

<!-- toc -->

En esta materia se tomarán principalmente los conjuntos de los números naturales \\(\mathbb{R}\\) y los números enteros \\(\mathbb{Z}\\), ya que son aquellos que nombramos **discretos**, debido a la distancia que separa a cada uno de sus elementos.

Originalmente, comprendemos dos operaciones en \\(\mathbb{N}\\) que luego extendemos a \\(\mathbb{Z}\\): la **suma** y el **producto**. Ambos serán tomados como obvios y no se demostrarán.

A partir de esa aclaración, podremos definir entonces a los **axiomas**, que funcionan como herramientas para demostrar propiedades de \\(\mathbb{Z}\\) y tampoco se demostrarán.

## Axiomas de los enteros
> En todos los casos, \\(\forall a,b,c,d \in \mathbb{Z}\\)

- \\(I_1: a + b \in \mathbb{Z} \land a \times b \in \mathbb{Z}\\)
- \\(I_2:\\) La suma y el producto son **conmutativas** (conmutatividad)
\\[a + b = b + a \land a \times b = b \times a\\]
- \\(I_3:\\) La suma y el producto son **asociativas** (asociatividad)
\\[(a + b) + c = a + (b + c) \land (a \times b) \times c = a \times (b \times c)\\]
- \\(I_4:\\) Existe un elemento neutro
\\[\exists 0, 1 \in \mathbb{Z}: a + 0 = a \land a \times 1 = a\\]
- \\(I_5:\\) Relación entre la suma y el producto: **distributiva**
\\[a \times (b + c) = a \times b + a \times c\\]
- \\(I_6:\\) Existe un **único** inverso aditivo
\\[\exists! (-a) \in \mathbb{Z}: a + (-a) = 0\\]
- \\(I_7:\\) Cancelación
\\[a \neq 0 \land ab = ac \implies b = c\\]
- \\(I_8:\\) Ley de la **tricotomía**, solo puede cumplirse uno de los siguientes casos:
\\[a < b \lor a = b \lor b < a\\]
- \\(I_9:\\) Ley de la **transitividad**:
\\[a < b \land b < c \implies a < c\\]
- \\(I_{10}:\\) Compatibilidad del orden con la suma:
\\[a < b \implies a + c < b + c\\]
- \\(I_{11}:\\) Compatibilidad del orden con el producto:
\\[a < b \land 0 < c \implies a \times c < b \times c\\]
- \\(I_{12}:\\) \\(\mathbb{X}\subseteq\mathbb{Z} \land \mathbb{X} \neq \emptyset \land \mathbb{X}\\ \text{tiene cota inferior}\implies \mathbb{X}\\ \text{tiene un mínimo}\\)

### Algunas observaciones y definiciones importantes

#### Resta

\\(a, b \in \mathbb{Z}: a - b = a + (-b)\\)

#### Regla de los signos

\\(a, b \in \mathbb{Z} \implies (-a)(-b) = ab \land (-a)b = a(-b) = -(ab) \\)

#### Significado natural de las desigualdades
- \\(a > b \implies b < a\\\)
- \\(a \leq b \implies a = b \lor a < b\\)
- \\(a \geq b \implies a = b \lor b < a\\)

> **Nota**: al comprender los nuevos significados de \\(>, \geq,\\) y \\(\leq\\), obtendremos una versión más general de los axiomas \\(I_9, I_{10}, I_{11}\\) y \\(I_{12}\\)

#### Números positivos y negativos
- Positivo: \\(a \in \mathbb{Z}: a > 0\\)
- Negativo: \\(a \in \mathbb{Z}: a < 0\\)

## Orden

El orden en los enteros nos permite diferenciarlos y ubicarlos en base a su valor, para lograr una visión organizada de su extensión como conjunto. Es de esta percepción que surgen los axiomas de tricotomía, transitividad, etc. Véase [Axiomas de los enteros](#axiomas-de-los-enteros).

### Relaciones

Encontramos que, a partir de los operadores de orden \\(>, <, \leq, \\) y \\(\geq\\), podemos encontrar ciertas propiedades.

Por ejemplo, para \\(\leq\\) con \\(a,b,c, \in \mathbb{Z}\\):
- **Reflexividad**: \\(a \leq a: a = a \implies a \leq a\\)
- **Antisimetría**: \\(a \leq b \land b \leq a \implies a = b\\)
\\[
  \begin{align}
  a < b \land b < a \implies \text{Absurdo}\newline
  a < b \land b = a \implies \text{Absurdo}\newline
  a  b \land b < a \implies \text{Absurdo}\newline
  a = b \land b = a \implies a = b
  \end{align}
\\]
- **Transitividad**: \\(a \leq b \land b \leq c \implies a \leq c\\)

Es importante observar que:
- \\(<\\) **no** es una relación de orden.
- \\(=\\) es una **relación de equivalencia** pues es **simétrica**.
- Para negar:
  - \\(\neq: a \neq b \implies a < b \lor b < a\\)
  - \\(\ngeq: a \ngeq b \implies a = b \lor b < a \\)

## Cotas

Para \\(\mathbb{X} \subseteq \mathbb{Z}\\), definimos la cota inferior como \\(b \in \mathbb{X}: b \leq a, \forall a \in \mathbb{X}\\). Es decir, una cota inferior es el valor más pequeño de un conjunto.

Para dar sentido entonces al axioma \\(I_{12}\\), definimos al **mínimo** de un conjunto como la cota inferior \\(b\\) de un conjunto \\(\mathbb{X}\\) que a su vez cumple que \\(b \in \mathbb{X}\\), o sea, que forma parte del conjunto.