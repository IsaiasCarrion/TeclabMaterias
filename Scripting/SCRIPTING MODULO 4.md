# SCRIPTING: MODULO 4

# Condicionales e iteradores

---

**1. Introducción a los valores booleanos:**

- Los valores booleanos son True o False.
- Se utilizan para representar condiciones que pueden ser ciertas o falsas.
- En Python, se pueden utilizar variables y operadores para comparar valores y determinar si son True o False.

**2. El operador de igualdad (==):**

- Se utiliza para comparar si dos valores son iguales.
- Devuelve True si los valores son iguales, False si no lo son.

```python
2 == 2  # True
"Hola" == "Adios"  # False
```

**3. La sentencia if:**

- Se utiliza para ejecutar un bloque de código si una condición es True.
- La sintaxis es la siguiente:

```python
if condición:
    # Bloque de código a ejecutar si la condición es True

# EJEMPLO
if 2 == 2:
    print("Es correcto")
```

**4. Uso de variables con if:**

- Se pueden utilizar variables para comparar valores en la sentencia if.

```python
numero = 2

if numero == 2:
    print("El valor de la variable es 2")
```

**5. Operadores lógicos:**

- Se utilizan para combinar dos o más condiciones.
- Los operadores lógicos más comunes son:
    - **and:** True si ambas condiciones son True.
    - **or:** True si al menos una condición es True.
    - **not:** Invierte el valor de la condición.

```python
numero = 2
es_par = numero % 2 == 0

if numero > 0 and es_par:
    print("El número es positivo y par")
```

**6. Operador de desigualdad (!=):**

- Se utiliza para comparar si dos valores son diferentes.
- Devuelve True si los valores son diferentes, False si son iguales.

```python
2 != 2  # False
"Hola" != "Adios"  # True
```

**7. Operador mayor que (>):**

- Se utiliza para comparar si un valor es mayor que otro.
- Devuelve True si el valor de la izquierda es mayor que el valor de la derecha, False si es menor o igual.

```python
5 > 3  # True
2 > 5  # False
```

**8. Operador mayor o igual que (>=):**

- Se utiliza para comparar si un valor es mayor o igual que otro.
- Devuelve True si el valor de la izquierda es mayor o igual que el valor de la derecha, False si es menor.

```python
5 >= 3  # True
2 >= 5  # False
5 >= 5  # True
```

**9. Operador menor que (<):**

- Se utiliza para comparar si un valor es menor que otro.
- Devuelve True si el valor de la izquierda es menor que el valor de la derecha, False si es mayor o igual.

```python
3 < 5  # True
5 < 2  # False
```

**10. Operador menor o igual que (<=):**

- Se utiliza para comparar si un valor es menor o igual que otro.
- Devuelve True si el valor de la izquierda es menor o igual que el valor de la derecha, False si es mayor.

```python
3 <= 5  # True
5 <= 2  # False
5 <= 5  # True
```

## Condiciones Anidadas: if/elif/else

---

**1. La instrucción else:**

- Se utiliza para definir una acción alternativa cuando la condición principal de la instrucción if es False.
- La sintaxis es la siguiente:

```python
if condición:
    # Bloque de código a ejecutar si la condición es True
else:
    # Bloque de código a ejecutar si la condición es False
    
#EJEMPLO
numero = 5

if numero == 10:
    print("El número es 10")
else:
    print("El número no es 10")
```

**2. La instrucción elif:**

- Se utiliza para agregar condiciones adicionales a la instrucción if.
- La sintaxis es la siguiente:

```python
if condición1:
    # Bloque de código a ejecutar si la condición1 es True
elif condición2:
    # Bloque de código a ejecutar si la condición1 es False y la condición2 es True
elif condición3:
    # Bloque de código a ejecutar si la condición1 y la condición2 son False y la condición3 es True
else:
    # Bloque de código a ejecutar si todas las condiciones son False

#EJEMPLO
numero = 8

if numero == 10:
    # Si el valor de la variable "numero" es 10, se ejecuta la primera instrucción if y se imprime el mensaje "La variable es 10"
    print("La variable es 10")
elif numero > 6:
		# Si el valor de la variable "numero" no es 10, se evalúa la primera instrucción elif. Si el valor es mayor a 6, se imprime el mensaje "La variable es mayor a 6"
    print("La variable es mayor a 6")
elif numero >= 3:
    # Si el valor de la variable "numero" no es 10 ni mayor a 6, se evalúa la segunda instrucción elif. Si el valor es mayor o igual a 3, se imprime el mensaje "La variable está entre 3 y 6".
    print("La variable está entre 3 y 6")
else:
		# Si el valor de la variable "numero" no es 10, no es mayor a 6 ni mayor o igual a 3, se ejecuta la instrucción else y se imprime el mensaje "La variable es menor a 3".
    print("La variable es menor a 3")   

```

## Expresiones Booleanas Compuestas

---

**1. Operadores lógicos:**

