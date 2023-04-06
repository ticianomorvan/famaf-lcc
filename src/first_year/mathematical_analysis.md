# Análisis matemático I (LCC)

<!-- toc -->

> **Conjunto**: colección de elementos que comparten peculiaridades.

Para el análisis, comprendemos diversos conjuntos numéricos.

- **Naturales**: \\(\mathbb{N} = \\{ 1, 2, 3, 4, 5, ... \\} \\)
- **Enteros**: \\(\mathbb{Z} = \\{ -2, -1, 0, 1, 2, ... \\} \\)
- **Racionales**: \\(\mathbb{Q} = \\{ \frac{1}{2}, \frac{1}{4}, \frac{2}{3}, ... \\} \\)
- **Irracionales**: \\(\mathbb{II} = \\{ \sqrt{2}, \sqrt{3}, \sqrt{5}, ... \\} \\)
- **Reales**: \\(\mathbb{R} = \mathbb{N}\cup\mathbb{Z}\cup\mathbb{Q}\cup\mathbb{II} \\)

Partiendo desde el conjunto de los números naturales, comenzamos a notar diversas particularidades.

- Para todo \\(\mathbb{N}\\), su suma y su producto darán como resultado otro \\(\mathbb{N}\\). Sin embargo, su diferencia no se comporta de la misma manera.
- Para resolver este problema, se incorporan el conjunto de los \\(\mathbb{Z}\\), que incluye los números negativos y el elemento neutro, llamado cero. Pero a su vez, la división entre dos enteros no corresponde siempre a otro igual.
- Entonces, es que surgen los \\(\mathbb{Q}\\) de la forma \\(\frac{m}{n}\\), donde \\(m\in\mathbb{Z}\\) y \\(n\in\mathbb{Z}\\).

A los números racionales o números del conjunto \\(\mathbb{Q}\\), podemos expresarlos de forma **decimal** y forma **fraccionaria**. La decimal pretende demostrar la parte *no entera* del número, de forma **finita** o **infinita periódica**, por ejemplo \\(1.25\\) ó \\(1.\overline{33}\\), donde este último contiene infinitas repeticiones del \\(.33\\).

Las fracciones tienen diversas propiedades interesantes:
- \\(\frac{m}{0}\\) **NO** está definido dentro de \\(\mathbb{R}\\).
- Dos fracciones son equivalentes si \\(\frac{m}{n}, \frac{p}{q}\\) con \\(m * q = n * q\\)
- \\(\frac{m}{n}\\) es irreducible si \\(m\\) y \\(n\\) no tienen divisores en común.
- La suma de fracciones se define como \\(\frac{m}{n} + \frac{p}{q} = \frac{mq + np}{nq}\\)
- La multiplicación de fracciones se define como \\(\frac{m}{n} * \frac{p}{q} = \frac{mp}{nq}\\)
- La división de fracciones se define como \\(\frac{\frac{m}{n}}{\frac{p}{q}} = \frac{m}{n} * \frac{q}{p} = \frac{mq}{np}\\)

Cabe aclarar que no todos los números tienen representación infinita periódica, por lo que surgen los **Irracionales** o \\(\mathbb{II}\\), que coexisten con los demás conjuntos dentro del conjunto de los reales.

Para representar gráficamente a los números reales, utilizamos la **recta numérica**, que es una línea horizontal numerada y que no termina en ninguno de sus extremos. Es importante colocar el \\(0\\) entre los números positivos y los negativos, que se suelen colocar por convención a la derecha e izquierda del cero respectivamente.

## Propiedades de los números reales \\(\mathbb{R}\\)
> Nota: estas propiedades valen \\(\forall a,b,c\in\mathbb{R}\\)

1. Propiedad asociativa de la suma: \\((a + b) + c = a + (b + c)\\)
2. Existe un elemento neutro para la suma: \\(\exists0\in\mathbb{R}: 0 + a = a + 0 = a\\)
3. Existe un elemento opuesto para la suma: \\(\exists(-a)\in\mathbb{R}: a + (-a) = 0\\)
4. Propiedad conmutativa de la suma: \\(a + b = b + a\\)
5. Propiedad asociativa del producto: \\((a * b) * c = a * (b * c)\\)
6. Existe un elemento neutro para el producto: \\(\exists1\in\mathbb{R}: 1 * a = a * 1 = a\\)
7. Existe un inverso para el producto: \\(\exists a^{-1}\in\mathbb{R}: a * a^{-1} = 1\\)
8. Propiedad conmutativa del producto: \\(a * b = b * a\\)
9. Propiedad distributiva del producto: \\(a(b + c) = ab + bc\\)

