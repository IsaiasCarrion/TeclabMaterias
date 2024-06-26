# PROCESAMIENTO DE DATOS: MODULO 2

# **Manipulación de datos**

---

### **¿Qué es la manipulación de datos?**

La manipulación de datos es el proceso de cambiar o alterar datos para hacerlos más legibles y organizados. Por ejemplo, puede ordenar los datos alfabéticamente para acelerar el proceso de búsqueda de información útil. Otro ejemplo de manipulación de datos es la gestión de sitios web. Los propietarios de sitios web pueden utilizar los registros del servidor web para localizar las páginas web más visitadas, las fuentes de tráfico y mucho más. De manera similar, los corredores de bolsa utilizan la manipulación de datos para pronosticar las tendencias del mercado de valores.

### **¿Por qué utilizar la manipulación de datos?**

Las empresas usan datos para predecir tendencias, comprender el comportamiento de los clientes, aumentar la productividad, reducir costos, etc. mediante la manipulación de datos. Otros beneficios adicionales incluyen:Consistencia de formato: Los datos organizados de manera unificada y ordenada ayudan a los usuarios comerciales a tomar mejores decisiones.

### **¿Qué son las herramientas de manipulación de datos?**

Las herramientas de manipulación de datos le permiten modificar datos para facilitar su lectura u organización. Estas herramientas ayudan a identificar patrones en sus datos que de otro modo no serían obvios. Por ejemplo, puede organizar un registro de datos en orden alfabético utilizando una herramienta de manipulación de datos para que las entradas discretas sean más fáciles de encontrar.La gente a menudo confunde manipulación de datos con ETL (*Extraction Transformation and Load*) y otras técnicas de transformación. Sin embargo, la manipulación de datos implica ordenar, reorganizar y mover datos sin cambiarlos esencialmente. Incluye operaciones para adaptar los datos en la forma necesaria para mostrar información o alimentar y entrenar un modelo analítico.El propósito clave de la manipulación de datos es alterar la relación (ya sea lógica o física) que un elemento de datos tiene con otro, no los datos en sí. Las operaciones comunes utilizadas para la manipulación de datos incluyen:

- Filtrado de filas y columnas.
- Agregación.
- Combinación.
- Concatenación.
- Manipulación de cadenas.
- Clasificación.
- Regresión.
- Fórmulas matemáticas.

ETL (Extract, Transform and Load), por otro lado, tiene un propósito diferente. Implica extraer datos del sistema de origen y hacer que sea compatible con el sistema de destino antes de escribir en él.

### **¿Por qué necesita herramientas de manipulación de datos?**

La manipulación de datos es una tarea crítica en la optimización de procesos. Transforma los datos en una forma utilizable que se puede utilizar más para generar información, como el análisis de datos financieros, el comportamiento de los clientes y la realización de análisis de tendencias.Las herramientas de manipulación de datos se utilizan ampliamente durante la integración para hacer que los datos sean compatibles con el sistema de destino. Por ejemplo, los usuarios asociados con la contabilidad a menudo manipulan datos sin procesar adquiridos de proveedores y marketing para comprender los precios de los productos, las tendencias de ventas o los posibles requisitos fiscales. Del mismo modo, los expertos del mercado de valores pueden aprovechar los conjuntos de datos para pronosticar las tendencias del mercado, lo que les permite administrar sus carteras de inversión en consecuencia.Estos son solo algunos casos de uso de manipulación de datos. Algunas de las otras formas en que la manipulación puede ser beneficiosa para las organizaciones incluyen:

