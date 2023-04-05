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

## Funciones

Una funcion es una regla que asigna a cada elemento de un conjunto X un unico elemento f(x) de un conjunto Y.

Para f: X -> Y, El **dominio** (Dom f) es X, mientras que Y es el **conjunto de llegada** (o codominio). f(x) es la imagen de X por f, es decir, a que valor llega un elemento x a partir de f. Por el contrario, la **imagen de f** (Im f) son todos los valores que toma a partir de uno del conjunto X.  

Hablamos de y = f(x) con y como variable **dependiente** y x como variable **independiente**. Para una funcion sin dominio definido, lo entendemos como el conjunto real mas extenso para el cual esta definido.

### Recta

Definimos una recta por y = ax + b, donde los pares (x, y) del plano satisfacen esta ecuacion.

Comprendemos diversas ecuaciones a partir de la anterior:
- x = -b/a, con y = 0
- a = (y2 - y1)/(x2 - x1)
- b = y - ax

Y definimos dos variantes de una recta:
- **Paralela**, aquella que tiene la misma pendiente.
- **Perpendicular**, aquella que tiene pendiente inversa reciproca.

### Desplazamientos
Con **c > 0**
- Verticales:
  - Hacia arriba: f(x) + c
  - Hacia abajo: f(x) - c
- Horizontales:
  - Hacia la izquierda: f(x + c)
  - Hacia la derecha: f(x - c)

### Estiramientos y reflexiones
Un estiramiento se da con **c >= 1**, mientras que una compresion se da con **c < 0**. Ambos comparten las formulas para el plano vertical y horizontal:
- Vertical: c * f(x)
- Horizontal: f(c * x)

Una reflexion, por otro lado, puede darse a traves de las siguientes formulas:
- Vertical: -f(x)
- Horizontal: f(-x)

### Funciones pares e impares
Una funcion par es aquella que satisface que f(x) = -f(x), mientras que una impar satisface que f(x) = -f(-x) => -f(x) = f(-x). La funcion par es simetrica con respecto al eje x, mientras que la impar es simetrica con respecto al origen.

### Operaciones con funciones
- Suma: f(x) + g(x) = (f + g)(x)
- Multiplicacion: f(x) * g(x) = f * g * x
- Division: f/g = f(x)/g(x)
