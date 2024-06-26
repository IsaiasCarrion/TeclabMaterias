# PROCESAMIENTO DE DATOS: MODULO 4

# Análisis e interpretación de datos

---

El análisis exploratorio de datos es una etapa crucial en el procesamiento de datos. Permite obtener una comprensión básica de los datos y las relaciones entre ellos, sentando las bases para el análisis e interpretación posteriores.

Python ofrece diversas herramientas para explorar datasets, incluyendo:

- **Librerías:** Pandas, NumPy, Matplotlib, Seaborn
- **Funciones:** describe(), head(), tail(), sort_values(), groupby()
- **Visualizaciones:** histogramas, gráficos de dispersión, gráficos de líneas, gráficos de barras

**Interpretación de gráficos:**

La interpretación de gráficos es fundamental para extraer información útil de los datos. Se debe considerar:

- **Ejes:** escala, etiquetas
- **Tendencias:** patrones, valores atípicos
- **Relaciones:** correlaciones, asociaciones

### Tipos de datos y cómo analizarlos

---

El análisis exploratorio de datos (EDA) es una etapa crucial en cualquier proyecto basado en datos. Su objetivo es obtener una comprensión básica de los datos y las relaciones entre ellos antes de realizar análisis más profundos.

**Idea clave:**

La observación de los datos es el primer paso fundamental en el EDA.

**Preguntas clave:**

- ¿Existe estructura en los datos?
- ¿Dónde están centrados?
- ¿Cuál es la dispersión?
- ¿Qué relaciones hay entre las variables?
- ¿Cómo sintetizar y presentar la información?
- ¿Hay sesgo o errores en los datos?
- ¿Hay datos atípicos o faltantes? ¿Cómo tratarlos?

**Pasos del EDA:**

1. Familiarizarse con los datos.
2. Examen gráfico y descriptivo de las variables.
3. Examen gráfico y descriptivo de las relaciones entre variables.
4. Preparar los datos para análisis.
5. Identificar y evaluar datos atípicos.
6. Analizar el efecto de datos faltantes.

**Conexión con la estadística descriptiva:**

La estadística descriptiva utiliza métodos gráficos y numéricos para resumir, procesar y transformar datos en información.

### Tipos de datos

---

![Untitled](PROCESAMIENTO%20DE%20DATOS%20MODULO%204%20163c4337268a455ba5f0226091cbf0ab/Untitled.png)

**Análisis de datos cualitativos:**

- **Datos discretos:** Son datos que solo pueden tomar ciertos valores específicos, como números enteros. Por ejemplo, el número de estudiantes en una clase o la cantidad de goles marcados en un partido de fútbol.
- **Datos continuos:** Son datos que pueden tomar cualquier valor dentro de un rango específico. Por ejemplo, la altura de los estudiantes en una clase o la temperatura en un día determinado.
- Las tablas de frecuencia son herramientas ideales para resumir y analizar datos cualitativos.
- Estas tablas muestran el recuento de las diferentes categorías presentes en los datos.
- Se pueden utilizar frecuencias absolutas o relativas (porcentajes), siendo estas últimas más comunes y útiles para la interpretación.

Datos cualitativos:

- **Datos ordinales:** Son datos que se pueden ordenar según una escala específica, pero no tienen una diferencia numérica significativa entre ellos. Por ejemplo, la calificación de una película (mala, regular, buena, excelente) o el nivel de satisfacción de los clientes (insatisfecho, neutral, satisfecho, muy satisfecho).
- **Datos nominales:** Son datos que se clasifican en categorías que no tienen un orden específico. Por ejemplo, el color de un automóvil o la religión de una persona.
- **Análisis de contenido:** Permite identificar temas, patrones y significados en los datos textuales.
- **Teoría fundamentada:** Permite desarrollar teorías a partir de los datos recolectados.
- **Entrevistas en profundidad:** Permiten obtener información detallada y matizada de los participantes.

**Medidas de frecuencia:**