- **Consistencia de los datos**: Un formato de datos coherente facilita la organización, la lectura y el análisis de datos. Cuando los datos provienen de fuentes dispares, el usuario debe transformarlos y manipularlos para crear un formato unificado. Después de estandarizar el formato, es más fácil escribir datos en el sistema empresarial o utilizarlos para generar informes.
- **Proyección de datos:** Como empresa, no se puede negar la importancia de los datos cuando se trata de inteligencia empresarial (BI). Realizar un análisis exhaustivo de los datos es vital para las empresas, especialmente cuando se trata de inversiones. Todas las empresas utilizan datos del pasado para planificar el futuro. Las herramientas de manipulación de datos facilitan la creación de proyecciones, especialmente en el sector financiero, donde depende de los resultados de sus inversiones pasadas para consideraciones futuras.
- **Generación de valor:** La manipulación de datos le permite actualizar, modificar, eliminar e ingresar datos en una base de datos. Esto significa que puede aprovechar los datos para obtener información detallada y tomar mejores decisiones comerciales.
- **Eliminación de datos redundantes:** A menudo, los datos que provienen de los sistemas de origen incluyen información redundante, errónea o no deseada. Hacer que estos datos sean útiles requiere ejecutarlos a través de controles de calidad y aplicar filtros de limpieza para extraer la información esencial para su empresa. Al utilizar la manipulación de datos, puede limpiar rápidamente sus datos para que pueda filtrar los registros que importan.
- **Interpretación de datos:** Cuando se trata de datos complejos que involucran múltiples formatos y condiciones comerciales, es casi imposible entenderlos sin manipulación. Debe tener la capacidad de visualizar datos y modificarlos para convertirlos en información valiosa y comprensible. Una herramienta de manipulación de datos podría resolver este problema convirtiendo los datos al formato deseado e integrándolos con diferentes herramientas para mejorar la experiencia visual. Esto facilita que los usuarios comprendan y consuman datos.
- **Panorama histórico:** acceder rápidamente a los datos de proyectos anteriores puede ayudar a una organización a tomar decisiones con respecto a la proyección de la fecha límite, la productividad del equipo, la asignación de presupuesto, etc.
- **Eficiencia mejorada:** al tener datos más organizados, una empresa puede aislar e incluso reducir las variables externas para contribuir a la eficiencia general de la empresa.


### El objeto array en NumPy

Un array (también conocido como arreglo o matriz) es una estructura de datos que almacena una colección ordenada de elementos del mismo tipo. Es similar a una lista, pero con la ventaja de que puede almacenar múltiples valores en una sola variable, lo que lo hace más eficiente para trabajar con grandes cantidades de datos.

**¿Cómo se crean los arrays en Python?**

Los arrays en Python se crean utilizando la función np.array() de la biblioteca NumPy. Esta función recibe como argumento una lista o tupla y devuelve un array NumPy.

Ejemplo de un array en Python:

```python
import numpy as np

# Creamos un array bidimensional con listas anidadas
array = np.array([[[1, 2, 3], [4, 5, 6]], [[7, 8, 9], [10, 11, 12]]])

# Imprimimos el array
print(array)

```

**¿Qué dimensiones puede tener un array?**

El número de dimensiones de un array depende de la cantidad de listas o tuplas anidadas en la estructura original.

- **Una lista:** Crea un array unidimensional (vector).
- **Dos listas:** Crea un array bidimensional (matriz).
- **Tres listas:** Crea un array tridimensional (cubo).
- **Más listas:** Crea un array con la cantidad de dimensiones correspondiente al número de listas anidadas.

**¿Qué tipo de datos pueden almacenar los arrays?**

Los elementos de un array deben ser del mismo tipo. El tipo de datos se infiere automáticamente a partir de los elementos de la lista o tupla original.

**¿Cómo se consulta el tamaño de un array?**

El tamaño de un array se puede consultar utilizando el atributo shape(). Este atributo devuelve una tupla con las dimensiones del array.

**Ejemplo:**

```python
# Obtenemos el tamaño del array
array_size = array.shape

# Imprimimos el tamaño
print(array_size)

```

### **Las dimensiones de un *array* también se conocen como ejes**

```python
>>> # Array de una dimensión

>>> a1 = np.array([1, 2, 3])

>>> print(a1)

[1 2 3]

# Array de dos dimensiones

a2 = np.array([[1, 2, 3], [4, 5, 6]])

print(a2)

[[1 2 3]

[4 5 6]]

# Array de tres dimensiones

a3 = np.array([[[1, 2, 3], [4, 5, 6]], [[7, 8, 9], [10, 11, 12]]])

print(a3)

[[[ 1 2 3]

[ 4 5 6]]

[[ 7 8 9]

[10 11 12]]].

```

**np.empty(dimensiones):** crea y devuelve una referencia a un *array* vacío con las dimensiones especificadas en la tupla dimensiones.**np.zeros(dimensiones):** crea y devuelve una referencia a un *array* con las dimensiones especificadas en la tupla dimensiones cuyos elementos son todos ceros.
**np.ones(dimensiones):** crea y devuelve una referencia a un *array* con las dimensiones especificadas en la tupla dimensiones cuyos elementos son todos unos.
**np.full(dimensiones, valor):** crea y devuelve una referencia a un *array* con las dimensiones especificadas en la tupla dimensiones cuyos elementos son todos valor.
**np.identity(n):** crea y devuelve una referencia a la matriz identidad de dimensión n.
**np.arange(inicio, fin, salto):** Crea y devuelve una referencia a un *array* de una dimensión cuyos elementos son la secuencia desde inicio hasta fin tomando valores cada salto.
**np.linspace(inicio, fin, n):** crea y devuelve una referencia a un *array* de una dimensión cuyos elementos son la secuencia de n valores equidistantes desde inicio hasta fin.
**np.random.random(dimensiones):** crea y devuelve una referencia a un *array* con las dimensiones especificadas en la tupla dimensiones cuyos elementos son aleatorios.+

