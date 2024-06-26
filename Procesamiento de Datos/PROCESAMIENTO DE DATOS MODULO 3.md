# PROCESAMIENTO DE DATOS: MODULO 3

### Ordenamiento de Datos

---

La ordenación de datos es un proceso fundamental dentro del procesamiento de datos. **Necesitamos establecer criterios de ordenamiento de los datos para darle un sentido y claridad a un gran volumen de datos iniciales.** Por ejemplo, organizamos los datos en orden alfabético o en un orden numérico ascendente o descendente o podemos ordenar una columna que enumere los valores de las ventas de un producto en orden descendente, para observar las ventas del producto de la más alta a la más baja.En programación, se utilizan métodos de ordenamiento. Por ejemplo, la operación de arreglar los registros de una tabla en algún orden secuencial de acuerdo con un criterio de ordenamiento. El ordenamiento puede realizarse basándose en el valor de algún campo en un registro.En Python, una forma que tenemos para ordenar datos es a través de Pandas, gracias a sus *DataFrames* y series.

> Las principales características de dichas librerías son:
> - Define nuevas estructuras de datos basadas en los *arrays* de la librería NumPy pero con nuevas funcionalidades.
> - Permite leer y escribir fácilmente ficheros en formato CSV, Excel y bases de datos SQL.
> - Permite acceder a los datos mediante índices o nombres para filas y columnas.
> - Ofrece métodos para reordenar, dividir y combinar conjuntos de datos.
> - Permite trabajar con series temporales.
> - Realiza todas estas operaciones de manera muy eficiente

### Orden de Datos

---

Ordenar datos con Pandas

Pandas es una librería fundamental para el análisis de datos en Python. Ofrece la clase `DataFrame` para almacenar datos en tablas similares a bases de datos. Este módulo se centra en técnicas para ordenar datasets para análisis posteriores.

**Ordenar una lista:**

- `sort()`: Ordena la lista en su lugar. Acepta argumentos opcionales `key` (función para ordenar) y `reverse` (orden ascendente o descendente).
- `sorted()`: Devuelve una nueva lista ordenada. Acepta argumentos opcionales `key`, `reverse` y otros.

```python
# sort()
lista = [5, 2, 3, 1, 4]
lista.sort()
print(lista)  # Salida: [1, 2, 3, 4, 5]

# sorted()
sorted_lista = sorted([5, 2, 3, 1, 4])
print(sorted_lista)  # Salida: [1, 2, 3, 4, 5]
```

**Ordenar un diccionario:**

- `sorted()` devuelve una lista de claves ordenadas.

```python
diccionario = {3: "tres", 1: "uno", 2: "dos"}
print(sorted(diccionario))  # Salida: [1, 2, 3]
```

**Diferencias entre `sort()` y `sorted()`:**

- `sort()` modifica la lista original, mientras que `sorted()` crea una nueva.
- `sort()` solo acepta listas, mientras que `sorted()` acepta cualquier iterable.

**Ordenar con una función `key`:**

- Permite definir un criterio de ordenamiento personalizado.

```python
nombres = ['Carolina', 'Luis', 'Leo', 'Jackeline', 'Penelope']
nombres.sort(key=len)  # Ordena por longitud de nombre
print(nombres)  # Salida: ['Leo', 'Luis', 'Carolina', 'Penelope', 'Jackeline']
```

**Argumento `reverse`:**

- Ordena en orden inverso (ascendente o descendente).

```python
nombres.sort(reverse=True)
print(nombres)  # Salida: ['Penelope', 'Luis', 'Leo', 'Jackeline', 'Carolina']
```

**Ordenar un DataFrame:**

- `sort_values()`: Ordena por una o más columnas.

```python
import pandas as pd

df = pd.DataFrame({'ventas': [4, 11, 13],
                   'clientes': ['Castillo', 'Alvarez', 'Quiroga'],
                   'fecha': ['2022-10-23', '2022-01-20', '2022-07-22']})

# Ordenar por fecha
df_ordenado = df.sort_values(by='fecha')
print(df_ordenado)
```

**Ordenar por columna de fechas:**

- Convertir la columna a formato fecha/hora antes de ordenar.

```python
df['fecha'] = pd.to_datetime(df['fecha'])
df_ordenado = df.sort_values(by='fecha')
print(df_ordenado)
```

### Agregaciones

---