> Observación: \\(a * b = 0 \implies a = 0 \lor b = 0\\)

**Radicación**: Se define la raíz cuadrada de \\(a\\) siendo un número positivo, al número también positivo \\(b\\) tal que \\(b ^ 2 = a\\) y \\(\sqrt{a} = b\\), como también vale que \\((- b) ^ 2 = a\\) y \\(-\sqrt{a} = -b\\). Es importante aclarar que vale *análogamente* para las raíces **pares**.

A su vez también se definen las raíces de índice **impar** para todos los \\(\mathbb{R}\\).

Así, extendremos la definición de **potencia** para todo número positivo de exponente racional:

> \\[a ^ {\frac{m}{n}} = \sqrt[n]{a ^ m}\\]

Y podemos agregar más propiedades a partir de dichas definiciones:

10. Propiedad distributiva de la potencia respecto al producto: \\((a * b) ^ n = a ^ n * b ^ n \\) con \\(n\in\mathbb{Q}\\)
11. Producto de potencias de igual base: \\(a ^ n * a ^ m = a ^ {m + n}\\) para \\(m, n\in\mathbb{Q}\\)
12. Diferencia de cuadrados: \\(a ^ 2 - b ^ 2 = (a + b) (a - b)\\)
13. Cuadrado del binomio: \\((a + b) ^ 2 = a ^ 2 + 2ab + b ^ 2\\)

## Ecuaciones
Una ecuación es *una igualdad entre expresiones algebraicas que contienen una o más incógnitas*.

Para resolver ecuaciones, aplicamos las propiedades de \\(\mathbb{R}\\) para poder *despejar* la incógnita y encontrar su valor.

Por ejemplo:

\\[2x + 6 = 18 \\]
\\[2x + 6 + (-6) = 18 + (-6)\\]
\\[2x \times \frac{1}{2} = 12 \times \frac{1}{2}\\]
\\[\Rightarrow x = 6 \\]

Es importante notar que *resolver una ecuación* es encontrar el conjunto de soluciones para los cuales la igualdad se cumple, es decir, el **conjunto solución**.

Definimos, por ahora, dos tipos de ecuaciones:
- Ecuaciones lineales: donde la/s incógnitas se encuentran a potencia \\(1\\).
- Ecuaciones cuadráticas: donde la/s incógnitas se encuentran a potencia \\(2\\).

### Ecuaciones cuadráticas
Si bien cualquier ecuación que contenga una incógnita a potencia \\(2\\) se pueden llamar *cuadráticas*, encontramos un caso especial de éstas, donde \\(ax^2 + bx + c = 0\\) para todo \\(a,b,c\in\mathbb{R}\\). Para este tipo de ecuaciones, buscaremos las llamadas **raíces** (es decir, aquellos números que al sustituir a la incógnita, mantienen la igualdad a \\(0\\)). Para ello, podemos utilizar dos métodos:

1. Bhaskara o fórmula resolvente, que resultará en las dos raíces a partir del \\(\pm\\)

\\[x_1,_2 = \frac{-b \pm \sqrt{b ^ 2 - 4ac}}{2a}\\]

2. Completar cuadrados, en el que buscaremos escribir la ecuación cuadrática de la forma:

\\[(x + a) ^ 2 + b\\]

## Desigualdades
Una desigualdad comprende dos expresiones que pueden ser distintas o iguales, pero no directamente iguales. Por ejemplo: \\(x + 3 < 5\\)

### Propiedades
1. \\(a > 0 \land b > 0 \implies a + b > 0 \land a \times b > 0\\)
2. \\(a \in \mathbb{R} \implies a = 0 \lor a > 0 \lor (-a) > 0\\)

Definimos un número positivo como \\(a > 0\\), mientras que un negativo \\(a < 0\\). También, sabemos que un número es **mayor** a otro si \\(a - b > 0\\)