- Se utilizan para combinar dos o más condiciones.
- Los operadores lógicos más comunes son:
    - **and:** True si todas las condiciones son True.
    - **or:** True si al menos una condición es True.
    - **not:** Invierte el valor de la condición.

```python
numero = 7

if numero > 5 and numero < 10:
    print("El número está entre 5 y 10")

```

**2. Uso de operadores lógicos en la instrucción if:**

- Se pueden utilizar operadores lógicos para combinar condiciones en la instrucción if.
- La sintaxis es la siguiente:

```python
if condición1 and condición2 and ...:
    # Bloque de código a ejecutar si todas las condiciones son True
elif condición1 or condición2 or ...:
    # Bloque de código a ejecutar si al menos una condición es True
else:
    # Bloque de código a ejecutar si todas las condiciones son False

#EJEMPLO

kilometraje = 32000
anios_desde_ultimo_service = 2

debe_realizar_service = kilometraje >= 30000 or anios_desde_ultimo_service >= 3

if debe_realizar_service:
    print("Debe realizar service")
else:
    print("No es necesario realizar service")

```

## Iteradores

---

**1. Concepto de iteración:**

- La iteración implica realizar una acción o serie de instrucciones de forma repetida.
- Se utiliza para ejecutar un bloque de código varias veces hasta cumplir una condición o un número específico de veces.
- En Python, existen dos tipos de iteradores principales: el ciclo `while` y el ciclo `for`.

**2. Concepto del ciclo `for`:**

- El ciclo `for` se utiliza para iterar sobre una secuencia de elementos.
- A diferencia del ciclo `while`, no evalúa una condición, sino que ejecuta un bloque de código un número específico de veces o hasta que recorre toda la secuencia.

```python
for variable in secuencia:
    # Bloque de código a ejecutar para cada elemento de la secuencia

# La variable i toma el valor de cada número del 0 al 9 (10 elementos en total).
for i in range(10):
    # Dentro del ciclo, se imprime el valor actual de i.
    print(i)
```

**Función `range()`:**

- La función `range()` genera una secuencia de números enteros.
- Puede usarse dentro del ciclo `for` para especificar la cantidad de iteraciones.

```python
for i in range(start, stop, step):
    # Bloque de código a ejecutar para cada elemento de la secuencia

# start (opcional): El valor inicial de la secuencia (por defecto es 0).
# stop: El valor final de la secuencia (no se incluye).
# step (opcional): La diferencia entre cada número de la secuencia (por defecto es 1).

for i in range(1, 6):
    print(i)
    
# Iteración sobre una lista:
nombres = ["Juan", "María", "Pedro"]

# La variable nombre toma el valor de cada nombre de la lista nombres.
for nombre in nombres:
    # Dentro del ciclo, se imprime un saludo personalizado para cada nombre
    print(f"Hola, {nombre}"
    
# Iteración sobre un diccionario:
persona = {"nombre": "Juan", "edad": 30, "ciudad": "Buenos Aires"}

# La variable clave toma el valor de cada clave del diccionario persona.
for clave, valor in persona.items():
		# La variable valor toma el valor de cada valor del diccionario persona.
		# Dentro del ciclo, se imprime la clave y el valor de cada elemento del diccionario.
    print(f"Clave: {clave}, Valor: {valor}")
```

**3. Ciclo `while`:**

- El ciclo `while` evalúa una condición antes de cada iteración.
- Si la condición es `True`, se ejecuta el bloque de código y se vuelve a evaluar la condición.
- Si la condición es `False`, se finaliza el ciclo.

```python
# La variable contador se inicializa en 1.
contador = 1

# El ciclo while se ejecuta mientras contador sea menor o igual que 10.
while contador <= 10:
    # Dentro del ciclo, se imprime el valor actual de contador y se incrementa en 1.
    print(f"Número: {contador}")
    # El ciclo se repite hasta que contador sea mayor que 10, momento en el que finaliza.
    contador += 1
```

**4. Instrucción `break`:**

- Se utiliza para salir de un ciclo `for` o `while` **inmediatamente**.
- Termina la ejecución del ciclo actual y continúa con la línea de código siguiente al ciclo.

```python
# El ciclo for itera del 0 al 9.
for i in range(10):
		# Si i es igual a 5, se ejecuta la instrucción break.
    if i == 5:
		    # Esto termina el ciclo for y continúa con la línea de código siguiente al ciclo.
        break
    print(i)
```

**5. Instrucción `continue`:**

- Se utiliza para omitir la iteración actual de un ciclo `for` y continuar con la siguiente.
- El resto del bloque de código de la iteración actual se omite.

```python
# El ciclo for itera del 0 al 9
for i in range(10):
		# Si i es par, se ejecuta la instrucción continue.
		# Esto omite la iteración actual y continúa con la siguiente.
    if i % 2 == 0:
        continue
    # Se imprimen los números impares del 0 al 9.
    print(i)

```