Las agregaciones son operaciones que permiten resumir un conjunto de datos en un solo valor. En Pandas, estas operaciones se realizan con la función `DataFrame.aggregate()` o `DataFrame.agg()`.

**Funciones de agregación básicas:**

- `sum()`: Suma los valores de una columna.
- `min()`: Obtiene el valor mínimo de una columna.
- `max()`: Obtiene el valor máximo de una columna.
- `mean()`: Calcula la media de una columna.
- `median()`: Obtiene la mediana de una columna.

**Sintaxis de `DataFrame.agg()`:**

```python
DataFrame.agg(func, axis=None, *args, **kwargs)
```

- `func`: Función de agregación a aplicar.
- `axis`: Eje sobre el que se aplica la función (0 por defecto para columnas, 1 para filas).
- `args`: Argumentos posicionales adicionales.
- `*kwargs`: Argumentos de palabras clave adicionales.

```python
import pandas as pd

# Crear un DataFrame
dataframe = pd.DataFrame({'Asistencia': [60, 100, 80],
                         'Nombre': ['Jose', 'Pedro', 'Carmen'],
                         'Calificaciones': [90, 75, 82]})

# Sumar valores de cada columna
dataframe_sum = dataframe.agg('sum')
print(dataframe_sum)

# Obtener estadísticas descriptivas
dataframe_stats = dataframe.describe()
print(dataframe_stats)

# Agregación con una columna específica:

# Aplicar funciones a la columna 'Calificaciones'
dataframe_agg_calificaciones = dataframe.agg({'Calificaciones': ['sum', 'max']})
print(dataframe_agg_calificaciones)
```

**Función `describe()`:**

- Obtiene estadísticas descriptivas de un `DataFrame` (media, mediana, mínimo, máximo, etc.).
- Solo funciona con columnas numéricas.

**Sintaxis de `describe()`:**

```python
DataFrame.describe(percentiles=None, include=None, exclude=None, datetime_is_numeric=False)
```

- `percentiles`: Percentiles a incluir (por defecto, [0.25, 0.5, 0.75]).
- `include`: Tipos de datos a incluir (por defecto, solo numéricos).
- `exclude`: Tipos de datos a excluir.
- `datetime_is_numeric`: Indica si tratar las fechas como números.

**Ejemplo de `describe()`:**

```python
print(dataframe.describe())
```

**Omitir valores faltantes:**

- Usar la función `dropna()` antes de la agregación.

**Sintaxis de `dropna()`:**

```python
DataFrame.dropna(axis, how, thresh, subset, inplace)
```

- `axis`: Eje sobre el que se aplica (0 por defecto para columnas, 1 para filas).
- `how`: Criterio de eliminación ("any" para cualquier valor faltante, "all" para todas las filas/columnas con valores faltantes).
- `thresh`: Umbral mínimo de valores no nulos para mantener filas/columnas.
- `subset`: Columnas específicas a considerar.
- `inplace`: Modificar el `DataFrame` original o crear uno nuevo.

Ejemplo de `dropna()`:

```python
dataframe_dropna = dataframe.dropna()
dataframe_agg_dropna = dataframe_dropna.agg('sum')
print(dataframe_agg_dropna)
```

### Agrupaciones

---

Las agrupaciones en Pandas permiten analizar datos en función de una o más columnas. La función `groupby()` es fundamental para esta tarea, ya que nos permite agrupar el DataFrame y aplicar funciones agregadas a cada grupo.

**Sintaxis de `groupby()`:**

```python
DataFrame.groupby(by=None, axis=0, level=None, as_index=True, sort=True,
                  group_keys=True, squeeze=False, observed=False)
```

**Parámetros:**

- `by`: Columna o columnas por las que se agrupa.
- `axis`: Eje sobre el que se agrupa (0 por defecto para filas, 1 para columnas).
- `level`: Nivel específico para agrupar (útil para DataFrames multinivel).
- `as_index`: Elevar las claves de grupo a un índice (True por defecto).
- `sort`: Ordenar las claves de grupo (True por defecto).
- `group_keys`: Incluir las claves de grupo en el resultado (True por defecto).
- `squeeze`: Reducir la dimensión del resultado si es posible (False por defecto).
- `observed`: Mostrar solo valores observados (False por defecto).

1. Agrupar por una columna y obtener la suma:

```python
import pandas as pd

# Crear un DataFrame
df = pd.DataFrame({'Fruta': ['Manzana', 'Naranja', 'Banana', 'Manzana', 'Melón'],
                   'Precio': [12, 14, 20, 12, 34]})

# Agrupar por 'Fruta' y sumar precios
df_grouped = df.groupby('Fruta')['Precio'].sum()

# Imprimir el resultado
print(df_grouped)
```

Salida:

```python
Fruta
Manzana     24
Naranja     14
Banana      20
Melón       34
Name: Precio, dtype: int64
```

2. Agrupar por varias columnas y obtener la media:

```python
# Agrupar por 'Fruta' y 'Color' y obtener la media del precio
df_grouped = df.groupby(['Fruta', 'Color'])['Precio'].mean()

# Imprimir el resultado
print(df_grouped)
```

3. Filtrar grupos:

```python
# Seleccionar solo el grupo 'Manzana'
df_filtered = df_grouped.get_group('Manzana')

# Imprimir el resultado
print(df_filtered)
```

4. Aplicar funciones personalizadas:

```python
# Definir una función para calcular el descuento
def descuento(precio):
    if precio > 20:
        return precio * 0.1
    else:
        return 0

# Aplicar la función 'descuento' al precio agrupado por 'Fruta'
df_grouped = df.groupby('Fruta')['Precio'].apply(descuento)

# Imprimir el resultado
print(df_grouped)
```

### Tablas *pivot*

---

Las tablas dinámicas (pivot tables) son herramientas útiles para resumir y analizar datos en forma tabular. Pandas ofrece la función `pivot_table()` para crear estas tablas de manera eficiente.

**Sintaxis:**

```python
pd.pivot_table(data, values=None, index=None, columns=None, aggfunc='mean',
              fill_value=None, margins=False, dropna=True, margins_name='All',
              observed=False, sort=True)
```

**Parámetros:**

- `data`: DataFrame a procesar.
- `values`: Columna que contiene los valores a agregar (por defecto, todas las numéricas).
- `index`: Columna que se convierte en el índice de la tabla pivote.
- `columns`: Columna que se convierte en las columnas de la tabla pivote.
- `aggfunc`: Función de agregación a aplicar (por defecto, `mean`). Se puede usar una lista o diccionario para funciones múltiples.
- `fill_value`: Valor a reemplazar por valores faltantes.
- `margins`: Incluir totales por fila y columna (por defecto, False).
- `dropna`: Eliminar filas con valores faltantes (por defecto, True).
- `margins_name`: Nombre para las filas y columnas de totales (por defecto, 'All').
- `observed`: Mostrar solo valores observados (por defecto, False).
- `sort`: Ordenar los niveles del índice y las columnas (por defecto, True).

**Ejemplo:**

Supongamos que tenemos un DataFrame con datos de estudiantes, fechas y puntuaciones en JavaScript:

```python
import pandas as pd

dataframe = pd.DataFrame({
    "Nombre": ["Ana", "Ana", "Ana", "Ana", "María", "María", "María", "María"],
    "Fecha": ["03-06-2022", "04-06-2022", "03-06-2022", "04-06-2022", "03-06-2022", "04-06-2022", "03-06-2022", "04-06-2022"],
    "Puntuación en JavaScript": [10, 2, 4, 6, 8, 9, 1, 10]
})
```

Crear una tabla pivote con la media de la puntuación por estudiante y fecha:

```python
pivot_table = pd.pivot_table(dataframe, index="Nombre", columns="Fecha", aggfunc='mean')
print(pivot_table)
```

Salida:

```python
           Puntuación en JavaScript
Fecha          03-06-2022  04-06-2022
Nombre
Ana            5.500000      4.000000
María           4.500000      9.500000
```

**Explicación:**

- `index="Nombre"`: Agrupa por la columna "Nombre", creando filas para cada estudiante.
- `columns="Fecha"`: Agrupa por la columna "Fecha", creando columnas para cada fecha.
- `aggfunc='mean'`: Calcula la media de la puntuación en JavaScript para cada estudiante y fecha.

**Conclusiones:**

- `pivot_table()` es una herramienta poderosa para resumir y analizar datos en Pandas.
- Permite agrupar y aplicar funciones de agregación a los datos de manera flexible.
- Es útil para generar tablas dinámicas que facilitan la comprensión de conjuntos de datos complejos.

## **Metodología y características**

---

Operaciones con *strings*

Las cadenas de texto (strings) son un tipo de datos fundamental en Python, utilizadas para representar texto. Se caracterizan por su inmutabilidad, es decir, no se pueden modificar una vez creadas.