### Reglas
- \\(a > b \land b > c \implies a > c\\)
- \\(a > b \implies a + c > b + c,\\ \forall c \in \mathbb{R}\\)
- \\(a > b \land c > d \implies a + c > b + d\\)
- \\(a > b \land c > 0 \implies a \times c > b \times c\\)
- \\(a > b \land c < 0 \implies a \times c < b \times c\\)

### Intervalos y conjuntos
Recordando la definición de conjuntos, podemos definir las operaciones entre ellos:

- Unión: \\(\mathbf{A}\cup\mathbf{B} = \\{ x \in \mathbf{A} \lor x \in \mathbf{B} \\}\\)
- Intersección: \\(\mathbf{A}\cap\mathbf{B} = \\{ x \in \mathbf{A} \land x \in \mathbf{B}\\}\\)

Además de la notación de conjuntos, podemos definir **intervalos** de números reales:

- Abierto: \\((a, b) \implies \\{ x \in \mathbb{R} \colon a < x < b \\}\\)
- Cerrado: \\([a, b] \implies \\{ x \in \mathbb{R} \colon a \leq x \leq b \\}\\)
- Semiabierto: \\([a, b) \implies \\{ x \in \mathbb{R} \colon a \leq x < b \\} \\)

Aunque también tenemos intervalos infinitos, por ejemplo: \\([a, \infty+) = \\{ x \in \mathbb{R} \colon a \leq x \\}\\)

> Nota: si aparece el infinito en un intervalo, debe ser **siempre** abierto por su lado.

## Valor absoluto
Podemos definir el valor absoluto de \\(a\\) que denotamos \\(|a|\\) como:

\\[
|x| =
  \begin{cases}
  \displaylines{x, & x \geq 0 \\\\\\ -x, & x < 0}
  \end{cases}
\\]

Podemos entender también la definición de valor absoluto como la **distancia al cero** a la que se encuentra un número. Por ejemplo, \\(|-5| = 5\\), es decir, el \\(-5\\) se encuentra a cinco unidades del cero.

### Propiedades
1. \\(|a^{2}| = a^{2} \land |a| = \sqrt{a^{2}} = \pm a \\)
2. \\(|a \times b| = |a| \times |b| \land |\frac{a}{b}| = \frac{|a|}{|b|}\\)
3. \\(|a + b| \leq |a| + |b|\\)

### Resultados útiles
- \\(|x| = a \iff x = a \lor x = (-a) \\)
- \\(|x| < a \iff -a < x < a \\)
- \\(|x| > a \iff x \in (-\infty, -a)\cup(a, \infty) \implies x < (-a) \lor a < x\\)

## Funciones
Una función es una regla que asigna a cada elemento de un conjunto \\(\mathbf{X}\\) un unico elemento \\(f(x)\\) de un conjunto \\(\mathbf{Y}\\).

Para \\(f\colon \mathbf{X} \longrightarrow \mathbf{Y}\\), El **dominio** (\\(Dom f\\)) es \\(\mathbf{X}\\), mientras que \\(\mathbf{Y}\\) es el **conjunto de llegada** (o codominio). \\(f(x)\\) es la imagen de \\(\mathbf{X}\\) por \\(\mathbf{f}\\), es decir, a que valor llega un elemento \\(\mathbf{x}\\) a partir de \\(\mathbf{f}\\). Por el contrario, la **imagen de f** (\\(Im f\\)) son todos los valores que toma a partir de uno del conjunto \\(\mathbf{X}\\).  

Hablamos de \\(y = f(x)\\) con \\(\\mathbf{y}\\) como variable **dependiente** y \\(\mathbf{x}\\) como variable **independiente**. Para una función sin dominio definido, lo entendemos como el conjunto real más extenso para el cual está definido.

### Recta

Definimos una recta por \\(y = ax + b\\), donde los pares \\((x, y)\\) del plano satisfacen esta ecuacion.

Comprendemos diversas ecuaciones a partir de la anterior:
- \\(x = \frac{-b}{a}, \text{con}\\ y = 0\\)
- \\(a = \frac{y_2 - y_1}{x_2 - x_1}\\)
- \\(b = y - ax\\)

Y definimos dos variantes de una recta:
- **Paralela**, aquella que tiene la misma pendiente.
- **Perpendicular**, aquella que tiene pendiente inversa reciproca.