- **Porcentaje:** Representa la proporción de una categoría respecto al total, expresada como un valor entre 0 y 100%.
- **Razón:** Es el cociente entre dos cantidades comparables, proporcionando la relación entre ellas.
- **Tasa:** Se define como la fracción entre dos magnitudes relacionadas, donde el denominador siempre debe incluir al numerador. Existen diferentes tipos de tasas, como la tasa de mortalidad, natalidad, interés, entre otras.
- **Índice:** Es una expresión numérica que resume la relación entre dos cantidades. Puede ser una proporción, razón, tasa o un valor contextual que indique una situación específica.

**Ejemplos de medidas de frecuencia:**

- **Porcentaje de respuestas correctas en un examen:** 90 respuestas correctas de 100 (equivalente al 90%).
- **Razón de ventas por vendedor:** 2000 productos vendidos / 10 vendedores (equivalente a 200 productos por vendedor).
- **Tasa de interés anual:** 2% (equivalente a 2 pesos cobrados por cada 100 pesos prestados).
- **Índice de aumento de ingresos:** (1200 ingresos este año - 1000 ingresos año anterior) / 1000 * 100% (equivalente a un aumento del 20%).

**Ordenamiento de tablas de frecuencia:**

- **Datos ordinales:** Se ordenan de forma natural según su propio orden inherente.
- **Datos nominales:** Se recomienda utilizar un criterio de ordenamiento sencillo, como el orden alfabético.

### Funciones para explorar el dataset

---

El análisis exploratorio de datos (EDA) es una etapa crucial en cualquier proyecto de análisis de datos. Su objetivo principal es detectar valores atípicos, errores y patrones en los datos para comprenderlos mejor antes de realizar análisis más profundos. Los resultados del EDA son valiosos para empresas que buscan conocer mejor a sus clientes, tomar decisiones informadas y expandir su negocio.

**Ejemplo práctico con un dataset de automóviles:**

**1. Importación de librerías y lectura del dataset:**

- Se importan las librerías necesarias para el análisis (numpy, pandas, matplotlib.pyplot).
- Se lee el dataset de automóviles desde un archivo CSV (se proporciona un enlace de descarga).
- Se verifica el tamaño del dataset utilizando la función "shape".

```python
# Importación de librerías
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Lectura del dataset de automóviles desde un archivo CSV
ruta_archivo = "C:\\Users\\IPP\\Downloads\\Automobile_data.csv"  # Ajustar la ruta según sea necesario
datos = pd.read_csv(ruta_archivo)

# Visualización de las primeras 5 filas del dataset
print(datos.head())

# Obtención del tamaño del dataset
print("Tamaño del dataset:", datos.shape)
```

**2. Descripción general del dataset:**

- Se utiliza la función "describe()" para obtener información resumida de las variables numéricas (media, desviación estándar, min, cuartiles, max).
- Se verifica la presencia de valores faltantes utilizando la función "isnull().sum()".

```python
# Importación de librerías
import numpy as np
import pandas as pd

# Lectura del dataset de automóviles desde un archivo CSV
ruta_archivo = "C:\\Users\\IPP\\Downloads\\Automobile_data.csv"  # Ajustar la ruta según sea necesario
datos = pd.read_csv(ruta_archivo)

# Descripción general del dataset: información resumida de las variables numéricas
descripcion_numericas = datos.describe()
print(descripcion_numericas)

# Descripción general del dataset: verificación de valores faltantes
valores_faltantes = datos.isnull().sum()
print(valores_faltantes)
```

**3. Análisis de tipos de datos:**

- Se verifica el tipo de datos de cada variable utilizando la función "dtypes".
- Se identifican variables que deberían ser numéricas pero están como "object" debido a la presencia del símbolo "?".

```python
# Importación de librerías
import numpy as np
import pandas as pd

# Lectura del dataset de automóviles desde un archivo CSV
ruta_archivo = "C:\\Users\\IPP\\Downloads\\Automobile_data.csv"  # Ajustar la ruta según sea necesario
datos = pd.read_csv(ruta_archivo)

# Análisis de tipos de datos: verificación de tipos de datos de cada variable
tipos_datos = datos.dtypes
print(tipos_datos)

# Análisis de tipos de datos: identificación de variables con errores de tipo
columnas_erroneas = datos.select_dtypes(include=['object']).columns
for columna in columnas_erroneas:
    # Revisión de valores "?" en las columnas identificadas
    valores_erroneos = datos[columna].str.contains('?').sum()
    if valores_erroneos > 0:
        print(f"La columna '{columna}' tiene {valores_erroneos} valores con '?'")
```

