# Fracciones Parciales: Método Resumido

## 1. Introducción
El método de fracciones parciales es un metodo matemático utilizado para descomponer una función normalmente dificil de operar a una suma de fracciones más simples. Este método es especialmente útil en el análisis de sistemas dinámicos y en la solución de ecuaciones diferenciales, ya que permite simplificar la transformada inversa de Laplace, facilitandonos así la obtención de soluciones en el dominio del tiempo.

## 2. Definición

Las fracciones parciales se aplican a un tipo de funcione normalmente de la forma:

$$\[ F(s) = \frac{A(s)}{B(s)} \]$$

donde $$\( A(s) \) y \( B(s) \)$$ son polinomios en el dominio de la frecuencia $$\( s \)$$, y el grado de $$\( A(s) \)$$ es menor que el grado de $$\( B(s) \)$$. El objetivo es expresar $$\( F(s) \)$$ como una suma de fracciones más simples.

### 2.1. Casos Principales

1. **Raíces reales diferentes**: $$Si \( B(s) \)$$ tiene raíces reales y distintas, la descomposición en fracciones parciales se tiene que hacer de la siguiente forma:

   $$\[ F(s) = \frac{a_1}{s + p_1} + \frac{a_2}{s + p_2} + \cdots + \frac{a_n}{s + p_n} \]$$

2. **Raíces reales repetidas**: Si $$\( B(s) \)$$ tiene raíces reales repetidas, la descomposición incluirá términos con potencias crecientes en el denominador:

   $$\[ F(s) = \frac{b_1}{s + p} + \frac{b_2}{(s + p)^2} + \cdots + \frac{b_k}{(s + p)^k} \]$$

3. **Raíces complejas conjugadas**: Si \( B(s) \) tiene raíces complejas, la descomposición incluirá términos con funciones seno y coseno amortiguadas:

   \[ F(s) = \frac{As + B}{(s + \alpha)^2 + \omega^2} \]

## 3. Ejemplos de Aplicación

### 3.1. Caso 1: Raíces Reales Diferentes

**Ejemplo 1:**

Dada la función:

\[ F(s) = \frac{s + 3}{(s + 1)(s + 2)} \]

La descomposición en fracciones parciales será:

\[ F(s) = \frac{a_1}{s + 1} + \frac{a_2}{s + 2} \]

Para encontrar \( a_1 \) y \( a_2 \), multiplicamos ambos lados por \( (s + 1)(s + 2) \) y evaluamos en \( s = -1 \) y \( s = -2 \):

\[ a_1 = \left[ (s + 1) \frac{s + 3}{(s + 1)(s + 2)} \right]_{s = -1} = 2 \]

\[ a_2 = \left[ (s + 2) \frac{s + 3}{(s + 1)(s + 2)} \right]_{s = -2} = -1 \]

Por lo tanto, la descomposición es:

\[ F(s) = \frac{2}{s + 1} - \frac{1}{s + 2} \]

### 3.2. Caso 2: Raíces Reales Repetidas

**Ejemplo 2:**

Dada la función:

\[ F(s) = \frac{s^2 + 2s + 3}{(s + 1)^3} \]

La descomposición en fracciones parciales será:

\[ F(s) = \frac{b_1}{s + 1} + \frac{b_2}{(s + 1)^2} + \frac{b_3}{(s + 1)^3} \]

Para encontrar \( b_1 \), \( b_2 \), y \( b_3 \), multiplicamos ambos lados por \( (s + 1)^3 \) y derivamos:

\[ b_3 = \left[ (s + 1)^3 \frac{s^2 + 2s + 3}{(s + 1)^3} \right]_{s = -1} = 2 \]

\[ b_2 = \left[ \frac{d}{ds} \left( (s + 1)^3 \frac{s^2 + 2s + 3}{(s + 1)^3} \right) \right]_{s = -1} = 0 \]

\[ b_1 = \left[ \frac{1}{2} \frac{d^2}{ds^2} \left( (s + 1)^3 \frac{s^2 + 2s + 3}{(s + 1)^3} \right) \right]_{s = -1} = 1 \]

Por lo tanto, la descomposición es:

\[ F(s) = \frac{1}{s + 1} + \frac{0}{(s + 1)^2} + \frac{2}{(s + 1)^3} \]

### 3.3. Caso 3: Raíces Complejas Conjugadas

**Ejemplo 3:**

Dada la función:

\[ F(s) = \frac{2s + 12}{s^2 + 2s + 5} \]

Completamos el cuadrado en el denominador:

\[ s^2 + 2s + 5 = (s + 1)^2 + 2^2 \]

La descomposición en fracciones parciales será:

\[ F(s) = \frac{10 + 2(s + 1)}{(s + 1)^2 + 2^2} = 5 \frac{2}{(s + 1)^2 + 2^2} + 2 \frac{s + 1}{(s + 1)^2 + 2^2} \]

Por lo tanto, la transformada inversa de Laplace será:

\[ f(t) = 5e^{-t} \sin(2t) + 2e^{-t} \cos(2t) \]

## 4. Aplicación en Matlab

Matlab puede calcular las fracciones parciales de manera automática utilizando la función `residue`. Por ejemplo, para la función:

\[ F(s) = \frac{s^2 - s - 3}{s(s - 1)(s + 3)} \]

El código en Matlab sería:

```matlab
num = [1 -1 -3];
den = conv([1 -1 0], [1 3]);
[r, p, k] = residue(num, den);