**Atributos de un *array*a.ndim:** Devuelve el número de dimensiones del *array* a.**a.shape:** Devuelve una tupla con las dimensiones del *array* a.**a.size:** Devuelve el número de elementos del *array* a.**a.dtype:** Devuelve el tipo de datos de los elementos del *array* a.

### Acceso a los elementos de un array en Python

Se puede acceder a los elementos de un array utilizando la notación de indexación. La indexación comienza en 0, por lo que el primer elemento tiene el índice 0, el segundo elemento tiene el índice 1, y así sucesivamente.

```python
import numpy as np

# Creamos un array
array = np.array([1, 2, 3, 4, 5])

# Accedemos al primer elemento (índice 0)
primer_elemento = array[0]
print(primer_elemento)  # Salida: 1

# Accedemos al último elemento (índice -1)
ultimo_elemento = array[-1]
print(ultimo_elemento)  # Salida: 5

# Accedemos a los tres primeros elementos
tres_primeros = array[0:3]
print(tres_primeros)  # Salida: [1 2 3]

# Accedemos a todos los elementos excepto el primero y el último
resto_elementos = array[1:-1]
print(resto_elementos)  # Salida: [2 3 4]

# Acceso a elementos con pasos
# array[inicio:fin:paso]
# Accedemos a los elementos pares del array
pares = array[0::2]
print(pares)  # Salida: [1 3 5]

# Acceso a elementos de un array bidimensional
# array[fila, columna]
# Creamos un array bidimensional
array_2d = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

# Accedemos al elemento de la fila 1, columna 2
elemento = array_2d[1, 2]
print(elemento)  # Salida: 6

# Acceso a elementos de un array multidimensional
# array[dimension1, dimension2, ..., dimensionN]
# Creamos un array tridimensional
array_3d = np.array([[[1, 2, 3], [4, 5, 6]], [[7, 8, 9], [10, 11, 12]]])

# Accedemos al elemento de la dimensión 0, fila 1, columna 2
elemento = array_3d[0, 1, 2]
print(elemento)  # Salida: 6

```

### Operaciones numéricas con arreglos

### **¿Qué tipos de datos puede contener un *array* en NumPy?**

Básicamente, los datos (elementos) que puede contener un *array* NumPy son los siguientes:

- Cadenas de caracteres.
- Números enteros de distintos tamaños.
- Números reales.
- Booleanos.

### Operaciones matemáticas con arrays

Las operaciones matemáticas con arrays en Python se realizan utilizando los mismos operadores que con números escalares. Sin embargo, cuando se opera con arrays, las operaciones se realizan **elemento a elemento**. Esto significa que la operación se aplica a cada par de elementos correspondientes en los arrays.

```python
import numpy as np

# Creamos dos arrays
array1 = np.array([1, 2, 3])
array2 = np.array([4, 5, 6])

# Sumamos los arrays
suma = array1 + array2
print(suma)  # Salida: [5 7 9]

# Restamos los arrays
resta = array1 - array2
print(resta)  # Salida: [-3 -3 -3]

# Multiplicamos los arrays
multiplicacion = array1 * array2
print(multiplicacion)  # Salida: [4 10 18]

# Dividimos los arrays
division = array1 / array2
print(division)  # Salida: [0.25  0.4  0.5]

# División entera
division_entera = array1 // array2
print(division_entera)  # Salida: [0 0 0]

# Potenciación
potenciacion = array1 ** array2
print(potenciacion)  # Salida: [1 32 216]

```

**Operaciones con un escalar:**

Las operaciones matemáticas también se pueden realizar entre un array y un escalar. En este caso, la operación se aplica a **cada elemento del array** utilizando el valor escalar.

