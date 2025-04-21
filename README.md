Teoría de Electrónica Digital
3.1 Compuertas Lógicas y Tablas de Verdad
Las compuertas lógicas son los bloques fundamentales de los circuitos digitales. Estas operan con señales binarias (0 y 1) y realizan operaciones lógicas básicas. Cada compuerta tiene una tabla de verdad que describe su comportamiento, mostrando todas las combinaciones posibles de entradas y la salida correspondiente.
Tipos de Compuertas Lógicas

NOT (Inversor): Invierte la entrada.

Símbolo: Un triángulo con un círculo en la salida.
Ecuación: ( Y = \overline{A} )
Tabla de verdad:A | Y
--|--
0 | 1
1 | 0




AND (Y): La salida es 1 solo si todas las entradas son 1.

Símbolo: Forma de "D" con entradas y salida.
Ecuación: ( Y = A \cdot B )
Tabla de verdad (2 entradas):A | B | Y
--|--|--
0 | 0 | 0
0 | 1 | 0
1 | 0 | 0
1 | 1 | 1




OR (O): La salida es 1 si al menos una entrada es 1.

Símbolo: Forma curva con entradas y salida.
Ecuación: ( Y = A + B )
Tabla de verdad (2 entradas):A | B | Y
--|--|--
0 | 0 | 0
0 | 1 | 1
1 | 0 | 1
1 | 1 | 1




NAND (NO Y): Inverso de AND. La salida es 0 solo si todas las entradas son 1.

Ecuación: ( Y = \overline{A \cdot B} )
Tabla de verdad:A | B | Y
--|--|--
0 | 0 | 1
0 | 1 | 1
1 | 0 | 1
1 | 1 | 0




NOR (NO O): Inverso de OR. La salida es 1 solo si todas las entradas son 0.

Ecuación: ( Y = \overline{A + B} )
Tabla de verdad:A | B | Y
--|--|--
0 | 0 | 1
0 | 1 | 0
1 | 0 | 0
1 | 1 | 0




XOR (O Exclusivo): La salida es 1 si el número de entradas en 1 es impar.

Ecuación: ( Y = A \oplus B = \overline{A}B + A\overline{B} )
Tabla de verdad:A | B | Y
--|--|--
0 | 0 | 0
0 | 1 | 1
1 | 0 | 1
1 | 1 | 0




XNOR (NO O Exclusivo): Inverso de XOR. La salida es 1 si el número de entradas en 1 es par.

Ecuación: ( Y = \overline{A \oplus B} = A\overline{B} + \overline{A}B )
Tabla de verdad:A | B | Y
--|--|--
0 | 0 | 1
0 | 1 | 0
1 | 0 | 0
1 | 1 | 1





Tablas de Verdad
Una tabla de verdad lista todas las combinaciones posibles de las entradas de un circuito lógico y la salida correspondiente. Para ( n ) entradas, hay ( 2^n ) filas. Se utilizan para:

Describir el comportamiento de compuertas o circuitos.
Derivar expresiones booleanas.
Verificar equivalencias lógicas.

3.1.1 Lógica TTL
TTL (Transistor-Transistor Logic) es una familia de circuitos integrados digitales que utilizan transistores bipolares. Las compuertas lógicas implementadas en TTL (como NOT, AND, OR, NAND, NOR, XOR) tienen características específicas:

Voltajes: 0 V (lógico 0), 5 V (lógico 1).
Velocidad: Rápida para su época, pero consume más energía que CMOS.
Fan-out: Capacidad de una compuerta para manejar múltiples entradas de otras compuertas (típicamente 10 en TTL estándar).
Ruido: Sensible al ruido, requiere fuentes de alimentación estables.
Ejemplos de CI TTL:
7400: Cuatro compuertas NAND de 2 entradas.
7402: Cuatro compuertas NOR de 2 entradas.
7404: Seis inversores NOT.
7486: Cuatro compuertas XOR de 2 entradas.



En prácticas con protoboard, las compuertas TTL se conectan con resistencias pull-up/pull-down y fuentes de 5 V, asegurando niveles lógicos claros.
3.1.2 Teoremas, Postulados y Expresiones del Álgebra de Boole
El álgebra de Boole es el marco matemático para analizar y simplificar circuitos lógicos. Se basa en variables binarias (0, 1) y operaciones lógicas (AND, OR, NOT).
Postulados

Identidad:
( A + 0 = A )
( A \cdot 1 = A )


