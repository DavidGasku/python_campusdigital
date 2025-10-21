# 01 - Variables y Tipos de Datos

## Mostrar información con print()

Antes de trabajar con variables, necesitamos saber cómo mostrar información en pantalla. En Python usamos la función `print()`:

```python
print("Hola, mundo!")
print("Mi primer programa en Python")
print(42)
print(3.14)
```

**Características de print():**
- Muestra texto o números en la pantalla
- Cada `print()` aparece en una línea nueva
- El texto va entre comillas (`"` o `'`)
- Los números van sin comillas

```python
# Mostrar diferentes tipos de datos
print("Esto es texto")
print(123)
print(45.67)
print(True)

# Mostrar varias cosas en un solo print()
print("El resultado es:", 10 + 5)
print("Tu edad es", 25, "años")
```

### Diferentes formas de imprimir

**1. Print básico**
```python
print("Hola")
print(42)
```

**2. Print con múltiples valores**
```python
nombre = "Ana"
edad = 25
print("Nombre:", nombre, "Edad:", edad)
# Salida: Nombre: Ana Edad: 25
```

**3. F-strings (forma moderna y recomendada)**
```python
nombre = "Ana"
edad = 25
print(f"Mi nombre es {nombre} y tengo {edad} años")
# Salida: Mi nombre es Ana y tengo 25 años

precio = 19.99
print(f"El precio es {precio:.2f} euros")
# Salida: El precio es 19.99 euros
```

**4. Método .format()**
```python
nombre = "Ana"
edad = 25
print("Mi nombre es {} y tengo {} años".format(nombre, edad))
# Salida: Mi nombre es Ana y tengo 25 años
```

**5. Concatenación de strings**
```python
nombre = "Ana"
edad = "25"  # Debe ser string para concatenar
print("Mi nombre es " + nombre + " y tengo " + edad + " años")
# Salida: Mi nombre es Ana y tengo 25 años
```

**6. Print con separadores personalizados**
```python
print("rojo", "verde", "azul", sep="-")
# Salida: rojo-verde-azul

print("Línea 1", end=" ")
print("Línea 2")
# Salida: Línea 1 Línea 2 (en la misma línea)
```

**💡 Recomendación:** Usa **f-strings** siempre que puedas, es la forma más clara y eficiente.

## ¿Qué es una variable?

Una variable es como una **caja** donde guardamos información para usarla después. En Python no hace falta declararlas, solo asignar un valor.

## Tipos de datos básicos

### 1. Strings (texto)

Texto entre comillas simples o dobles:

```python
nombre = "Ana"
ciudad = 'Madrid'
mensaje = "Hola, mundo!"
```

### 2. Integers (números enteros)

Números sin decimales:

```python
edad = 25
puntos = 100
temperatura = -5
```

### 3. Floats (números decimales)

Números con decimales:

```python
altura = 1.75
precio = 19.99
pi = 3.14159
```

### 4. Booleans (verdadero/falso)

Solo dos valores posibles: `True` o `False`

```python
es_estudiante = True
tiene_carnet = False
esta_lloviendo = False
```

## Ejemplos básicos

```python
# Crear variables
nombre = "Carlos"
edad = 30
altura = 1.80
es_programador = True

# Usar variables
print(nombre)
print(edad)

# Cambiar el valor de una variable
edad = 31
print(edad)

# Usar variables en operaciones
precio = 10
cantidad = 3
total = precio * cantidad
print(total)  # 30
```

## Ver el tipo de una variable con type()

Usa `type()` para saber qué tipo de dato es una variable:

```python
nombre = "Ana"
edad = 25
altura = 1.65
es_estudiante = True

print(type(nombre))        # <class 'str'>
print(type(edad))          # <class 'int'>
print(type(altura))        # <class 'float'>
print(type(es_estudiante)) # <class 'bool'>

# Útil para debugging
dato = "25"
print(type(dato))  # <class 'str'> - es texto, no número!
```

## Pedir datos al usuario con input()

Puedes pedir al usuario que escriba datos usando `input()`:

```python
# Pedir el nombre (siempre devuelve string)
nombre = input("¿Cómo te llamas? ")
print(f"Hola, {nombre}!")

# Pedir un número (convertir de string a int)
edad_str = input("¿Cuántos años tienes? ")
edad = int(edad_str)  # Convertir a entero
print(f"El próximo año tendrás {edad + 1} años")

# Forma corta (convertir directamente)
altura = float(input("¿Cuánto mides en metros? "))
print(f"Mides {altura} metros")
```

**⚠️ Recuerda:** `input()` siempre devuelve un string. Si necesitas un número, usa `int()` o `float()`.

## Reglas para nombres de variables

✅ **Permitido:**
- Letras (a-z, A-Z)
- Números (pero no al inicio)
- Guión bajo (_)

❌ **No permitido:**
- Empezar con número
- Espacios
- Caracteres especiales (@, #, $, etc.)

```python
# ✅ Bien
nombre = "Ana"
edad_usuario = 25
precio_total = 100
dato1 = "valor"

# ❌ Mal
1nombre = "Ana"      # Empieza con número
edad usuario = 25    # Tiene espacio
precio-total = 100   # Guión medio no permitido
```

## Buenas prácticas

- Usa nombres **descriptivos**: `edad` mejor que `e`
- Usa **minúsculas** con guiones bajos: `nombre_completo`
- Sé **consistente** con tu estilo

---

## 📝 Ejercicios

### Ejercicio 1: Tus datos personales con input()

Pide al usuario:
- Su nombre
- Su edad (convertir a int)
- Su altura en metros (convertir a float)
- Si es estudiante (responder "si" o "no")

Imprime toda la información y el tipo de cada variable con `type()`.

**Ejemplo de ejecución:**
```
¿Cómo te llamas? Ana
¿Cuántos años tienes? 25
¿Cuánto mides en metros? 1.65
¿Eres estudiante? (si/no): si

Tus datos:
Nombre: Ana (tipo: <class 'str'>)
Edad: 25 (tipo: <class 'int'>)
Altura: 1.65 (tipo: <class 'float'>)
Estudiante: True (tipo: <class 'bool'>)
```

---

## 💡 Tips

- Para ver el tipo de una variable usa: `type(variable)`
- Para imprimir con formato usa f-strings: `print(f"Edad: {edad}")`
- Python es sensible a mayúsculas: `Nombre` y `nombre` son diferentes
- `input()` siempre devuelve string, conviértelo si necesitas número

## 🎯 Resumen

- Las variables guardan información
- Tipos principales: `str`, `int`, `float`, `bool`
- `type()` muestra el tipo de dato
- `input()` pide datos al usuario (siempre devuelve string)
- Usa `int()` o `float()` para convertir strings a números