```python
import numpy as np

# Creamos un array y un escalar
array = np.array([1, 2, 3])
escalar = 5

# Sumamos el escalar a cada elemento del array
suma_escalar = array + escalar
print(suma_escalar)  # Salida: [6 7 8]

# Multiplicamos el escalar por cada elemento del array
multiplicacion_escalar = array * escalar
print(multiplicacion_escalar)  # Salida: [5 10 15]

```

**Funciones matemáticas:**

NumPy también proporciona una amplia gama de funciones matemáticas que se pueden aplicar a arrays. Algunas de las funciones más comunes incluyen:

- np.sin()
- np.cos()
- np.tan()
- np.log()
- np.exp()
- np.sqrt()
- np.abs()
- np.random()
- np.round()
- np.floor()
- np.ceil()

```python
import numpy as np

# Creamos un array
array = np.array([1, 2, 3])

# Calculamos el seno de cada elemento del array
senos = np.sin(array)
print(senos)  # Salida: [0.84147098 0.90631781 0.98994949]

# Calculamos la raíz cuadrada de cada elemento del array
raices_cuadradas = np.sqrt(array)
print(raices_cuadradas)  # Salida: [1. 1.41421356 1.73205081]

```

### **Filtrado de elementos de un *array***

El filtrado de elementos de un array en Python consiste en seleccionar un subconjunto de elementos del array que cumplen con una condición específica.

**Función filter():**

La función filter() de la biblioteca estándar de Python se utiliza para filtrar elementos de un iterable (como un array) en base a una función de prueba. La función devuelve un nuevo iterador que contiene solo los elementos para los que la función de prueba devuelve True.

```python
# filter(funcion_prueba, iterable)
import numpy as np

# Creamos un array
array = np.array([1, 2, 3, 4, 5, 6])

# Definimos la función de prueba
def es_par(x):
  return x % 2 == 0

# Filtramos el array para obtener solo los números pares
pares = filter(es_par, array)

# Convertimos el iterador filtrado en una lista
lista_pares = list(pares)

print(lista_pares)  # Salida: [2 4 6]

```

Donde:

- funcion_prueba es una función que recibe un elemento del iterable como argumento y devuelve True si el elemento debe incluirse en el resultado filtrado, o False en caso contrario.
- iterable es el array del que se desea filtrar los elementos.

**Comprensión de listas:**

Las comprensiones de listas en Python proporcionan una forma concisa de crear nuevas listas a partir de iterables existentes. Se pueden utilizar para filtrar elementos de un array de manera similar a la función filter().

```python
# [elemento for elemento in iterable if condicion]
import numpy as np

# Creamos un array
array = np.array([1, 2, 3, 4, 5, 6])

# Filtramos el array para obtener solo los números pares
pares = [x for x in array if x % 2 == 0]

print(pares)  # Salida: [2 4 6]

```

Donde:

- elemento es la variable que representa cada elemento del iterable.
- iterable es el array del que se desea filtrar los elementos.
- condicion es una expresión booleana que debe ser True para que el elemento se incluya en la lista resultante.

**Indexación booleana:**

La indexación booleana en Python permite seleccionar elementos de un array utilizando una expresión booleana como índice. La expresión booleana se evalúa para cada elemento del array, y solo los elementos para los que la expresión devuelve True se incluyen en el resultado.

```python
# array[condicion]
import numpy as np

# Creamos un array
array = np.array([1, 2, 3, 4, 5, 6])

# Filtramos el array para obtener solo los números pares
pares = array[array % 2 == 0]

print(pares)  # Salida: [2 4 6]

```

Donde:

- array es el array del que se desea filtrar los elementos.
- condicion es una expresión booleana que debe ser True para que el elemento se incluya en el resultado.

### **Comparación de arrays con NumPy**

---

`numpy.array_equal()`, permite comparar dos arrays para determinar si son iguales en términos de forma y elementos.

**Función `numpy.array_equal()`:**

- La función `numpy.array_equal(a1, a2, equal_nan=False)` toma dos arrays `a1` y `a2` como entrada y devuelve `True` si ambos arrays tienen la misma forma y elementos.
- Si los arrays tienen diferentes formas o elementos, la función devuelve `False`.
- El parámetro opcional `equal_nan` indica si se deben considerar iguales los valores `NaN` (Not a Number). Por defecto, `equal_nan` es `False`, lo que significa que los valores `NaN` se consideran diferentes.

```python
import numpy as np

a1 = np.array([1, 2, 4, 6, 7])
a2 = np.array([1, 3, 4, 5, 7])

print(np.array_equal(a1, a1))  # True
print(np.array_equal(a1, a2))  # False

```

