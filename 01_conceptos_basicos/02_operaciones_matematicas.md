# 02 - Operaciones Matemáticas

## Operaciones básicas

Python puede hacer cálculos como una calculadora.

### Suma (+)
```python
resultado = 10 + 5  # 15
print(resultado)
```

### Resta (-)
```python
resultado = 10 - 5  # 5
print(resultado)
```

### Multiplicación (*)
```python
resultado = 10 * 5  # 50
print(resultado)
```

### División (/)
```python
resultado = 10 / 5  # 2.0 (siempre devuelve float)
print(resultado)
```

## Operaciones especiales

### División entera (//)
Divide y elimina los decimales:
```python
resultado = 10 // 3  # 3 (no 3.333...)
resultado = 17 // 5  # 3 (no 3.4)
```

### Módulo (%) - Resto de la división
```python
resultado = 10 % 3   # 1 (10 dividido 3 da 3, y sobra 1)
resultado = 15 % 4   # 3 (15 dividido 4 da 3, y sobran 3)

# Útil para saber si un número es par
numero = 8
resto = numero % 2   # 0 → es par
```

### Potencia (**)
```python
resultado = 2 ** 3   # 8 (2 elevado a 3)
resultado = 5 ** 2   # 25 (5 al cuadrado)
resultado = 10 ** 0  # 1 (cualquier número elevado a 0 es 1)
```

## Orden de operaciones

Python sigue las reglas matemáticas (PEMDAS):
1. **P**aréntesis
2. **E**xponentes (potencias)
3. **M**ultiplicación / **D**ivisión
4. **A**dición / **S**ustracción

```python
resultado = 2 + 3 * 4      # 14 (primero 3*4=12, luego 2+12=14)
resultado = (2 + 3) * 4    # 20 (primero paréntesis 2+3=5, luego 5*4=20)
resultado = 10 / 2 + 3     # 8.0 (primero 10/2=5, luego 5+3=8)
```

## Operaciones con variables

```python
precio = 100
descuento = 20
precio_final = precio - descuento
print(precio_final)  # 80

base = 5
altura = 3
area = base * altura
print(area)  # 15
```

## Modificar variables

### Forma larga
```python
puntos = 10
puntos = puntos + 5  # Suma 5 a los puntos actuales
print(puntos)  # 15
```

### Forma corta (operadores compuestos)
```python
puntos = 10
puntos += 5   # Equivale a: puntos = puntos + 5
print(puntos) # 15

puntos -= 3   # Equivale a: puntos = puntos - 3
puntos *= 2   # Equivale a: puntos = puntos * 2
puntos /= 4   # Equivale a: puntos = puntos / 4
```

## Usando input() con operaciones

```python
# Calculadora simple con input()
num1 = float(input("Primer número: "))
num2 = float(input("Segundo número: "))

suma = num1 + num2
resta = num1 - num2
multiplicacion = num1 * num2
division = num1 / num2

print(f"Suma: {suma}")
print(f"Resta: {resta}")
print(f"Multiplicación: {multiplicacion}")
print(f"División: {division}")
```

---

## 📝 Ejercicios

### Ejercicio 1: Calculadora básica con input()

Pide al usuario dos números.
Calcula e imprime:
- La suma
- La resta
- La multiplicación
- La división

---

### Ejercicio 2: Calculadora de propina con input()

Pide al usuario el total de una cuenta de restaurante.
Pide el porcentaje de propina que quiere dejar (ej: 15 para 15%).

Calcula:
- La propina (cuenta × porcentaje / 100)
- El total a pagar (cuenta + propina)

---

### Ejercicio 3: Conversor de temperatura con input()

Pide al usuario una temperatura en Celsius.
Conviértela a Fahrenheit usando la fórmula:

**Fahrenheit = (Celsius × 9/5) + 32**

---

### Ejercicio 4: Área y perímetro de un círculo con input()

Pide al usuario el radio de un círculo.
Usa `pi = 3.14159`

Calcula:
- Área = π × radio²
- Perímetro = 2 × π × radio

---

### Ejercicio 5: Repartir en partes iguales con input()

Pide al usuario:
- Cantidad total de caramelos
- Número de amigos

Calcula:
- ¿Cuántos caramelos recibe cada amigo? (división entera)
- ¿Cuántos caramelos sobran? (módulo)

---

### Ejercicio 6: Calculadora de potencias con input()

Pide al usuario:
- Un número base
- Un exponente

Calcula y muestra el resultado de base elevado al exponente.

---

### Ejercicio 7: Precio final con IVA con input()

Pide al usuario el precio de un producto (sin IVA).
Calcula el precio con IVA del 21% (precio × 1.21).
Muestra ambos precios.

---

### Ejercicio 8: Contador de puntos con operadores compuestos

Crea una variable `puntos = 0`.

Pide al usuario cuántos puntos gana en cada ronda (3 rondas).
Usa el operador `+=` para ir sumando los puntos.

Muestra los puntos después de cada ronda y el total final.

**Ejemplo:**
```
Puntos iniciales: 0
¿Puntos ganados en ronda 1? 10
Puntos actuales: 10
¿Puntos ganados en ronda 2? 25
Puntos actuales: 35
¿Puntos ganados en ronda 3? 15
Puntos finales: 50
```

---

## 💡 Tips

- La división (`/`) siempre devuelve un float, incluso si el resultado es entero
- Usa paréntesis cuando tengas dudas sobre el orden
- El operador `%` es muy útil para saber si un número es par: `numero % 2 == 0`
- Los operadores compuestos (`+=`, `-=`, etc.) hacen el código más corto

## 🎯 Resumen

| Operador | Operación | Ejemplo | Resultado |
|----------|-----------|---------|-----------|
| + | Suma | 5 + 3 | 8 |
| - | Resta | 5 - 3 | 2 |
| * | Multiplicación | 5 * 3 | 15 |
| / | División | 5 / 2 | 2.5 |
| // | División entera | 5 // 2 | 2 |
| % | Módulo (resto) | 5 % 2 | 1 |
| ** | Potencia | 5 ** 2 | 25 |
| += | Incremento | x += 5 | x = x + 5 |
