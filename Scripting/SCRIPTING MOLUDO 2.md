# SCRIPTING: MOLUDO **2**

## Unidad 1. Variables y operadores

---

Las variables son espacios en la memoria de la computadora que almacenan valores. Estos valores pueden ser utilizados para realizar operaciones, modificar el flujo del programa o evaluar condiciones.

En Python, las variables se clasifican en diferentes tipos:

- Numéricos: Enteros (ej: 1, 2, 3) y decimales (ej: 1.5, 3.14)
- Texto: Cadenas de caracteres (ej: "Hola", "Mundo")
- Lógicos: Verdadero o Falso
- Complejos: Números complejos (ej: 3+4j)

Cada tipo de variable tiene sus propias características y se utiliza para almacenar diferentes tipos de información. Es importante elegir el tipo de variable adecuado para cada dato que se quiera almacenar, ya que esto puede afectar el rendimiento del programa.

Las variables se declaran utilizando el nombre de la variable seguido del signo de igual (=) y el valor que se le quiere asignar

Enteros (int): como su nombre indica, son números enteros. Es decir, un número sin parte fraccionaria o decimal. 
Flotante (float): a diferencia del tipo de dato anterior, un número flotante contiene (o es capaz de contener) una componente fraccionaria. 
Cadena de texto (str): las cadenas se utilizan cuando se desea o se necesita procesar texto en lugar de números. Siempre se debe usar comillas (ya sea doble o simple) para definir. 
Booleanos (bool): este tipo de dato solo acepta dos valores posibles, “True” o “False”. Los valores booleanos son útiles principalmente para evaluar si una condición se cumple o no, y actuar en consecuencia al resultado.
Valor nulo (none): el valor nulo no es realmente un tipo de dato en sí, pero vale la pena mencionarlo dentro de esta clasificación. Su uso aplica principalmente cuando se desea especificar que una variable no tiene valor, y asignarle el valor 0 o -1 sería algo ambiguo. En esos escenarios, este objetivo se puede cumplir asignando el valor “None”.

### Definiendo las variables en Python

---

En Python, las variables no tienen un tipo de dato predefinido. El tipo de dato se asigna automáticamente según el valor que se le asigne a la variable. Esto se conoce como tipado dinámico.

```python
edad = 30  # Variable de tipo entero
nombre = "Juan"  # Variable de tipo cadena de caracteres
pi = 3.14159  # Variable de tipo decimal

print(type(edad))  # Mostrará: <class 'int'>
print(type(nombre))  # Mostrará: <class 'str'>
print(type(pi))  # Mostrará: <class 'float'>
```

**Ventajas del tipado dinámico:**

- Simplifica la sintaxis del código.
- Permite mayor flexibilidad en la programación.

**Desventajas del tipado dinámico:**

- Puede generar errores en tiempo de ejecución si no se maneja adecuadamente.
- Dificulta la detección de errores en la fase de compilación.

### Conversión de datos

---

Las funciones de conversión de tipos en Python permiten transformar variables de un tipo de dato a otro. Estas funciones son esenciales para manipular datos de manera eficiente y obtener los resultados deseados en nuestros programas. A continuación, se detalla cada función junto con ejemplos de uso:

1. int(): Convierte a entero

La función `int()` convierte su argumento a un número entero. Si el argumento ya es un entero, lo devuelve sin modificarlo.

```python
numero_decimal = 10.5

# Convertir a entero
numero_entero = int(numero_decimal)
print(numero_entero)  # Mostrará: 10

# Convertir una cadena de caracteres a entero
cadena_numerica = "20"
numero_entero = int(cadena_numerica)
print(numero_entero)  # Mostrará: 20
```

**2. float(): Convierte a decimal**

La función `float()` convierte su argumento a un número decimal. Si el argumento ya es un decimal, lo devuelve sin modificarlo.

```python
numero_entero = 5

# Convertir a decimal
numero_decimal = float(numero_entero)
print(numero_decimal)  # Mostrará: 5.0

# Convertir una cadena de caracteres a decimal
cadena_numerica = "3.14"
numero_decimal = float(cadena_numerica)
print(numero_decimal)  # Mostrará: 3.14
```

**3. str(): Convierte a cadena de caracteres**

La función `str()` convierte su argumento a una cadena de caracteres (string).

```python
numero_entero = 42

# Convertir a cadena de caracteres
cadena_texto = str(numero_entero)
print(cadena_texto)  # Mostrará: '42'

# Convertir un booleano a cadena de caracteres
verdadero = True
cadena_texto = str(verdadero)
print(cadena_texto)  # Mostrará: 'True'
```

**4. bool(): Convierte a booleano (Verdadero o Falso)**

La función `bool()` convierte su argumento a un valor booleano (Verdadero o Falso).

```python
numero_entero = 0

# Convertir a booleano
valor_booleano = bool(numero_entero)
print(valor_booleano)  # Mostrará: False

cadena_texto = "Hola"

# Convertir a booleano
valor_booleano = bool(cadena_texto)
print(valor_booleano)  # Mostrará: Tr
```

**5. list(): Convierte a lista**

La función `list()` convierte su argumento a una lista. Si el argumento ya es una lista, lo devuelve sin modificarlo.

```python
tupla = (1, 2, 3)

# Convertir a lista
lista_numeros = list(tupla)
print(lista_numeros)  # Mostrará: [1, 2, 3]

cadena_texto = "Hola Mundo"

# Convertir a lista de caracteres
lista_caracteres = list(cadena_texto)
print(lista_caracteres)  # Mostrará: ['H', 'o', 'l', 'a', ' ', 'M', 'u', 'n', 'd', 'o']
```