**4. Tratamiento de valores faltantes y errores:**

- Se reemplazan los valores "?" por "nan" (valor nulo) en las variables con errores.
- Se realiza un recuento de valores nulos en las variables afectadas.
- Se visualiza la distribución de valores nulos con un mapa de calor.
- Se opta por rellenar los espacios vacíos en las variables numéricas con la media.

```python
# Importación de librerías
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Lectura del dataset de automóviles desde un archivo CSV
ruta_archivo = "C:\\Users\\IPP\\Downloads\\Automobile_data.csv"  # Ajustar la ruta según sea necesario
datos = pd.read_csv(ruta_archivo)

# Análisis de tipos de datos: identificación de variables con errores de tipo
columnas_erroneas = datos.select_dtypes(include=['object']).columns

# Reemplazo de valores "?" por NaN en las variables con errores
for columna in columnas_erroneas:
    datos[columna] = datos[columna].str.replace('?', np.nan)

# Recuento de valores nulos en las variables afectadas
valores_nulos = datos.isnull().sum()
print(valores_nulos)

# Visualización de la distribución de valores nulos con un mapa de calor
mapa_calor = valores_nulos.plot(kind='heatmap')
plt.show()

# Relleno de espacios vacíos en variables numéricas con la media
for columna_numerica in datos.select_dtypes(include=['number']).columns:
    if valores_nulos[columna_numerica] > 0:
        datos[columna_numerica].fillna(datos[columna_numerica].mean(), inplace=True)

# Verificación final de valores nulos
valores_nulos_final = datos.isnull().sum()
print(valores_nulos_final)
```

### Funciones básicas de matemáticas

---

- Los tipos de datos incorporados en Python son adecuados para la mayoría de las necesidades matemáticas básicas.

```python
# Tipos de datos numéricos básicos
entero = 10  # Tipo int (números enteros)
decimal = 5.2  # Tipo float (números de coma flotante)

# Operaciones básicas
suma = entero + decimal
resta = entero - decimal
multiplicacion = entero * decimal
division = entero / decimal

print(f"Suma: {suma}")
print(f"Resta: {resta}")
print(f"Multiplicación: {multiplicacion}")
print(f"División: {division}")
```

- El módulo `decimal` ofrece una representación exacta de números no enteros.

```python
# Importación del módulo decimal
import decimal

# Creación de un objeto decimal con mayor precisión
valor_decimal = decimal.Decimal("10.234567890123456789")

# Operaciones con mayor precisión
suma_decimal = valor_decimal + 5.2
resta_decimal = valor_decimal - 5.2
multiplicacion_decimal = valor_decimal * 2
division_decimal = valor_decimal / 3

# Conversión a string para visualizar la precisión
print(f"Suma decimal: {suma_decimal}")
print(f"Resta decimal: {resta_decimal}")
print(f"Multiplicación decimal: {multiplicacion_decimal}")
print(f"División decimal: {division_decimal}")
```

- El módulo `fractions` es útil para trabajar con números racionales (fracciones).

```python
# Importación del módulo fractions
from fractions import Fraction

# Creación de números racionales
fraccion1 = Fraction(1, 2)  # Fracción 1/2
fraccion2 = Fraction(3, 4)  # Fracción 3/4

# Operaciones con números racionales
suma_fraccion = fraccion1 + fraccion2
resta_fraccion = fraccion1 - fraccion2
multiplicacion_fraccion = fraccion1 * fraccion2
division_fraccion = fraccion1 / fraccion2

# Conversión a string para visualizar las fracciones
print(f"Suma fracciones: {suma_fraccion}")
print(f"Resta fracciones: {resta_fraccion}")
print(f"Multiplicación fracciones: {multiplicacion_fraccion}")
print(f"División fracciones: {division_fraccion}")
```

- El módulo `random` permite generar números aleatorios con diferentes distribuciones.