Complemento:
( A + \overline{A} = 1 )
( A \cdot \overline{A} = 0 )


Nulo:
( A + 1 = 1 )
( A \cdot 0 = 0 )


Idempotencia:
( A + A = A )
( A \cdot A = A )



Teoremas

Conmutativo:
( A + B = B + A )
( A \cdot B = B \cdot A )


Asociativo:
( (A + B) + C = A + (B + C) )
( (A \cdot B) \cdot C = A \cdot (B \cdot C) )


Distributivo:
( A \cdot (B + C) = A \cdot B + A \cdot C )
( A + (B \cdot C) = (A + B) \cdot (A + C) )


Absorción:
( A + A \cdot B = A )
( A \cdot (A + B) = A )


De Morgan:
( \overline{A + B} = \overline{A} \cdot \overline{B} )
( \overline{A \cdot B} = \overline{A} + \overline{B} )


Involución:
( \overline{\overline{A}} = A )



Expresiones Booleanas

Una expresión booleana combina variables (A, B, C, etc.) con operaciones lógicas (AND, OR, NOT).
Ejemplo: ( Y = A \cdot B + \overline{A} \cdot C ).
Las expresiones se simplifican usando los teoremas para reducir el número de compuertas necesarias en un circuito.

3.1.3 Minitérminos, Maxitérminos y Mapas deක
Minitérminos

Un minitérmino es un producto (AND) de todas las variables de una función, donde cada variable aparece exactamente una vez, en forma directa o complementada.
Representa una fila de la tabla de verdad donde la salida es 1.
Ejemplo: Para 3 variables ( A, B, C ), el minitérmino ( A \cdot \overline{B} \cdot C ) corresponde a la combinación donde ( A=1, B=0, C=1 ).
Una función en suma de productos (SOP) es la suma (OR) de minitérminos.
Ejemplo: ( F = A \cdot \overline{B} \cdot C + \overline{A} \cdot B \cdot C ).



Maxitérminos

Un maxitérmino es una suma (OR) de todas las variables, donde cada variable aparece exactamente una vez, en forma directa o complementada.
Representa una fila de la tabla de verdad donde la salida es 0.
Ejemplo: Para 3 variables, el maxitérmino ( A + B + \overline{C} ) corresponde a una combinación donde la salida es 0.
Una función en producto de sumas (POS) es el producto (AND) de maxitérminos.
Ejemplo: ( F = (A + B + \overline{C}) \cdot (\overline{A} + B + C) ).



Mapas de Karnaugh
El mapa de Karnaugh (K-map) es una herramienta gráfica para simplificar expresiones booleanas.

Estructura:
Para ( n ) variables, el mapa tiene ( 2^n ) celdas.
Cada celda representa un minitérmino.
Las variables se organizan para que celdas adyacentes difieran en una sola variable (código Gray).


Pasos para simplificar:
Llenar el mapa con 1s (para SOP) o 0s (para POS) según la tabla de verdad.
Agrupar 1s (o 0s) en bloques de ( 2^n ) celdas (1, 2, 4, 8, etc.).
Cada grupo genera un término simplificado:
Incluir solo las variables que no cambian dentro del grupo.
Si una variable es 1, aparece sin complementar; si es 0, aparece complementada.


La expresión final es la suma (para SOP) o producto (para POS) de los términos.


Reglas:
Los grupos deben ser lo más grandes posible.
Minimizar el número de grupos.
Los grupos pueden solaparse y envolverse (aristas opuestas son adyacentes).



Ejercicios de Simplificación
Ejercicio 1: Simplificación por Álgebra de Boole y Mapa de Karnaugh
Dada la expresión: ( F = \overline{A} \cdot (B + \overline{C}) + A \cdot \overline{B} \cdot C + \overline{A} \cdot B \cdot \overline{C} )
a) Simplificación por Álgebra de Boole

Reescribir la expresión:[F = \overline{A} \cdot B + \overline{A} \cdot \overline{C} + A \cdot \overline{B} \cdot C + \overline{A} \cdot B \cdot \overline{C}]
Agrupar términos comunes:[F = \overline{A} \cdot B \cdot (1 + \overline{C}) + \overline{A} \cdot \overline{C} + A \cdot \overline{B} \cdot C]
Aplicar ( 1 + \overline{C} = 1 ):[F = \overline{A} \cdot B + \overline{A} \cdot \overline{C} + A \cdot \overline{B} \cdot C]
No se puede simplificar más sin combinar términos incompatibles.

b) Simplificación por Mapa de Karnaugh