**6. tuple(): Convierte a tupla**

La función `tuple()` convierte su argumento a una tupla. Si el argumento ya es una tupla, lo devuelve sin modificarlo.

```python
Python
lista_numeros = [1, 2, 3]

# Convertir a tupla
tupla_numeros = tuple(lista_numeros)
print(tupla_numeros)  # Mostrará: (1, 2, 3)

cadena_texto = "Hola Mundo"

# Convertir a tupla de caracteres
tupla_caracteres = tuple(cadena_texto)
print(tupla_caracteres)  # Mostrará: ('H', 'o', 'l', 'a', ' ', 'M', 'u', 'n', 'd', 'o')
```

**7. set(): Convierte a conjunto**

La función `set()` convierte su argumento a un conjunto. Si el argumento ya es un conjunto, lo devuelve sin modificarlo.

```python
conjunto_vacio = set()  # Crea un conjunto vacío
conjunto_numeros = set({1, 2, 3, 4})  # Crea un conjunto con elementos
conjunto_cadena = set("Hola Mundo")  # Crea un conjunto con caracteres únicos de una cadena
```

## Funciones

---

Las funciones se definen utilizando la palabra clave `def` seguida del nombre de la función, paréntesis (pueden contener argumentos), dos puntos y el bloque de código de la función.
**Las funciones en Python son bloques de código reutilizables que realizan tareas específicas.** Permiten organizar el código de manera modular, haciendo que los programas sean más fáciles de leer, entender y mantener.

```python
# EJEMPLO
def nombre_funcion(argumento1, argumento2):
    """
    Documentación de la función

    Ejemplo:
    nombre_funcion(arg1, arg2)
    """

    # Bloque de código de la función
    pass

# EJEMPLO 
def calcular_area_rectangulo(base, altura):
    """
    Calcula el área de un rectángulo.

    Argumentos:
        base: La longitud de la base del rectángulo (número).
        altura: La longitud de la altura del rectángulo (número).

    Retorna:
        El área del rectángulo (número).
    """

    area = base * altura
    return area

# Ejemplo de uso
base = 5
altura = 3

area_rectangulo = calcular_area_rectangulo(base, altura)
print(f"El área del rectángulo es: {area_rectangulo}")  # Mostrará: El área del rectángulo es: 15
```

### Devolver resultado de una función

**Las funciones en Python pueden devolver valores como resultado de su ejecución.** Estos valores pueden ser utilizados en otras partes del programa o asignados a variables, para devolver un valor, se utiliza la palabra clave `return` seguida de la expresión que contiene el valor que se quiere devolver.

- El valor devuelto por una función puede ser utilizado en otras partes del programa o asignado a variables.
- Una función solo puede devolver un valor.
- Si una función no necesita devolver un valor, se puede utilizar la palabra clave `pass` en su lugar pero no es lo idóneo.

```python
# EJEMPLO
def nombre_funcion(argumento1, argumento2):
    """
    Documentación de la función

    Ejemplo:
    valor_devuelto = nombre_funcion(arg1, arg2)
    """

    # Bloque de código de la función

    # Calcular el valor a devolver
    valor_a_devolver = ...

    # Devolver el valor
    return valor_a_devolver
   
# EJEMPLO
def calcular_area_triangulo(base, altura):
    """
    Calcula el área de un triángulo.

    Argumentos:
        base: La longitud de la base del triángulo (número).
        altura: La longitud de la altura del triángulo (número).

    Retorna:
        El área del triángulo (número).
    """

    area = (base * altura) / 2
    return area

# Ejemplo de uso
base = 6
altura = 4

area_triangulo = calcular_area_triangulo(base, altura)
print(f"El área del triángulo es: {area_triangulo}")  # Mostrará: El área del triángulo es: 12.0
```

### Funciones integradas

Las funciones integradas en Python son funciones que ya vienen predefinidas en el lenguaje y no necesitan importarse de ninguna biblioteca. Estas funciones son de gran utilidad para realizar tareas comunes de programación, como trabajar con datos, cadenas de texto, entrada y salida, etc.

**Beneficios del uso de funciones integradas:**

- **Facilidad de uso:** No es necesario importar módulos adicionales.
- **Eficiencia:** Las funciones integradas están optimizadas para su uso dentro del lenguaje.
- **Claridad del código:** El código es más legible y fácil de entender.

Ejemplos de funciones integradas en Python

- **`print()`:** Imprime un mensaje en la consola.
- **`input()`:** Obtiene un valor del usuario y lo devuelve como cadena de texto.
- **`type()`:** Devuelve el tipo de dato de un objeto.
- **`int()`:** Convierte un valor a un número entero.
- **`float()`:** Convierte un valor a un número decimal.
- **`str()`:** Convierte un valor a una cadena de texto.
- **`len()`:** Devuelve la longitud de una secuencia (cadena de texto, lista, etc.).
- **`range()`:** Genera una secuencia de números enteros.
- **`list()`:** Crea una lista a partir de un iterable.
- **`tuple()`:** Crea una tupla a partir de un iterable.
- **`set()`:** Crea un conjunto a partir de un iterable.
- **`abs()`:** Devuelve el valor absoluto de un número.
- **`pow()`:** Eleva un número a una potencia.
- **`round()`:** Redondea un número a un número decimal específico.