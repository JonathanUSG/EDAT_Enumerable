# Tema 1: Error Absoluto y Error Relativo

## 📘 Introducción

En los métodos numéricos, el **error** es una medida de la diferencia entre el valor real (o exacto) y el valor aproximado de una cantidad. Entender y calcular los errores es esencial para evaluar la precisión de los resultados obtenidos mediante aproximaciones numéricas.

Los dos tipos de error más comunes son:

- **Error absoluto**
- **Error relativo**

---

## 🟦 ¿Qué es el Error Absoluto?

El **error absoluto** se refiere a la diferencia en valor absoluto entre el valor verdadero y el valor aproximado.

### 🔹 Fórmula:

$$
\text{Error Absoluto} = |x_{\text{verdadero}} - x_{\text{aproximado}}|
$$

### 🔹 Características:
- Mide cuánto se desvía el valor aproximado del valor exacto.
- Su unidad es la misma que la del valor medido.
- Es útil cuando se necesita saber la magnitud del error en términos reales.

### 🔹 Ejemplo:

Si el valor real es $10.5$ y el valor aproximado es $10.1$:

$$
\text{Error Absoluto} = |10.5 - 10.1| = 0.4
$$

---

## 🟨 ¿Qué es el Error Relativo?

El **error relativo** compara el error absoluto con el valor verdadero, y se expresa a menudo como un porcentaje.

### 🔹 Fórmula:

$$
\text{Error Relativo} = \frac{|x_{\text{verdadero}} - x_{\text{aproximado}}|}{|x_{\text{verdadero}}|}
$$

Si se desea expresar como porcentaje:

$$
\text{Error Relativo (\%)} = \left( \frac{|x_{\text{verdadero}} - x_{\text{aproximado}}|}{|x_{\text{verdadero}}|} \right) \times 100
$$

### 🔹 Características:
- Es una medida adimensional (no tiene unidades).
- Es útil cuando se necesita evaluar el error en términos proporcionales.
- Ayuda a comparar la precisión de resultados en distintas escalas.

### 🔹 Ejemplo:

Con los mismos datos anteriores:

$$
\text{Error Relativo} = \frac{|10.5 - 10.1|}{10.5} = \frac{0.4}{10.5} \approx 0.0381
