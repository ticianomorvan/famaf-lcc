# Introducción a los algoritmos

<!-- toc -->

Esta materia busca introducir (valga la redundancia) en conceptos básicos de la algoritmia e integrar conceptos fundamentales de la programación, utilizando principalmente el lenguaje de programación [Haskell](https://haskell.org).

Principalmente, se desarrollan los siguientes temas:
- Razonamiento funcional, escritura formal de un algoritmo.
- Listas y razonamiento sobre listas, fuente de problemas y caso de estudio.
- Lógica, herramienta para diseñar y verficar soluciones.

## Aritmética

Permite pensar, a través de una sintaxis, en problemas aritméticos. Tenemos en cuenta diversos elementos:
- Números, a los que llamamos **constantes**
- Letras, a las que llamamos **variables**
- Operadores, que permiten combinar expresiones \\(+, -, *, / \\) y ^. Nota: se deben utilizar paréntesis entre los elementos de un operador.
- Relaciones, que combinan expresiones mediante operadores de relación \\(\neq, =, \leq, <, >, \geq \\)

Por ejemplo, una expresión válida podría ser: \\((3 * 2) + (4 - 5) \\), mientras que una expresión inválida sería: \\((2 +) * 4 - 3 \\), debido a que carece de un segundo valor en la operación \\((2+) \\) y de un paréntesi en la segunda operación \\(4 - 3 \\)

### Fórmulas

A partir de la sintaxis aritmética es posible generar *fórmulas*, utilizando los operadores de relación.

Por ejemplo: \\((2 + 3) \neq (7 * 2) \\)

El resultado de la anterior fórmula es un *booleano*, es decir, un valor de verdad que puede ser *True* (verdadero) o *False* (falso), dependiendo de la expresión, en este caso sería *True*, ya que 5 es distinto de 14.

### Precedencia

La precedencia nos permite "obviar" los paréntesis que hasta ahora eran obligatorios, puesto que entendemos una relación de jerarquía entre los operadores de la siguiente forma:

De mayor a menor precedencia:

- ^ (potencia)
- \\(*, /\\) (producto y división)
- \\(+, -\\) (suma y resta)
- \\(=, <, \leq, >, \geq\\) (operadores de relación)

Por ejemplo, la expresión \\(((2 * 4) + 3) \leq ((3 ^ 4) + (2 * 3))\\), se puede simplificar a \\(2 * 4 + 3 \leq 3 ^ 4 + 2 * 3\\)

## Haskell

Al igual que la sintaxis aritmética, **Haskell** es un lenguaje de programación funcional que funciona a su vez como lenguaje formal, ya que posee una sintaxis estricta con reglas definidas. Es un lenguaje interpretado, puesto que a través de **GHCi** (Glasgow Haskell Compiler), se pueden ejecutar expresiones del lenguaje sin tener que compilar ningún tipo de archivo.

### Algunas anotaciones importantes

#### Tipo de una función

Dentro de GHCi, es posible conocer el tipo de una función o método a través del comando `:type` o su alias `:t`. Por ejemplo, el operador `+`:

```haskell
:t (+)
(+) :: Num a => a -> a -> a
```

Esto nos indica que el operador `+` (determinado por el símbolo `::`) toma dos valores `a` y devuelve otro `a`, que como determina la sintaxis `Num a`, será del tipo numérico, o más específicamente de la clase `Num`.

#### Funciones

Una función es *un conjunto de reglas que indica para cada valor de entrada cual será el resultado*. En Haskell, para definir una función deberemos primero indentificar que tipo tendrá, y luego desarrollar su funcionamiento. Por ejemplo, para una función que tome un nombre como valor de entrada para luego devolver un saludo, podríamos hacerlo de la siguiente forma:

```haskell
greet :: [Char] -> [Char];
greet name = "Hola, " ++ name;
```

Donde podemos ver que definimos que `greet` tomará un valor de entrada del tipo `[Char]` (usado normalmente para cadenas de caracteres) y devolverá otro del mismo tipo. Debajo, vemos la definición propia de la función, donde tomando un argumento `name`, procederemos a unirlo a una frase `"Hola, "`, a través del operador `++`. Es importante entender que el operador `++` es solo válido para este tipo de valores, puesto que no funciona con valores numéricos.