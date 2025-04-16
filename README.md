# Tema 1: Investigación – Error Absoluto y Error Relativo

## 📌 Introducción

En el ámbito de los métodos numéricos, **los errores** son inevitables debido a la naturaleza aproximada de los cálculos realizados. Dos de los conceptos fundamentales para medir la precisión de una aproximación son el **error absoluto** y el **error relativo**. Ambos permiten evaluar qué tan lejos está un valor calculado de un valor verdadero o exacto.

---

## 📐 Error Absoluto

### 🔹 Definición

El **error absoluto** se define como la **diferencia en valor absoluto** entre el valor exacto o verdadero y el valor aproximado.

\[
\text{Error absoluto} = | \text{Valor verdadero} - \text{Valor aproximado} |
\]

### 🔹 Características

- Se expresa en **las mismas unidades** que la cantidad que se está midiendo.
- No toma en cuenta la **magnitud del valor exacto**.
- Es útil para saber **cuánto se ha desviado** el resultado.

### 🔹 Ejemplo

Si el valor exacto es `5.00` y el valor aproximado es `4.83`, el error absoluto es:

\[
| 5.00 - 4.83 | = 0.17
\]

---

## 📏 Error Relativo

### 🔹 Definición

El **error relativo** mide la proporción del error absoluto respecto al valor exacto. Es más útil cuando se comparan errores de diferentes magnitudes.

\[
\text{Error relativo} = \frac{|\text{Valor verdadero} - \text{Valor aproximado}|}{|\text{Valor verdadero}|}
\]

Este resultado **puede expresarse como porcentaje** multiplicando por 100.

\[
\text{Error relativo porcentual} = \left( \frac{|\text{Valor verdadero} - \text{Valor aproximado}|}{|\text{Valor verdadero}|} \right) \times 100\%
\]

### 🔹 Características

- Es **adimensional** (sin unidades).
- Permite comparar errores entre valores muy grandes o muy pequeños.
- Indica **cuán significativa es la diferencia** con respecto al valor real.

### 🔹 Ejemplo

Continuando con el caso anterior:

\[
\text{Error relativo} = \frac{0.17}{5.00} = 0.034 = 3.4\%
\]

---

## 📊 Comparación

| Aspecto             | Error Absoluto                  | Error Relativo                       |
|---------------------|----------------------------------|--------------------------------------|
| Fórmula             | \|valor real - valor aproximado\| | \|valor real - valor aproximado\| / \|valor real\| |
| Unidades            | Mismas que la medida            | No tiene unidades                   |
| Uso principal       | Magnitud del error              | Proporcionalidad del error          |
| Afectado por escala | Sí                              | No                                  |

---

## 🧠 Importancia en los Métodos Numéricos

- Permiten **evaluar la precisión** de un resultado.
- Son fundamentales para **establecer tolerancias** en algoritmos iterativos.
- Ayudan a **detectar errores de redondeo o truncamiento**.
- El error relativo es especialmente importante cuando se trabaja con **valores muy pequeños o muy grandes**.

---

## 📚 Conclusión

Tanto el **error absoluto** como el **error relativo** son herramientas esenciales para evaluar la calidad de una solución numérica. Mientras el primero mide la desviación directa, el segundo proporciona una idea de la significancia de esa desviación. Comprender ambos es clave para aplicar correctamente los métodos numéricos y analizar los resultados obtenidos.

---

## 📎 Recursos adicionales

- Chapra, S. C., & Canale, R. P. (2015). *Métodos Numéricos para Ingenieros*.
- Video explicativo: [https://www.youtube.com/watch?v=b7t1SENvuM0](https://www.youtube.com/watch?v=b7t1SENvuM0)
- Ejercicios interactivos: [https://www.symbolab.com/solver/error-calculator](https://www.symbolab.com/solver/error-calculator)