**Atributo `shape`:**

- El atributo `shape` de un array NumPy devuelve una tupla que indica el tamaño del array.
- Cada elemento de la tupla representa el tamaño de una dimensión del array.
- Por ejemplo, un array bidimensional con 2 filas y 6 columnas tendría un `shape` de `(2, 6)`.

**Manipulaciones de arrays:**

NumPy proporciona diversas funciones para manipular arrays, incluyendo:

- **Indexación:** Permite acceder a elementos específicos de un array utilizando índices o subíndices.
- **Segmentación:** Permite extraer subconjuntos de un array en función de condiciones específicas.
- **Remodelación:** Permite cambiar la forma de un array sin modificar sus elementos.
- **Unión y división:** Permite combinar o dividir arrays en función de diferentes criterios.

```python
a = np.array([[1, 24, 37], [43, 15, 68]])

print(a[0, 1])  # 24 (elemento en la fila 0, columna 1)
print(a[1])  # [43 15 68] (fila 1 completa)

```

## Operaciones complejas en arreglos de NumPy

---

NumPy proporciona diversas funciones para realizar operaciones matemáticas complejas en arrays multidimensionales. Estas operaciones van más allá de la simple aplicación de sintaxis aritmética básica.

**Ejemplos de operaciones matemáticas:**

- **Raíz cuadrada:** `np.sqrt(a)` calcula la raíz cuadrada de cada elemento en el array `a`.
    - Ejemplo: `np.sqrt(np.array([49, 81, 144, 16]))` = `array([ 7., 9., 12., 4.])`

```python
import numpy as np

a = np.array([49, 81, 144, 16])

raices_cuadradas = np.sqrt(a)

print(raices_cuadradas)  # Salida: array([ 7.  9. 12.  4.])
```

- **Funciones trigonométricas:**
    - `np.sin(arr)` calcula el seno trigonométrico de cada valor en el array `arr`.
    - `np.cos(arr)` calcula el coseno trigonométrico de cada valor en el array `arr`.

```python
import numpy as np

angulos = np.array([0, np.pi/2, np.pi])

senos = np.sin(angulos)

print(senos)  # Salida: array([ 0.  1.  0.])
```

- **Logaritmo:**
    - `np.log(arr)` calcula el logaritmo en base diez de cada valor en el array `arr`.

```python
import numpy as np

valores = np.array([1, 10, 100, 1000])

logaritmos = np.log10(valores)

print(logaritmos)  # Salida: array([ 0.  1.  2.  3.])
```

**Operaciones estadísticas:**

- **Media:** `np.mean(arr)` calcula la media aritmética de los elementos en el array `arr`.
    - Ejemplo: `np.mean(np.array([5, 10.4, 4, 3, 6.6]))` = `5.8`
    - Cálculo de porcentajes: `np.mean(arr > valor)` indica el porcentaje de elementos en `arr` que son mayores que `valor`.

```python
import numpy as np

datos = np.array([5, 10.4, 4, 3, 6.6])

media = np.mean(datos)

print(media)  # Salida: 5.8
```

- **Mediana:** `np.median(arr)` calcula la mediana de los elementos en el array `arr` (valor central cuando ordenado).
    - Ejemplo: `np.median(np.array([1, 1, 2, 3, 4, 5, 5]))` = `3.0`
- **Desviación estándar:** `np.std(arr)` calcula la desviación estándar de los elementos en el array `arr`.
    - Ejemplo: `np.std(np.array([65, 36, 52, 91, 63, 79]))` = `17.716909687891082`

```python
import numpy as np

numeros_ordenados = np.array([1, 1, 2, 3, 4, 5, 5])

mediana = np.median(numeros_ordenados)

print(mediana)  # Salida: 3.0
```

**Operaciones lógicas:**

- Se realizan elemento a elemento en los arrays.
- Comparan valores y devuelven `True` o `False`.
- Ejemplos:
    - `np.greater(a, b)`: `True` si cada elemento en `a` es mayor que el correspondiente en `b`.
    - `np.less_equal(a, b)`: `True` si cada elemento en `a` es menor o igual que el correspondiente en `b`.
    - `np.logical_and(a, b)`: `True` si ambos elementos en `a` y `b` son `True`.
    - `np.logical_xor(a, b)`: `True` si solo uno de los elementos en `a` o `b` es `True`, pero no ambos.

    ```python
    import numpy as np

    a = np.array([5, 2, 3])
    b = np.array([2, 3, 2])

    mayores = np.greater(a, b)

    print(mayores)  # Salida: array([ True  False  True])
    ```


