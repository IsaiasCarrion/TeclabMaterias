# SCRIPTING: MODULO 3

# Listas y diccionarios

---

**¿Qué son las listas?**

Las listas son estructuras de datos en Python que permiten almacenar **múltiples valores** en una misma variable. A diferencia de las variables simples, que solo pueden almacenar un único valor, las listas son ideales para trabajar con **conjuntos de datos**.

**¿Cómo se definen las listas?**

Las listas se definen utilizando corchetes `[]` y separando los elementos por comas. Los elementos pueden ser de cualquier tipo de dato en Python, incluso otras listas.

```python
mi_lista = [1, 2.5, "Hola", True]
```

**¿Cómo acceder a elementos de una lista?**

Para acceder a un elemento específico de una lista, se utiliza el índice del elemento entre corchetes. El índice comienza en **0** para el primer elemento y aumenta en 1 para cada elemento subsecuente.

```python
primer_elemento = mi_lista[0]  # primer_elemento = 1
tercer_elemento = mi_lista[2]  # tercer_elemento = "Hola"
```

**¿Cómo modificar elementos de una lista?**

Se puede modificar el valor de un elemento de una lista asignando un nuevo valor al índice correspondiente.

```python
mi_lista[2] = "Mundo"  # Cambia "Hola" por "Mundo" en la lista
```

**¿Cómo agregar elementos a una lista?**

Se pueden agregar elementos al final de una lista utilizando el método `append()`.

```python
mi_lista.append(6)  # Agrega el número 6 al final de la lista
```

**¿Cómo eliminar elementos de una lista?**

Se pueden eliminar elementos de una lista utilizando el método `remove()` o el operador `del`.

```python
mi_lista.remove(2.5)  # Elimina el elemento 2.5 de la lista
del mi_lista[0]  # Elimina el primer elemento de la lista
```

**¿Cómo obtener la longitud de una lista?**

Se puede obtener la longitud de una lista utilizando la función `len()`.

```python
longitud_lista = len(mi_lista)  # longitud_lista = 4
```

## ¿Qué es un índice en una lista en Python?

En Python, un índice es una **posición numérica** que se asigna a cada elemento dentro de una lista. Los índices comienzan en **0** para el primer elemento y aumentan en 1 para cada elemento subsecuente, los índices sirven para **acceder a elementos específicos** de una lista de manera precisa y eficiente.

**Beneficios:**

- **Organización:** Permite una organización estructurada de los datos dentro de la lista.
- **Acceso rápido:** Facilita el acceso a elementos específicos sin recorrer toda la lista.
- **Modificación:** Permite modificar o eliminar elementos específicos de la lista.

```python
# Lista de nombres
nombres = ["Juan", "María", "Pedro", "Ana"]

# Si quieres acceder al nombre "María", que se encuentra en la segunda posición, puedes usar su índice:
nombre = nombres[1]  # nombre = "María"
```

**Tipos de índices:**

- **Positivo:** Comienza en 0 y aumenta en 1 para cada elemento. Se utiliza para acceder a elementos desde el principio de la lista.
- **Negativo:** Comienza en -1 y disminuye en 1 para cada elemento. Se utiliza para acceder a elementos desde el final de la lista.

```python
# Indice Negativo
ultimo_nombre = nombres[-1]  # ultimo_nombre = "Ana"
```

### Operaciones con listas en Python

**1. Suma de listas:**

- El operador `+` concatena las listas.
- La primera lista se agrega al final de la segunda.
- Ejemplo: `lista1 + lista2 = [elementos_lista1, elementos_lista2]`

**2. Multiplicación de listas:**

- El operador `` repite la lista la cantidad de veces indicada.
- La lista se multiplica por sí misma.
- Ejemplo: `lista * 3 = [elemento1, elemento2, ..., elementoN] * 3 = [elemento1, elemento1, elemento1, ..., elementoN, elementoN, elementoN]`

**3. Reemplazar un valor:**

- Asignar un nuevo valor a un índice específico de la lista.
- El índice comienza en 0.
- Ejemplo: `lista[indice] = nuevo_valor`

**4. Copiar valores:**

- Asignar el valor de un índice a otro índice de la lista.
- Ejemplo: `lista[indice_destino] = lista[indice_origen]`

**Importancia:**

- Las operaciones de listas son esenciales para **manipular y actualizar datos** de forma eficiente.
- Permiten **agregar, eliminar, modificar y reordenar** elementos de la lista.

## Operaciones con listas dinámicas en Python

**Introducción:**

Las listas en Python no solo se limitan a definirse estáticamente con un conjunto de elementos inicial, sino que también pueden **variar su tamaño** durante la ejecución del programa. Esto permite **agregar, eliminar y modificar elementos** de forma dinámica.

**Funciones y métodos:**

- **Funciones:** Se utilizan con variables para obtener un resultado, pero no pertenecen a un tipo de dato específico.
- **Métodos:** Pertenecen a un tipo de dato específico y permiten modificar el estado de la variable. Se invocan utilizando `objeto.metodo()`.

**Operaciones principales:**

**1. Función `len()`:**

- Obtiene la cantidad de elementos en una lista.
- Sintaxis: `len(lista)`
- Ejemplo: `resultado = len(mi_lista)`

**2. Método `append()`:**

- Agrega un elemento al **final** de la lista.
- Sintaxis: `lista.append(elemento)`
- Ejemplo: `mi_lista.append(6)`

**3. Método `insert()`:**