```python
# Importación del módulo random
import random

# Generación de números aleatorios uniformes
numero_aleatorio_uniforme = random.random()  # Valor entre 0 y 1
print(f"Número aleatorio uniforme: {numero_aleatorio_uniforme}")

# Generación de números aleatorios enteros dentro de un rango
numero_aleatorio_entero = random.randint(10, 20)  # Entre 10 y 20 (incluidos)
print(f"Número aleatorio entero: {numero_aleatorio_entero}")

# Generación de números aleatorios con distribución normal
numero_aleatorio_normal = random.gauss(mu=5, sigma=2)  # Media = 5, desviación estándar = 2
print(f"Número aleatorio normal: {numero_aleatorio_normal}")
```

- El módulo `math` proporciona funciones matemáticas avanzadas como logaritmos y funciones trigonométricas.

```python
# Importación del módulo math
import math

# Cálculo de logaritmo neperiano
valor = 10
logaritmo_neperiano = math.log(valor)
print(f"Logaritmo neperiano de {valor}: {logaritmo_neperiano}")

# Cálculo de seno
angulo_en_radianes = math.pi / 4  # Radianes
seno = math.sin(angulo_en_radianes)
print(f"Seno de {angulo_en_radianes} radianes: {seno}")

# Cálculo de la raíz cuadrada
numero = 16
raiz_cuadrada = math.sqrt(numero)
print(f"Raíz cuadrada de {numero}: {raiz_cuadrada}")
```

- El módulo `statistics` implementa fórmulas estadísticas comunes para diversos tipos de datos.

```python
# Importación del módulo statistics
import statistics

# Lista de datos
datos = [10, 5, 2]
```

- Pandas facilita el análisis de datos tabulares y la creación de visualizaciones.

```python
# Carga de datos y exploración
import pandas as pd

datos_venta = pd.read_csv("datos_venta.csv")

print(datos_venta.head())
print(datos_venta.info())
print(datos_venta.describe())

# Análisis de las ventas por producto

# Agrupación de datos por producto
datos_agrupados_producto = datos_venta.groupby("Producto")

# Cálculo de las ventas totales por producto
ventas_totales_producto = datos_agrupados_producto["Precio_venta"] * datos_agrupados_producto["Cantidad"].sum()

# Visualización de las ventas totales por producto en un gráfico de barras
ventas_totales_producto.plot(kind="bar")

# Análisis de las ventas por fecha

# Agrupación de datos por fecha
datos_agrupados_fecha = datos_venta.groupby("Fecha")

# Cálculo de las ventas totales por fecha
ventas_totales_fecha = datos_agrupados_fecha["Precio_venta"] * datos_agrupados_fecha["Cantidad"].sum()

# Visualización de las ventas totales por fecha en un gráfico de líneas
ventas_totales_fecha.plot(kind="line")

# Identificación del producto más vendido

# Selección del producto con mayor venta total
producto_mas_vendido = ventas_totales_producto.idxmax()
print(f"Producto más vendido: {producto_mas_vendido}")

# Exportación de los resultados

# Guardado de las ventas totales por producto en un archivo CSV
ventas
```

# Gráficos y su interpretación

---

Existen diversas librerías de visualización asociadas a Python que se están aplicando en diversas áreas de vanguardia:
Machine learning.

**Librerías para visualización:**

- **Matplotlib:** Librería estándar para crear gráficos de calidad para publicaciones impresas o digitales. Permite generar diversos tipos de gráficos como series temporales, histogramas y diagramas de barras.
- **Seaborn:** Basada en Matplotlib, ofrece una interfaz de alto nivel para crear visualizaciones estadísticas atractivas e informativas. Se integra con Pandas para facilitar el análisis de datos.
- **Bokeh:** Permite crear gráficos interactivos para visualización en navegadores web. Se enfoca en un alto rendimiento y la capacidad de manejar grandes volúmenes de datos, incluso en tiempo real.

**Librerías para cálculo numérico y análisis de datos:**