**Operaciones adicionales:**

- `np.maximum(a, b)`: Devuelve el máximo elemento a elemento entre `a` y `b`.
- `np.minimum(a, b)`: Devuelve el mínimo elemento a elemento entre `a` y `b`.

## **Funciones trigonométricas con NumPy**

---

### 1. Funciones trigonométricas

- **`np.sin(x)`:** Calcula el seno del ángulo en radianes representado por cada elemento en el array `x`.
    - Ejemplo: `np.sin(np.array([0, np.pi/2, np.pi]))` = `array([0. 1. 0.])`
- **`np.cos(x)`:** Calcula el coseno del ángulo en radianes representado por cada elemento en el array `x`.
    - Ejemplo: `np.cos(np.array([0, np.pi/2, np.pi]))` = `array([1. 0. -1.])`
- **`np.tan(x)`:** Calcula la tangente del ángulo en radianes representado por cada elemento en el array `x`.
    - Ejemplo: `np.tan(np.array([0, np.pi/4, np.pi/2]))` = `array([0. 1. tan(pi/2)])`
- **`np.arcsin(x)`:** Calcula el arcoseno (inverso del seno) de cada elemento en el array `x` (entre -1 y 1).
    - Ejemplo: `np.arcsin(np.array([0, 1/2, 1]))` = `array([0. 0.5 1.57079633])`
- **`np.arccos(x)`:** Calcula el arcocoseno (inverso del coseno) de cada elemento en el array `x` (entre 0 y pi).
    - Ejemplo: `np.arccos(np.array([1, 0, -1]))` = `array([0. 1.57079633 3.14159265])`
- **`np.arctan(x)`:** Calcula la arcotangente (inverso de la tangente) de cada elemento en el array `x`.
    - Ejemplo: `np.arctan(np.array([1, 0, -1]))` = `array([0.78539816 0. -1.57079633])`
- **`np.deg2rad(x)`:** Convierte ángulos de grados sexagesimales a radianes.
    - Ejemplo: `np.deg2rad(np.array([90, 180, 270]))` = `array([1.57079633 3.14159265 4.71238898])`

### 2. Cortes

- **Cortes simples:**
    - `array[start:end]`: Recupera elementos desde `start` (inclusivo) hasta `end` (exclusivo).
    - Ejemplo: `a[2:5]` recupera `[3, 4]`.
- **Cortes con paso:**
    - `array[start:end:step]`: Recupera elementos con un intervalo de `step`.
    - Ejemplo: `a[0:8:2]` recupera `[0, 2, 4, 6]`.