- Inserta un elemento en una **posición específica** de la lista.
- Sintaxis: `lista.insert(indice, elemento)`
- Ejemplo: `mi_lista.insert(2, "texto")`

**4. Método `pop()`:**

- Elimina un elemento de la lista por su **índice** y lo devuelve.
- Sintaxis: `elemento = lista.pop(indice)`
- Ejemplo: `elemento_eliminado = mi_lista.pop(0)`

**Beneficios:**

- **Flexibilidad:** Permiten adaptar las listas a las necesidades del programa durante la ejecución.
- **Gestión eficiente de datos:** Facilitan la manipulación de grandes conjuntos de datos dinámicos.

### Definición y diferencia con tuplas

**¿Qué son las tuplas?**

Las tuplas son estructuras de datos que almacenan **colecciones ordenadas de elementos**. Son similares a las listas, pero con una diferencia crucial: **son inmutables**, es decir, **no se pueden modificar** una vez creadas.

**¿Cuándo usar tuplas?**

- **Datos inmutables:** Para almacenar datos que no van a cambiar, como constantes o configuraciones.
- **Eficiencia:** Las tuplas son más rápidas de procesar que las listas, ideales para casos donde se requiere alto rendimiento.
- **Seguridad:** La inmutabilidad las hace seguras contra modificaciones accidentales.

```python
# Definición de una tupla
mi_tupla = (1, 2, 3, 4, 5)

# Imprimir la tupla completa
print(mi_tupla)  # Resultado: (1, 2, 3, 4, 5)

# Acceder a un elemento por índice
segundo_elemento = mi_tupla[1]
print(segundo_elemento)  # Resultado: 2

# Intentar modificar un elemento (genera un error)
mi_tupla[1] = 10
print(mi_tupla)  # Resultado: Error: 'tuple' object does not support item assignment
```

### Diccionarios

---

**¿Qué son los diccionarios?**

Los diccionarios son estructuras de datos que almacenan **colecciones de pares de clave-valor**. A diferencia de las listas, donde cada elemento es independiente, en los diccionarios cada elemento asocia una **clave** (identificador) con un **valor** (información).

**Características:**

- **Ordenados:** Los diccionarios mantienen un orden interno, pero no es garantizado.
- **Mutables:** Se pueden modificar después de su creación.
- **Útiles para:**
    - Almacenar datos relacionados.
    - Configurar opciones.
    - Representar datos en formato JSON.

**Errores comunes:**

- **Comas en lugar de punto y coma:** Al definir múltiples pares.
- **Corchetes en lugar de llaves:** Al definir el diccionario.
- **Llaves sin mayúscula:** Si se desea usar claves sensibles a mayúsculas/minúsculas.

**¿Cómo se definen?**

Se utilizan llaves `{}` y cada par clave-valor se separa por comas. La clave se escribe entre comillas y se separa del valor con dos puntos `:`.

```python
persona = {
    "nombre": "Juan",
    "edad": 30,
    "genero": "Masculino"
}
```

**Cómo acceder a los valores?**

Se utiliza la clave entre corchetes `[]`.

```python
edad = persona["edad"]
print(edad)  # Resultado: 30
```

## Operaciones con diccionarios

**Características:**

- Las operaciones son eficientes.
- Permiten modificar la estructura del diccionario dinámicamente.
- Son útiles para actualizar y gestionar datos de forma organizada.

**Modificar un elemento:**

- Se utiliza la clave entre corchetes y se le asigna un nuevo valor.

```python
persona = {"nombre": "Juan", "edad": 30}
persona["nombre"] = "Pedro"

print(persona)  # Resultado: {"nombre": "Pedro", "edad": 30}
```

**Agregar un nuevo elemento:**

- Se utiliza la clave entre corchetes y se le asigna un valor.

```python
persona["genero"] = "Masculino"

print(persona)  # Resultado: {"nombre": "Pedro", "edad": 30, "genero": "Masculino"
```

**Eliminar un elemento:**

- Se utiliza la palabra clave `del` seguida de la clave entre corchetes.

```python
del persona["nombre"]

print(persona)  # Resultado: {"edad": 30, "genero": "Masculino"}
```

## Métodos de diccionarios en Python

**Método `keys()`:**

- Obtiene una lista con las **llaves** del diccionario.
- Útil para verificar la existencia de llaves o recorrerlas.

```python
persona = {"nombre": "Juan", "edad": 30, "genero": "Masculino"}

llaves = persona.keys()
print(llaves)  # Resultado: dict_keys(['nombre', 'edad', 'genero'])
```

**Método `values()`:**

- Obtiene una lista con los **valores** del diccionario.
- Útil para verificar la existencia de valores o procesarlos.

```python
valores = persona.values()
print(valores)  # Resultado: dict_values(['Juan', 30, 'Masculino'])
```

**Método `items()`:**

- Obtiene una lista de **tuplas** con llaves y valores.
- Útil para iterar sobre ambos simultáneamente.

```python
items = persona.items()
print(items)  # Resultado: [('nombre', 'Juan'), ('edad', 30), ('genero', 'Masculino')]
```

**Método `pop()`:**

- Elimina un elemento por su **llave** y devuelve su valor.
- Útil para eliminar y obtener un elemento a la vez.

```python
valor_eliminado = persona.pop("nombre")
print(valor_eliminado)  # Resultado: 'Juan'
print(persona)  # Resultado: {'edad': 30, 'genero': 'Masculi
```