### Desplazamientos
Con \\(c > 0\\)
- Verticales:
  - Hacia arriba: \\(f(x) + c\\)
  - Hacia abajo: \\(f(x) - c\\)
- Horizontales:
  - Hacia la izquierda: \\(f(x + c)\\)
  - Hacia la derecha: \\(f(x - c)\\)

### Estiramientos y reflexiones
Un estiramiento se da con \\(c \geq 1\\), mientras que una compresión se da con \\(c < 0\\). Ambos comparten las fórmulas para el plano vertical y horizontal:
- Vertical: \\(c \times f(x)\\)
- Horizontal: \\(f(c \times x)\\)

Una reflexión, por otro lado, puede darse a través de las siguientes fórmulas:
- Vertical: \\(-f(x)\\)
- Horizontal: \\(f(-x)\\)

### Funciones pares e impares
Una funcion par es aquella que satisface que \\(f(x) = -f(x)\\), mientras que una impar satisface que \\(f(x) = -f(-x) \iff -f(x) = f(-x)\\). La funcion par es simétrica con respecto al eje x, mientras que la impar es simétrica con respecto al origen.

### Operaciones con funciones
- Suma: \\(f(x) + g(x) = (f + g)(x)\\)
- Multiplicación: \\(f(x) * g(x) = f \times g \times x\\)
- División: \\(\frac{f}{g} = \frac{f(x)}{g(x)}\\)

### Composición de funciones
Si \\(g(x) \in \mathbf{A}\\) y \\(f(x) \in \mathbf{B}\\) entonces se puede definir \\(f \circ g\\) como \\(f(g(x))\\).

La imagen de \\(g\\) debe estar contenida dentro del dominio de \\(f\\) para que \\(f \circ g \\) esté definida, es decir, **los valores que devuelve \\(g(x) \longrightarrow\\) valores que toma \\(f(x)\\)**

### Inyectivas y suryectivas (o sobreyectivas)
Tomando a \\(f\colon \mathbf{X} \longrightarrow \mathbf{Y}\\) como una función:

Una función es inyectiva si \\(\forall x_1, x_2 \in \mathbf{X}, x_1 \neq x_2 \implies f(x_1) \neq f(x_2)\\). Por lo tanto, para que la desigualdad no se cumpla, el único caso posible es que \\(x_1 = x_2\\). Para demostrar que una función es inyectiva, podemos igualar \\(f(x_1) = f(x_2)\\) y verificar que \\(x_1 = x_2\\)

Por otro lado, una función es suryectiva si \\(Im \\ \mathbf{f} = \mathbf{Y}\\). Es decir, si todo elemento del contradominio es imagen de algún elemento del conjunto \\(\mathbf{X}\\). Puede expresarse como: \\(\forall y \in \mathbf{Y}, \exists x \in \mathbf{X} \colon f(x) = y\\). Para demostrarse que una función es suryectiva, se debe despejar a \\(\mathbf{x}\\) de la ecuación de la forma \\(y = f(x)\\) y probar que, al evaluar \\(f(x)\\) en dicho despeje, se obtiene \\(\mathbf{x}\\).

Si una función es inyectiva y suryectiva simultáneamente, es posible calcular su **inversa**.

### Función inversa

Definimos la inversa de una función biyectiva \\(f\colon \mathbf{X} \longrightarrow \mathbf{Y}\\) denotada como \\(f^{-1}\\) por:

\\(f^{-1}(y) = x \iff f(x) = y\\)

Y observamos que los dominios e imágenes entre las funciones se intercalan, es decir, \\(Dom \\ f = Im \\ f^{-1} \land Dom \\ f^{-1} = Im \\ f\\)

Para calcular la función inversa, podemos seguir los siguiente pasos:

1. Reescribir la función como \\(y = f(x)\\)
2. Despejar \\(\mathbf{x}\\)
3. (opcional) intercambiar \\(\mathbf{y}\\) por \\(\mathbf{x}\\)

Por ejemplo:

\\[
  \begin{align}
  & y = \frac{1}{x} \\\\\\
  & x = \frac{1}{y} \\\\\\
  & f^{-1}(y) = \frac{1}{y} \implies f^{-1}(x) = \frac{1}{x}
  \end{align}
\\]