- **NumPy:** Brinda estructuras de datos eficientes para manejar grandes conjuntos de datos y funciones matemáticas de alto nivel para su análisis.
- **SciPy:** Complementa a NumPy con rutinas numéricas especializadas para optimización, interpolación, transformadas de Fourier y análisis estadístico.
- **Pandas:** Ofrece estructuras de datos DataFrames y Series para manejar datos tabulares de manera eficiente. Facilita la manipulación, limpieza y análisis de datos.
- **Numba:** Compilador de Python que acelera la ejecución de código numérico mediante la generación de código máquina optimizado.

**Librerías para Machine Learning:**

- **Scikit-learn:** Librería de referencia para Machine Learning con una amplia gama de algoritmos para tareas de clasificación, regresión y agrupamiento. Destaca por su facilidad de uso y flexibilidad.

**Librerías para Deep Learning:**

- **TensorFlow:** Desarrollada por Google, permite realizar cálculos numéricos mediante diagramas de flujo de datos. Es flexible y se puede ejecutar en CPUs, GPUs o dispositivos móviles.
- **Keras:** Interfaz de alto nivel para trabajar con redes neuronales en TensorFlow, simplificando la creación y experimentación de modelos Deep Learning.
- **PyTorch:** Librería para cálculo numérico eficiente en CPU y GPU, similar a NumPy pero con enfoque en Deep Learning. Permite aprovechar la potencia de las GPUs para acelerar cálculos matriciales.

**Librerías para Inteligencia Artificial Explicable:**

- **SHAP:** Utiliza técnicas de teoría de juegos para explicar las predicciones de modelos de Machine Learning complejos como random forests o redes neuronales. Permite comprender la influencia de las variables en las decisiones del modelo.

**Librerías para Procesamiento del Lenguaje Natural:**

- **NLTK:** Librería clásica para procesamiento del lenguaje natural, útil para tareas como tokenización, lematización y eliminación de palabras irrelevantes.
- **Gensim:** Especializada en modelado de temas, identifica automáticamente los temas principales en un conjunto de documentos. También permite crear representaciones vectoriales de palabras y analizar la similitud entre documentos.
- **spaCy:** Librería rápida para procesamiento del lenguaje natural enfocada en aplicaciones reales. Extrae información relevante, prepara texto para otras tareas de Machine Learning y permite construir modelos lingüísticos estadísticos.

**Herramientas adicionales:**

- **Jupyter Notebook:** Entorno web interactivo para ejecutar código Python, visualizar datos, crear documentos y facilitar la experimentación y documentación del trabajo.
- **Anaconda:** Distribución de Python que incluye muchas de las librerías mencionadas y facilita su instalación y gestión. Permite crear entornos de trabajo aislados para diferentes proyectos.

### Matplotlib: consejos generales

---

Matplotlib es una librería de Python para la visualización de datos en 2D, basada en matrices de NumPy. Permite crear y personalizar diversos tipos de gráficos, como diagramas de barras, histogramas, diagramas de sectores, diagramas de caja y bigotes, diagramas de violín, diagramas de dispersión, diagramas de líneas, diagramas de áreas, diagramas de contorno y mapas de color, además de combinaciones entre ellos.

Permite crear y personalizar los tipos de gráficos más comunes:

- Diagramas de barras.
- Histograma.
- Diagramas de sectores.
- Diagramas de caja y bigotes (boxplot).
- Diagramas de violín.
- Diagramas de dispersión o puntos.
- Diagramas de líneas.
- Diagramas de áreas.
- Diagramas de contorno.
- Mapas de color.

### Pasos para usar Matplotlib:

1. **Importar Matplotlib**:

```python
import matplotlib.mpl as plt
```

1. **Estilos de configuración**:
Utiliza `plt.style` para elegir estilos estéticos, comenzando con el estilo clásico y actualizándolo según sea necesario.
2. **Visualización de gráficos**:
Usa `plt.show()` para mostrar gráficos en ventanas interactivas.
3. **Creación de gráficos simples**:
    - Grafico de línea simple:

        ```python
        import matplotlib.pyplot as plt
        fig, ax = plt.subplots()
        ax.plot(x, y)
        plt.show()
        ```

4. **Ajuste de gráficos**:
    - Colores y estilos de línea:

        ```python
        plt.plot(x, y, color='blue', linestyle='--')
        ```

    - **Límites de los ejes**:

        ```python
        plt.xlim(min, max)
        plt.ylim(min, max)
        ```

