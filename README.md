# 📚 Tema 2: Métodos de Solución de Ecuaciones

Este tema abarca diferentes métodos numéricos para encontrar raíces de funciones no lineales. La raíz de una función $f(x)$ es el valor de $x$ que hace que $f(x) = 0$. Los métodos se dividen en dos grandes categorías: **métodos cerrados** y **métodos abiertos**.

---

## 📦 Contenido

- 📁 `MetodosCerrados/`: Métodos que requieren un intervalo con un cambio de signo ($f(a) \cdot f(b) < 0$).
  - Método de Bisección
  - Método de la Regla Falsa

- 📁 `MetodosAbiertos/`: Métodos que no necesitan un intervalo inicial, solo uno o dos valores de inicio.
  - Método del Punto Fijo
  - Método de Newton-Raphson
  - Método de la Secante

---

## 🔍 Comparación General

| Característica         | Métodos Cerrados               | Métodos Abiertos                      |
|------------------------|--------------------------------|----------------------------------------|
| Requieren intervalo    | Sí ($f(a) \cdot f(b) < 0$)     | No, solo valores iniciales            |
| Convergencia           | Lenta pero garantizada         | Rápida, pero no siempre garantizada   |
| Implementación         | Sencilla                       | Puede requerir derivadas              |
| Ejemplos               | Bisección, Regla Falsa         | Punto Fijo, Newton-Raphson, Secante   |

---

## 🎯 Objetivo del Tema

El objetivo de este tema es que el estudiante:
- Comprenda la diferencia entre métodos cerrados y abiertos.
- Aplique cada método correctamente según el tipo de función y condiciones iniciales.
- Evalúe ventajas y desventajas de cada técnica.
- Analice la **convergencia** y **eficiencia** de cada método.

---

## 📌 Recomendaciones

- Graficar la función antes de aplicar cualquier método.
- Verificar que se cumplan las condiciones de uso de cada método.
- Comparar el número de iteraciones requeridas por cada técnica.

---

## 🧮 Notación

- $x_r$: Aproximación de la raíz.
- $f(x)$: Función evaluada.
- $x_n$: Iteración actual.
- $x_{n+1}$: Siguiente iteración.
