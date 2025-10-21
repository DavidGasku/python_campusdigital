# 03 - Strings y Texto

## ¿Qué es un string?

Un **string** (cadena de texto) es una secuencia de caracteres. En Python se escriben entre comillas.

```python
nombre = "Ana"
ciudad = 'Barcelona'
mensaje = "Hola, mundo!"
```

Puedes usar comillas simples (`'`) o dobles (`"`), pero sé consistente.

## Concatenar (unir) strings

### Método 1: Con el operador +

```python
nombre = "Carlos"
apellido = "García"
nombre_completo = nombre + " " + apellido
print(nombre_completo)  # Carlos García

saludo = "Hola, " + nombre + "!"
print(saludo)  # Hola, Carlos!
```

### Método 2: f-strings (recomendado) ⭐

Las f-strings son la forma moderna y más legible:

```python
nombre = "Ana"
edad = 25

# Pones 'f' antes de las comillas y las variables entre {}
mensaje = f"Me llamo {nombre} y tengo {edad} años"
print(mensaje)  # Me llamo Ana y tengo 25 años

# Puedes hacer operaciones dentro
puntos = 150
print(f"Tienes {puntos} puntos, el doble sería {puntos * 2}")
```

### Con input()

```python
nombre = input("¿Cómo te llamas? ")
edad = input("¿Cuántos años tienes? ")

# Usando f-strings con input
print(f"Hola {nombre}, tienes {edad} años")
```

## Métodos útiles de strings

Los strings tienen funciones incorporadas llamadas "métodos":

### Cambiar mayúsculas/minúsculas

```python
texto = "hola mundo"

print(texto.upper())       # HOLA MUNDO
print(texto.lower())       # hola mundo
print(texto.capitalize())  # Hola mundo
print(texto.title())       # Hola Mundo
```

### Reemplazar texto

```python
texto = "Me gusta Python"
nuevo = texto.replace("Python", "programar")
print(nuevo)  # Me gusta programar

frase = "hola hola hola"
nueva = frase.replace("hola", "adiós")
print(nueva)  # adiós adiós adiós
```

### Otras operaciones útiles

```python
texto = "Python es genial"

# Contar caracteres
longitud = len(texto)
print(longitud)  # 16

# Comprobar si contiene algo
contiene = "Python" in texto
print(contiene)  # True

contiene_java = "Java" in texto
print(contiene_java)  # False

# Dividir en palabras
palabras = texto.split()
print(palabras)  # ['Python', 'es', 'genial']
```

## Uso práctico con input()

```python
# Convertir input a mayúsculas para comparar
respuesta = input("¿Quieres continuar? (SI/NO): ")
respuesta = respuesta.upper()

if respuesta == "SI":
    print("Continuando...")
else:
    print("Finalizando...")

# O en una línea
respuesta = input("¿Quieres continuar? (SI/NO): ").upper()
```

## Caracteres especiales

```python
# Salto de línea: \n
print("Primera línea\nSegunda línea")

# Tabulación: \t
print("Nombre:\tCarlos")

# Comillas dentro de strings
print("Dijo: \"Hola\"")  # Dijo: "Hola"
print('Dijo: "Hola"')    # Más fácil con comillas simples
```

---

## 📝 Ejercicios

### Ejercicio 1: Presentación personalizada con input()

Pide al usuario:
- Su nombre
- Su ciudad
- Su edad

Usando f-strings, muestra:
"Hola, soy [nombre], tengo [edad] años y vivo en [ciudad]"

---

### Ejercicio 2: Manipular texto con input()

Pide al usuario una frase.
1. Conviértela a mayúsculas
2. Cuenta cuántos caracteres tiene
3. Reemplaza los espacios por guiones bajos (_)

Muestra el resultado de cada operación.

---

### Ejercicio 3: Información de película con input()

Pide al usuario:
- Título de una película
- Año de estreno
- Puntuación (0-10)

Muestra con f-strings:
"La película [titulo] ([año]) tiene una puntuación de [puntuacion]/10"

---

### Ejercicio 4: Formatear nombre con input()

Pide al usuario su nombre completo (puede estar en mayúsculas, minúsculas o mezclado).

Formátalo para que cada palabra empiece con mayúscula.
Ejemplo: "juan garcía pérez" → "Juan García Pérez"

**Pista:** Usa el método `.title()`

---

### Ejercicio 5: Creador de email con input()

Pide al usuario:
- Su nombre
- Su apellido
- Dominio del email (ej: "gmail.com")

Crea un email con el formato: `nombre.apellido@dominio`
Todo en minúsculas.

Ejemplo: "Ana García" + "hotmail.com" → "ana.garcia@hotmail.com"

---

### Ejercicio 6: Búsqueda en texto con input()

Pide al usuario:
- Una frase
- Una palabra a buscar en la frase

Comprueba si la palabra está en la frase (usa `in`).
Muestra "La palabra [palabra] SÍ está en la frase" o "NO está".

---

### Ejercicio 7: Contador de vocales con input()

Pide al usuario una palabra.
Cuenta cuántas veces aparece la letra 'a' (usa el método `.count()`).
Muestra el resultado.

**Pista:** `texto.count("a")` cuenta las apariciones de "a"

---

## 💡 Tips

- **f-strings** son la forma preferida para combinar texto y variables
- Los métodos de strings **no modifican** el original, devuelven uno nuevo
- `len()` funciona con cualquier string
- Usa `in` para comprobar si un texto contiene otro
- `.lower()` o `.upper()` son útiles para comparar strings sin importar mayúsculas

## 🎯 Resumen

| Operación | Código | Resultado |
|-----------|--------|-----------|
| Concatenar | `"Hola" + " " + "Ana"` | "Hola Ana" |
| f-string | `f"Hola {nombre}"` | "Hola Ana" |
| Mayúsculas | `"hola".upper()` | "HOLA" |
| Minúsculas | `"HOLA".lower()` | "hola" |
| Title Case | `"hola mundo".title()` | "Hola Mundo" |
| Reemplazar | `"hola".replace("h", "H")` | "Hola" |
| Longitud | `len("hola")` | 4 |
| Contiene | `"la" in "hola"` | True |
| Contar | `"hola".count("o")` | 1 |