5. **Etiquetar gráficos**:
    - Añadir títulos y etiquetas de ejes:

    ```python
    plt.title('Título')
    plt.xlabel('Eje X')
    plt.ylabel('Eje Y')
    ```

    - Crear leyendas

    ```python
    plt.legend(['Etiqueta'])
    ```


### Sinusoide

Un gráfico que representa la función seno, mostrando su comportamiento ondulatorio a lo largo del eje x.

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 10, 100)
y = np.sin(x)

fig, ax = plt.subplots()
ax.plot(x, y)
plt.show()
```

### Figura con varias líneas

Un gráfico que muestra múltiples líneas, permitiendo comparar diferentes conjuntos de datos en el mismo espacio de ejes.

```python
y2 = np.cos(x)

fig, ax = plt.subplots()
ax.plot(x, y, label='Sine')
ax.plot(x, y2, label='Cosine')
plt.legend()
plt.show()
```

### Cómo ajustar el gráfico: colores y estilos de línea

Personalizar un gráfico cambiando el color y el estilo de las líneas para mejorar la visualización y diferenciación de datos.

```python
fig, ax = plt.subplots()
ax.plot(x, y, color='blue', linestyle='--', label='Sine')
ax.plot(x, y2, color='green', linestyle='-', label='Cosine')
plt.legend()
plt.show()
```

### Especificar color

Definir colores específicos para las líneas o elementos del gráfico, utilizando nombres de colores, códigos RGB o abreviaciones.

```python
fig, ax = plt.subplots()
ax.plot(x, y, color='#1f77b4')  # RGB Hex color
plt.show()
```

### Estilo de línea

Modificar el patrón de las líneas en un gráfico, como líneas sólidas, punteadas o a rayas.

```python
fig, ax = plt.subplots()
ax.plot(x, y, linestyle='-.')  # Dash-dot line
plt.show()
```

### Abreviaciones

Usar códigos cortos para especificar colores y estilos de línea, facilitando la personalización rápida de gráficos.

```python
fig, ax = plt.subplots()
ax.plot(x, y, 'g--')  # Green dashed line
plt.show()
```

### Cómo ajustar el gráfico: límite de los ejes

Configurar los límites mínimos y máximos de los ejes x e y para enfocar áreas específicas del gráfico.

```python
fig, ax = plt.subplots()
ax.plot(x, y)
ax.set_xlim(0, 12)
ax.set_ylim(-1.5, 1.5)
plt.show()
```

### Ajustar el gráfico

Realizar cambios en los límites de los ejes para mejorar la presentación de los datos.

```python
fig, ax = plt.subplots()
ax.plot(x, y)
ax.set_xlim(0, 8)
ax.set_ylim(-1, 1)
plt.show()
```

### Gráfico ajustado

Un gráfico que ha sido modificado en sus límites de ejes para resaltar áreas específicas de interés.

```python
fig, ax = plt.subplots()
ax.plot(x, y)
ax.set_xlim(2, 8)
ax.set_ylim(-0.5, 0.5)
plt.show()
```

### Invertir el orden de los ejes

Revertir la dirección de los ejes x o y, invirtiendo el orden en que se presentan los datos.

```python
fig, ax = plt.subplots()
ax.plot(x, y)
ax.set_xlim(ax.get_xlim()[::-1])  # Invertir eje x
ax.set_ylim(ax.get_ylim()[::-1])  # Invertir eje y
plt.show()
```

### Etiquetar los gráficos

Añadir títulos, etiquetas a los ejes y leyendas para describir y explicar el contenido del gráfico.

```python
fig, ax = plt.subplots()
ax.plot(x, y)
ax.set_title('Título del Gráfico')
ax.set_xlabel('Eje X')
ax.set_ylabel('Eje Y')
plt.show()
```

### Revisar etiquetas y títulos

Ajustar la posición, tamaño y estilo de los títulos y etiquetas de los ejes para mejorar la claridad y presentación del gráfico.

```python
fig, ax = plt.subplots()
ax.plot(x, y)
ax.set_title('Título del Gráfico', fontsize=14, fontweight='bold')
ax.set_xlabel('Eje X', fontsize=12)
ax.set_ylabel('Eje Y', fontsize=12)
plt.show()
```

### Método plt.legend()

Crear una leyenda en el gráfico que explique los diferentes elementos o series de datos mostrados.

```python
fig, ax = plt.subplots()
ax.plot(x, y, label='Sine')
ax.plot(x, y2, label='Cosine')
ax.legend(loc='upper right')
plt.show()
```

### Gráfico de barras discreto

Un gráfico que muestra datos categóricos mediante barras verticales, donde la altura de cada barra representa el valor de la categoría correspondiente.

```python
categories = ['A', 'B', 'C', 'D']
values = [5, 7, 3, 8]

