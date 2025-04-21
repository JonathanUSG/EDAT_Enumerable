# 📘 Preguntas y Respuestas sobre el Problema de Desintegración Radiactiva

Este documento recopila las preguntas más comunes relacionadas con el modelado matemático de la desintegración radiactiva, resolviendo paso a paso el proceso mediante ecuaciones diferenciales y transformadas de Laplace.

---

## 📌 1. ¿Qué tipo de ecuación diferencial se utiliza para modelar la desintegración radiactiva?

Una **ecuación diferencial lineal de primer orden**:

$$
\frac{dN}{dt} = -kN
$$

donde:

- $N(t)$ es la cantidad de material radiactivo en el tiempo $t$.
- $k$ es la **constante de desintegración**.

---

## 📌 2. ¿Por qué el signo en la ecuación diferencial es negativo?

El signo negativo indica que la cantidad de material **disminuye con el tiempo**, ya que la desintegración reduce la masa original.

---

## 📌 3. ¿Cuál es la condición inicial dada en el problema?

La **condición inicial** es:

$$
N(0) = N_0
$$

donde $N_0$ representa la masa inicial del material.

---

## 📌 4. ¿Qué información proporciona la condición en $t = 1$?

Se indica que el **10% del material se ha desintegrado** tras una hora:

$$
N(1) = 0.9N_0
$$

---

## 📌 5. ¿Por qué se usa la transformada de Laplace para resolver este problema?

La **transformada de Laplace** convierte ecuaciones diferenciales en algebraicas, lo cual:

- Facilita el tratamiento de condiciones iniciales.
- Permite una resolución sistemática.

---

## 📌 6. ¿Cuál es la transformada de Laplace de $\frac{dN}{dt}$?

$$
\mathcal{L}\left\{\frac{dN}{dt}\right\} = s \bar{N}(s) - N_0
$$

---

## 📌 7. ¿Qué resulta al aplicar la transformada al lado derecho de $\frac{dN}{dt} = -kN$?

$$
\mathcal{L}\left\{-kN(t)\right\} = -k \bar{N}(s)
$$

---

## 📌 8. ¿Cuál es la expresión de $\bar{N}(s)$ tras resolver la ecuación algebraica?

$$
\bar{N}(s) = \frac{N_0}{s + k}
$$

---

## 📌 9. ¿Cómo se obtiene $N(t)$ a partir de $\bar{N}(s)$?

Aplicando la **transformada inversa de Laplace**:

$$
\mathcal{L}^{-1}\left\{\frac{1}{s + k}\right\} = e^{-kt}
$$

Por lo tanto:

$$
N(t) = N_0 e^{-kt}
$$

---

## 📌 10. ¿Cómo se usa la condición $N(1) = 0.9N_0$ para encontrar $k$?

Sustituyendo en la solución:

$$
0.9N_0 = N_0 e^{-k} \Rightarrow e^{-k} = 0.9 \Rightarrow k = -\ln(0.9)
$$

---

## 📌 11. ¿Qué valor aproximado tiene $k$?

$$
k \approx -\ln(0.9) \approx 0.10536
$$

---

## 📌 12. ¿Qué es la vida media en este contexto?

Es el tiempo $t_{1/2}$ en el cual la cantidad de material se reduce a la mitad:

$$
N(t_{1/2}) = \frac{N_0}{2}
$$

---

## 📌 13. ¿Cómo se deriva la fórmula de la vida media?

Desde:

$$
\frac{N_0}{2} = N_0 e^{-k t_{1/2}} \Rightarrow e^{-k t_{1/2}} = \frac{1}{2} \Rightarrow k t_{1/2} = \ln 2
$$

Entonces:

$$
t_{1/2} = \frac{\ln 2}{k}
$$

---

## 📌 14. ¿Cuál es la expresión exacta de la vida media en este problema?

$$
t_{1/2} = \frac{\ln 2}{-\ln(0.9)} = \frac{\ln 2}{\ln\left(\frac{10}{9}\right)}
$$

---

## 📌 15. ¿Cuál es el valor numérico aproximado de la vida media?

$$
t_{1/2} \approx \frac{0.69315}{0.10536} \approx 6.579 \text{ horas}
$$

---

## 📌 16. ¿Por qué no es necesario conocer $N_0$ explícitamente?

Porque $N_0$ se **cancela en las proporciones** al sustituir condiciones como:

- $N(1) = 0.9N_0$
- $N(t_{1/2}) = \frac{N_0}{2}$

---

## 📌 17. ¿Qué tipo de función es $N(t) = N_0 e^{-kt}$?

Una **función exponencial decreciente**.

---

## 📌 18. ¿Cómo se verifica que la solución satisface la condición en $t = 1$?

Sustituyendo $k = -\ln(0.9)$:

$$
N(1) = N_0 e^{-(-\ln(0.9))} = N_0 e^{\ln(0.9)} = 0.9N_0
$$

---

## 📌 19. ¿Qué representa físicamente la constante $k$?

La constante de desintegración $k$ representa **la rapidez con la que el material se desintegra**.

---

## 📌 20. ¿Qué pasaría si el 20% del material se desintegrara en una hora?

Tendríamos:

$$
e^{-k} = 0.8 \Rightarrow k = -\ln(0.8)
$$

Y la vida media sería:

$$
t_{1/2} = \frac{\ln 2}{-\ln(0.8)}
$$

Este valor sería **menor**, indicando una desintegración **más rápida**.

---

### 📎 Nota final

Este problema representa un clásico modelo matemático aplicado a la física nuclear y a otros contextos donde se presentan procesos de decaimiento exponencial.