Construir la tabla de verdad para ( F ):A | B | C | F
--|--|--|--
0 | 0 | 0 | 0
0 | 0 | 1 | 0
0 | 1 | 0 | 1
0 | 1 | 1 | 1
1 | 0 | 0 | 0
1 | 0 | 1 | 1
1 | 1 | 0 | 0
1 | 1 | 1 | 0


Llenar el K-map (3 variables: ( A ), ( B ), ( C )):    BC
     00 01 11 10
A 0 | 0  0  1  1
  1 | 0  1  0  0


Agrupar los 1s:
Grupo 1: ( (0,1,0) ) y ( (0,1,1) ) → ( \overline{A} \cdot B )
Grupo 2: ( (0,0,1) ) y ( (0,1,1) ) → ( \overline{A} \cdot \overline{C} )
Grupo 3: ( (1,0,1) ) → ( A \cdot \overline{B} \cdot C )


Expresión simplificada:[F = \overline{A} \cdot B + \overline{A} \cdot \overline{C} + A \cdot \overline{B} \cdot C]

Nota: En este caso, el K-map confirma la expresión, pero no reduce más términos.
Ejercicio 2: Simplificación de una Expresión No SOP
Dada la expresión: ( F = (A + \overline{B}) \cdot (\overline{A} + C) + \overline{A} \cdot B \cdot \overline{C} )
a) Simplificación por Álgebra de Boole

Expandir ( (A + \overline{B}) \cdot (\overline{A} + C) ):[(A + \overline{B}) \cdot (\overline{A} + C) = A \cdot \overline{A} + A \cdot C + \overline{B} \cdot \overline{A} + \overline{B} \cdot C]
Simplificar ( A \cdot \overline{A} = 0 ):[= A \cdot C + \overline{B} \cdot \overline{A} + \overline{B} \cdot C]
Sumar el término restante:[F = A \cdot C + \overline{B} \cdot \overline{A} + \overline{B} \cdot C + \overline{A} \cdot B \cdot \overline{C}]
Buscar términos comunes:[F = \overline{A} \cdot (\overline{B} + B \cdot \overline{C}) + A \cdot C + \overline{B} \cdot C]
Simplificar ( \overline{B} + B \cdot \overline{C} = \overline{B} + \overline{C} ):[F = \overline{A} \cdot (\overline{B} + \overline{C}) + A \cdot C + \overline{B} \cdot C]
Combinar términos con ( \overline{B} \cdot C ):[F = \overline{A} \cdot \overline{B} + \overline{A} \cdot \overline{C} + A \cdot C + \overline{B} \cdot C]

b) Simplificación por Mapa de Karnaugh

Construir la tabla de verdad para ( F ):A | B | C | F
--|--|--|--
0 | 0 | 0 | 1
0 | 0 | 1 | 1
0 | 1 | 0 | 1
0 | 1 | 1 | 0
1 | 0 | 0 | 0
1 | 0 | 1 | 1
1 | 1 | 0 | 0
1 | 1 | 1 | 1


Llenar el K-map:    BC
     00 01 11 10
A 0 | 1  1  0  1
  1 | 0  1  1  0


Agrupar los 1s:
Grupo 1: ( (0,0,0) ), ( (0,0,1) ), ( (0,1,0) ) → ( \overline{A} )
Grupo 2: ( (1,0,1) ), ( (1,1,1) ) → ( A \cdot C )


Expresión simplificada:[F = \overline{A} + A \cdot C]

Comparación: El K-map produce una expresión más simple (( \overline{A} + A \cdot C )) que el álgebra de Boole, mostrando la potencia del método gráfico.
Consejos para el Examen

Compuertas y Tablas de Verdad:
Memoriza las tablas de verdad de las compuertas básicas.
Practica derivar tablas de verdad para circuitos combinacionales.


Álgebra de Boole:
Domina los teoremas de De Morgan y distributivos.
Practica expandir y factorizar expresiones.


Mapas de Karnaugh:
Practica construir K-maps rápidamente para 3 y 4 variables.
Asegúrate de agrupar correctamente y verificar bordes envolventes.


Ejercicios:
Resuelve expresiones no SOP/POS convirtiéndolas primero a SOP o usando K-maps.
Verifica tus resultados con la tabla de verdad si el tiempo lo permite.


Prácticas Anteriores:
Revisa tus circuitos en protoboard para recordar conexiones de compuertas TTL.
Relaciona las simplificaciones de las prácticas con los métodos teóricos.