fig, ax = plt.subplots()
ax.bar(categories, values)
plt.show()
```

### Gráfico invertido

Un gráfico de barras donde las barras se presentan horizontalmente en lugar de verticalmente.

```python
fig, ax = plt.subplots()
ax.barh(categories, values)  # Horizontal bar chart
plt.show()
```

### Barras agrupadas

Un gráfico de barras que muestra múltiples series de datos agrupadas por categorías, permitiendo comparaciones directas entre las series dentro de cada categoría.

```python
categories = ['A', 'B', 'C', 'D']
values1 = [5, 7, 3, 8]
values2 = [4, 6, 2, 9]
width = 0.35  # Ancho de las barras

fig, ax = plt.subplots()
ax.bar(np.arange(len(categories)) - width/2, values1, width, label='Grupo 1')
ax.bar(np.arange(len(categories)) + width/2, values2, width, label='Grupo 2')
ax.set_xticks(np.arange(len(categories)))
ax.set_xticklabels(categories)
ax.legend()
plt.show()
```

### Gráfico de barras apiladas

Un gráfico de barras que apila múltiples series de datos en una sola barra por categoría, mostrando la contribución de cada serie al total de la categoría.

```python
fig, ax = plt.subplots()
ax.bar(categories, values1, label='Grupo 1')
ax.bar(categories, values2, bottom=values1, label='Grupo 2')  # Apilar grupo 2 sobre grupo 1
ax.legend()
plt.show()
```

### Histograma

Un gráfico que muestra la distribución de un conjunto de datos dividiéndolo en intervalos (bins) y representando la frecuencia de datos en cada intervalo mediante barras.

```python
data = np.random.randn(1000)

fig, ax = plt.subplots()
ax.hist(data, bins=30)
plt.show()
```

### Histograma con más atributos

Un gráfico que muestra la distribución de un conjunto de datos dividiéndolo en intervalos (bins) y representando la frecuencia de datos en cada intervalo mediante barras.

```python
fig, ax = plt.subplots()
ax.hist(data, bins=30, edgecolor='black', alpha=0.7)
plt.show()
```

### Uso de histtype='stepfilled’

Un histograma donde las barras se dibujan con contornos y están rellenas, combinando las ventajas de los histogramas de paso y de relleno.

```python
fig, ax = plt.subplots()
ax.hist(data, bins=30, edgecolor='black', alpha=0.7, histtype='stepfilled')
plt.show()
```

### Diagrama de caja

Un gráfico que muestra la distribución de un conjunto de datos mediante sus cuartiles y posibles valores atípicos, destacando la mediana, el rango intercuartílico y los valores extremos.

Los cuartiles son divisiones de los datos en cuatro partes: el primer cuartil (Q1) representa hasta un 25 %. El segundo cuartil (Q2) corresponde al 50 % (igual a la mediana). El tercer cuartil (Q3) es la ubicación del dato en la posición del 75 %. También podemos encontrar quintiles al dividir en 5 grupos, deciles al dividir en 10 grupos y percentiles al dividir en 100.

```python
import matplotlib.pyplot as plt
import numpy as np
# Generar datos aleatorios para dos grupos
np.random.seed(10)  # Semilla para la reproducibilidad
data1 = np.random.normal(0, 1, 100)  # Grupo 1: media 0, desviación estándar 1
data2 = np.random.normal(1, 1.5, 100)  # Grupo 2: media 1, desviación estándar 1.5