- **Cortes con indexación booleana:**
    - `array[condicion]`: Recupera elementos que satisfacen la condición booleana.
    - Ejemplo: `a[a > 50]` recupera `[81, 144]`.

    ```python
    import numpy as np

    a = np.array([144, 81, 16, 49])

    # Raíces cuadradas
    raices_cuadradas = np.sqrt(a)
    print("Raíces cuadradas:", raices_cuadradas)

    # Senos (convertir a radianes primero)
    radianes = np.deg2rad(a)
    senos = np.sin(radianes)
    print("Senos:", senos)

    # Cosenos (convertir a radianes primero)
    cosenos = np.cos(radianes)
    print("Cos

    ```

    ## **Manipulación y Exploración de Datos**

    ---

    ### Manipulación de datos con Pandas

    Pandas es una librería de Python para el análisis y manipulación de datos. Se basa en NumPy y ofrece estructuras de datos potentes y flexibles para trabajar con datos tabulares.

    **Estructuras de datos:**

    - **Series:** Representa un vector unidimensional con etiquetas (índices) y datos de un único tipo.
        - Ejemplo: `s = pd.Series([10, 20, 30], index=['a', 'b', 'c'])`
    - **DataFrame:** Representa una tabla bidimensional con filas (registros) y columnas (variables). Cada columna es un Series.
        - Ejemplo: `df = pd.DataFrame({'nombre': ['Ana', 'Beto', 'Carlos'], 'edad': [25, 30, 22], 'ciudad': ['Buenos Aires', 'Córdoba', 'Rosario']})`

    **Características:**

    - **Carga de datos:** Facilita la lectura de datos desde diversos formatos (.csv, .xls, .json, SQL, etc.).
    - **Manipulación:** Permite seleccionar, filtrar, ordenar, agrupar y transformar datos con facilidad.
    - **Análisis:** Ofrece funciones para calcular estadísticas descriptivas, realizar análisis de series temporales y crear visualizaciones.

    **Ventajas:**

    - **Potente y flexible:** Maneja grandes conjuntos de datos de forma eficiente.
    - **Facilidad de uso:** Sintaxis intuitiva y similar a Python.
    - **Amplia comunidad:** Gran cantidad de recursos disponibles y soporte de la comunidad.

    ```python
    import pandas as pd

    # Lectura del archivo CSV en un DataFrame
    df = pd.read_csv("datos.csv")

    # Selección de una columna
    nombres = df["nombre"]

    # Filtrado de filas
    mayores_30 = df[df["edad"] > 30]

    # Agrupamiento por una columna
    por_ciudad = df.groupby("ciudad")["edad"].mean()

    # Cálculo de una estadística descriptiva
    promedio_edad = df["edad"].mean()
    ```

    ### Series y *DataFrames* en Pandas

    ---

    **Series:** La estructura de datos fundamental en Pandas, similar a una columna en Excel.

    **Componentes:**

    - **Índice:** Etiquetas únicas y ordenadas (generalmente).
    - **Datos:** Valores de un único tipo (números, cadenas, etc.).

    ```python
    import pandas as pd

    # Ejemplo 1: Lista
    s = pd.Series([10, 20, 30])

    # Ejemplo 2: Diccionario
    d = {"a": 1, "b": 2, "c": 3}
    s = pd.Series(d)

    # Ejemplo 3: Especificando índice
    s = pd.Series([5, 7, 9], index=["rojo", "verde", "azul"])
    ```

    **Acceso a elementos:**

    - `s[indice]`
    - `s.loc[indice]` (acceso por etiqueta)
    - `s.iloc[posicion]` (acceso por posición)

    **Operaciones:**

    - Aritméticas (+, -, *, /)
    - Comparaciones (==, !=, <, >, <=, >=)
    - Funciones de agregación (mean(), sum(), max(), min())
    - Aplicación de funciones personalizadas (`s.apply(funcion)`)

    ```python
    import pandas as pd

    # Creación de una serie
    ciudades = pd.Series(["Buenos Aires", "Córdoba", "Rosario"], index=["BA", "CBA", "ROS"])

    # Acceso a elementos
    print(ciudades["BA"])  # Salida: Buenos Aires
    print(ciudades.loc["CBA"])  # Salida: Córdoba
    print(ciudades.iloc[1])  # Salida: Córdoba

    # Operaciones
    poblacion = pd.Series([3000000, 1500000, 1200000], index=["BA", "CBA", "ROS"])
    mayor_poblacion = ciudades[poblacion > 1800000]
    print(mayor_poblacion)  # Salida: Series con ciudades que superan 1.8M de habitantes
    ```

    ### ***DataFrame* en Pandas**

    ---

    Un `DataFrame` en Pandas es una estructura de datos bidimensional similar a una hoja de cálculo de Excel. Está compuesto por filas (registros) y columnas (variables). Cada columna es un objeto `Series`.

    ```python
    import pandas as pd

    # Ejemplo 1: Diccionario
    datos = {'nombre': ['Ana', 'Beto', 'Carlos'], 'edad': [25, 30, 22], 'ciudad': ['Buenos Aires', 'Córdoba', 'Rosario']}
    df = pd.DataFrame(datos)

    # Ejemplo 2: Lista de listas
    datos = [[10, 11, 12], [20, 21, 22], [30, 31, 32]]
    df = pd.DataFrame(datos)
    ```

    **Acceso a elementos:**

    - `df['columna']`: Accede a una columna por nombre.
    - `df.loc[fila, 'columna']`: Accede a un elemento por índice de fila y nombre de columna.
    - `df.iloc[fila, columna]`: Accede a un elemento por índice de fila y posición de columna.

    **Operaciones:**

    - **Selección:** `df[condicion]`, `df.loc[condicion]`, `df.iloc[condicion]`.
    - **Filtrado:** `df[columna] > valor`, `df['columna'].isin(['valor1', 'valor2'])`.
    - **Ordenación:** `df.sort_values(by='columna')`, `df.sort_index(ascending=False)`.
    - **Agrupación:** `df.groupby('columna')['variable'].mean()`.
    - **Estadísticas:** `df['columna'].mean()`, `df.describe()`.
    - **Uniones:** `pd.concat([df1, df2], axis=1, join='inner')`.

    ```python
    import pandas as pd

    # Creación de un DataFrame
    df = pd.DataFrame({'nombre': ['Ana', 'Beto', 'Carlos'], 'edad': [25, 30, 22], 'ciudad': ['Buenos Aires', 'Córdoba', 'Rosario']})

    # Selección de una columna
    nombres = df['nombre']

    # Filtrado de filas
    mayores_30 = df[df['edad'] > 30]

    # Agrupamiento por una columna
    por_ciudad = df.groupby('ciudad')['edad'].mean()

    # Cálculo de una estadística descriptiva
    promedio_edad = df['edad'].mean()
    ```

    ### Manejo de archivos CSV

    ---

    - Se utiliza la función `pd.read_csv()` para cargar el contenido de un archivo CSV en un DataFrame.
    - Sintaxis básica: `df = pd.read_csv('archivo.csv')`
    - Argumentos opcionales:
        - `sep`: Carácter delimitador (por defecto, coma).
        - `encoding`: Codificación de caracteres del archivo.
        - `index_col`: Columna que se usará como índice del DataFrame.
        - `header`: Indica si la primera fila contiene nombres de columna (por defecto, True).

    ```python
    import pandas as pd

    # Lectura de un archivo CSV con comas como separador y encabezados en la primera fila
    df = pd.read_csv('datos.csv')

    # Acceso a los datos
    print(df['columna1'])
    print(df.loc[0, 'columna2'])
    ```

    **Escritura de archivos CSV:**

    - Se utiliza el método `to_csv()` de un DataFrame para guardarlo en un archivo CSV.
    - Sintaxis básica: `df.to_csv('archivo.csv')`
    - Argumentos opcionales:
        - `sep`: Carácter delimitador (por defecto, coma).
        - `index`: Incluir o no el índice en el archivo (por defecto, True).
        - `header`: Incluir o no los nombres de columna en la primera fila (por defecto, True).

    ```python
    import pandas as pd

    # Creación de un DataFrame
    df = pd.DataFrame({'columna1': [1, 2, 3], 'columna2': ['a', 'b', 'c']})

    # Guardado en un archivo CSV con punto y coma como separador
    df.to_csv('datos.csv', sep=';', index=False)
    ```

    ### Conexión con bases de datos tipo SQL

    ---

    Pandas y SQL son herramientas poderosas para trabajar con datos, pero sirven para diferentes propósitos. Pandas se utiliza principalmente para el análisis y la manipulación de datos en memoria, mientras que SQL se utiliza para interactuar con bases de datos relacionales.

    **Lectura de datos desde SQL a Pandas:**

    - Se utiliza la función `pd.read_sql()` para cargar datos de una tabla o consulta SQL en un DataFrame.
    - Requiere una conexión a la base de datos y la especificación de la tabla o consulta.

    **Consideraciones:**

    - La interacción entre Pandas y SQL requiere conocimientos básicos de ambos lenguajes.
    - Pandas ofrece mayor flexibilidad para el análisis y la manipulación de datos, mientras que SQL es más eficiente para el manejo de grandes volúmenes de datos en bases de datos.