**Operaciones básicas:**

- **Longitud:** La función `len()` devuelve la longitud de la cadena, es decir, la cantidad de caracteres que la componen.
- **Acceso a caracteres:** Se puede acceder a un carácter específico de la cadena utilizando su índice entre corchetes `[]`. La indexación comienza en 0 y se puede usar indexación negativa para acceder a caracteres desde el final de la cadena.
- **Iteración:** Las cadenas son iterables, lo que significa que se pueden recorrer carácter por carácter usando un bucle `for`.

```python
palabra = "manzana"

# Longitud de la cadena
longitud = len(palabra)
print(f"Longitud de la palabra: {longitud}") # Salida: Longitud de la palabra: 7

# Acceso a caracteres
primer_caracter = palabra[0]
print(f"Primer caracter: {primer_caracter}") # Salida: Primer caracter: m

ultimo_caracter = palabra[-1]
print(f"Ultimo caracter: {ultimo_caracter}") # Salida: Ultimo caracter: a

# Iteración sobre la cadena
for caracter in palabra:
    print(caracter)
```

Salida:

```python
Longitud de la palabra: 7
Primer caracter: m
Ultimo caracter: a
m
a
n
z
a
n
a
```

Operaciones Básicas con Cadenas de Texto (Strings) en Python:

Las cadenas de texto (strings) son un tipo de dato fundamental en Python, utilizadas para representar texto.

**Operaciones básicas:**

**Concatenación:**

- Combina dos o más cadenas de texto usando el operador `+`.
- Se utiliza para unir frases o palabras.
- Ejemplo: `mensaje1 = "Hola"; mensaje2 = "Mundo"; frase = mensaje1 + " " + mensaje2; print(frase)`

**Multiplicación:**

- Repite una cadena de texto un número específico de veces usando el operador ``.
- Se utiliza para crear patrones repetitivos o llenar espacios.
- Ejemplo: `mensaje2a = "Hola " * 3; mensaje2b = "Mundo"; print(mensaje2a + mensaje2b)`

**Adición:**

- Agrega un carácter o cadena de texto al final de una cadena existente usando el operador `+=`.
- Se utiliza para construir cadenas de forma incremental.
- Ejemplo: `mensaje3 = "Hola"; mensaje3 += " "; mensaje3 += "Mundo"; print(mensaje3)`

**Comparación:**

- Compara dos cadenas de texto para determinar si son iguales o diferentes.
- Se utilizan operadores como `==`, `!=`, `<`, `>`, `<=` y `>=`.
- Ejemplo: `letra1 = "d"; letra1 > "a"; letra1 > "g"; letra1 == "D"`

**Conversión de mayúsculas/minúsculas:**

- Convierte una cadena de texto a mayúsculas usando el método `upper()`.
- Convierte una cadena de texto a minúsculas usando el método `lower()`.
- Ejemplo: `mi_cadena = "escrito"; mi_cadena.upper(); mi_cadena.lower()`

**Pertenencia:**

- Verifica si una subcadena específica se encuentra dentro de una cadena de texto usando el operador `in`.
- Devuelve un valor booleano (True o False).
- Ejemplo: `proverb = "Más vale malo conocido que bueno por conocer"; "malo" in proverb; "bueno" in proverb; "regular" in proverb`

**Segmentación:**

- Divide una cadena de texto en una lista de subcadenas utilizando el método `split()`.
- Se utiliza para separar cadenas por un delimitador específico.
- Ejemplo: `texto = "Estoy aprendiendo operaciones con cadenas"; print(texto.split())`

**Cadenas de varias líneas:**

- Define cadenas de texto largas que abarcan varias líneas usando tres comillas simples o dobles (`"""`).
- Conserva los saltos de línea y la estructura del texto.
- Ejemplo: `x = """Estoy aprendiendo operaciones con cadenas en Python..."""; print(x)`

**Eliminación:**

- Elimina una variable que contiene una cadena de texto usando la instrucción `del`.
- Libera el espacio en memoria asociado a la cadena.
- Ejemplo: `texto = "Este es un texto de ejemplo"; print(texto); del texto; print(texto)`

**Caracteres Unicode:**

- Python permite trabajar con caracteres Unicode, incluyendo emojis y símbolos especiales.
- Se utilizan códigos Unicode para representar estos caracteres.
- Ejemplo: `rocket_code = 0x1F680; rocket = chr(rocket_code); print(rocket)`