# Crear el diagrama de caja
fig, ax = plt.subplots()
ax.boxplot([data1, data2], labels=['Grupo 1', 'Grupo 2'])

# Añadir títulos y etiquetas
ax.set_title('Comparación de Grupos con Boxplot')
ax.set_xlabel('Grupo')
ax.set_ylabel('Valor')

# Mostrar el gráfico
plt.show()
```

### Interpretación de datos y gráficos

---

El análisis de datos a partir de gráficos es una herramienta fundamental en el análisis exploratorio, ya que permite visualizar y comprender rápidamente grandes conjuntos de datos. El objetivo no es solo crear gráficos, sino extraer conclusiones relevantes que apoyen la toma de decisiones.

**Tipos de gráficos:**

**a. Gráfico de barras discreto:**

- Permite comparar rápidamente cantidades o sumas entre diferentes categorías.
- Ejemplo: Comparación de costos de vuelos por aerolínea.
- Preguntas de negocio: ¿Qué ciudad tiene el mismo costo de viaje en ambas aerolíneas? ¿Qué aerolínea conviene para viajar a Puerto Varas en términos de costo?

```python
import matplotlib.pyplot as plt

# Definir datos
ciudades = ["Concepción", "Puerto Montt", "Temuco", "Valdivia"]
aerolíneas = ["Latam", "SKY"]
precios_latam = [50000, 42000, 45000, 58000]
precios_sky = [48000, 38000, 42000, 55000]

# Crear figura y ejes
fig, ax = plt.subplots()

# Crear barras
bar_width = 0.35
bar_pos = range(len(ciudades))

ax.bar(bar_pos, precios_latam, label='Latam', width=bar_width, color='blue')
ax.bar([p + bar_width for p in bar_pos], precios_sky, label='SKY', width=bar_width, color='orange')

# Personalizar el gráfico
plt.title('Comparación de precios de vuelos por aerolínea')
plt.xlabel('Ciudad')
plt.ylabel('Precio (miles de pesos)')
plt.xticks([p + bar_width / 2 for p in bar_pos], ciudades)
plt.legend()

# Mostrar el gráfico
plt.show()

```

**b. Histograma:**

- Mide la distribución de datos continuos (peso, temperatura, tiempo, etc.).
- Ejemplo: Distribución de precios de automóviles.
- Permite identificar concentraciones de datos y valores atípicos.

```python
import matplotlib.pyplot as plt
import numpy as np

# Definir datos
datos = np.random.randn(1000)  # Ejemplo de datos aleatorios (puedes cambiarlos por tus datos)

# Crear figura y eje
fig, ax = plt.subplots()

# Crear histograma
n, bins, patches = ax.hist(datos, bins='auto', edgecolor='black')

# Personalizar el gráfico
plt.title('Histograma de datos')
plt.xlabel('Valor')
plt.ylabel('Frecuencia')
plt.grid(True)

# Mostrar el gráfico
plt.show()
```

**c. Diagrama de caja (boxplot):**

- Permite identificar valores atípicos y comparar distribuciones de datos.
- Muestra la distribución del 50% de los valores centrales.
- Ejemplo: Comparación de distribuciones de "normalized-losses".

```python
import matplotlib.pyplot as plt
import numpy as np

# Definir datos
datos = np.array([
    [25000, 30000, 35000, 40000, 45000],  # Grupo 1
    [32000, 35000, 38000, 42000, 46000],  # Grupo 2
    [28000, 31000, 34000, 37000, 40000],  # Grupo 3
])

# Crear figura y eje
fig, ax = plt.subplots()

# Crear diagrama de caja
bp = ax.boxplot(datos, vert=True, patch_artist=True)

# Personalizar el gráfico
plt.title('Diagrama de caja de datos')
plt.xlabel('Grupo')
plt.ylabel('Valor')
plt.xticks([1, 2, 3], ['Grupo 1', 'Grupo 2', 'Grupo 3'])

# Ajustar colores
for box, median in zip(bp['boxes'], bp['medians']):
    box.set_facecolor('lightblue')
    median.set_color('red')

# Mostrar el gráfico
plt.show()
```