```python
import pandas as pd
from sqlalchemy import create_engine

# Conexión a la base de datos
engine = create_engine('mysql+pymysql://usuario:password@host:puerto/base_datos')

# Lectura de datos de una tabla
df = pd.read_sql('SELECT * FROM mi_tabla', engine)

# Lectura de datos con una consulta SQL
df = pd.read_sql('SELECT nombre, edad FROM mi_tabla WHERE edad > 18', engine)
```

**Escritura de datos desde Pandas a SQL:**

- Se utiliza el método `to_sql()` de un DataFrame para insertar o actualizar datos en una tabla SQL.
- Requiere una conexión a la base de datos y la especificación del nombre de la tabla.

```python
import pandas as pd
from sqlalchemy import create_engine

# Conexión a la base de datos
engine = create_engine('mysql+pymysql://usuario:password@host:puerto/base_datos')

# Creación de un DataFrame
df = pd.DataFrame({'nombre': ['Ana', 'Beto', 'Carlos'], 'edad': [25, 30, 22]})

# Inserción de datos en una tabla existente
df.to_sql('mi_tabla', engine, if_exists='append', index=False)

# Actualización de datos en una tabla existente (reemplaza registros con la misma clave primaria)
df.to_sql('mi_tabla', engine, if_exists='replace', index=False)
```