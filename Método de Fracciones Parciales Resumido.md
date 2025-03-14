# Fracciones Parciales: Método Resumido
Angel David Melo, Valentina Riveros, Daniel Ladino
## 1. Introducción
El método de fracciones parciales es un metodo matemático utilizado para descomponer una función normalmente dificil de operar a una suma de fracciones más simples. Este método es especialmente útil en el análisis de sistemas dinámicos y en la solución de ecuaciones diferenciales, ya que permite simplificar la transformada inversa de Laplace, facilitandonos así la obtención de soluciones en el dominio del tiempo.

## 2. Casos Principales

### 2.1. **Raíces reales diferentes**
$$Si \( B(s) \)$$ tiene raíces reales y distintas, la descomposición en fracciones parciales se tiene que hacer de la siguiente forma:

   $$\[ F(s) = \frac{a_1}{s + p_1} + \frac{b_2}{s + p_2} + \cdots + \frac{b_n}{s + p_n} \]$$

**Hallamos los valores de $$\(b_1 \) y \(b_2 \)$$**:

   - Para encontrar $$\(b_1 \)$$, multiplicas ambos lados de la ecuación por $$\( (s + p_1) \)$$ y luego sustituimos $$\( s = -p_1 \)$$. Esto hace que todos los términos excepto $$\(b_1 \)$$ se cancelen:
     $$b_1 = \left[ (s + p_1) \cdot F(s) \right]_{s = -p_1}$$

   - Hacemos lo mismo para $$\(b_2 \)$$: multiplicas por $$\( (s + p_2) \)$$ y $$\( s = -p_2 \)$$: $$b_2 = \left[ (s + p_2) \cdot F(s) \right]_{s = -p_2}$$
     

   - Después de hacer estos pasos, obtenemos los valores de $$\( b_1 \)$$ y $$\( b_2 \)$$, y obtenemos la suma de fracciones más simples:
   $$F(s) = \frac{b_1}{s + p_1} + \frac{b_2}{s + p_2}.$$

### 2.2. **Raíces reales repetidas**: 

Si $$\( B(s) \)$$ tiene raíces reales repetidas, la descomposición incluirá términos con potencias crecientes en el denominador:

   $$\[ F(s) = \frac{b_1}{s + p} + \frac{b_2}{(s + p)^2} + \cdots + \frac{b_k}{(s + p)^k} \]$$
   
**Hallamos los valores de $$\( b_1 \), \( b_2 \), y \( b_3 \)$$**:

   - **Para \( b_3 \)**:
     Multiplicas ambos lados de la ecuación por $$\( (s + p)^3 \)$$ y luego reemplazamos $$\( s = -p \)$$. Esto elimina todos los términos excepto $$\( b_3 \)$$:
     $$b_3 = \left[ (s + p)^3 \cdot F(s) \right]_{s = -p}$$

   - **Para $$\( b_2 \)$$**:
     Derivas la ecuación con respecto a $$\( s \)$$ y luego reemplazamos $$\( s = -p \)$$. con esto hallamos $$\( b_2 \)$$:
     $$b_2 = \left[ \frac{d}{ds} \left( (s + p)^3 \cdot F(s) \right) \right]_{s = -p}$$

   - **Para $$\( b_1 \)$$**:
     Derivas nuevamente ambos lados de la ecuación con respecto a $$\( s \)$$ y luego reemplazamos $$\( s = -p \)$$.con esto hallamos $$\( b_1 \)$$:
     $$b_1 = \left[ \frac{1}{2} \cdot \frac{d^2}{ds^2} \left( (s + p)^3 \cdot F(s) \right) \right]_{s = -p}$$
   - Después de calcular $$\( b_1 \), \( b_2 \), y \( b_3 \)$$, lo reemplazamos en la fracciób original como la suma de fracciones más simples:
   $$F(s) = \frac{b_1}{s + p} + \frac{b_2}{(s + p)^2} + \frac{b_3}{(s + p)^3}$$
   
### 2.3. **Raíces complejas conjugadas**

Si $$\( B(s) \)$$ tiene raíces complejas, la descomposición incluirá términos con funciones seno y coseno :

   $$\[ F(s) = \frac{As + B}{(s + \alpha)^2 + \omega^2} \]$$

## 3. Ejemplos de Aplicación

### 3.1. Caso 1: Raíces Reales Diferentes

**Ejemplo 1:**

Función:

$$\[ F(s) = \frac{s + 3}{(s + 1)(s + 2)} \]$$

Descomposición en fracciones parciales:

$$\[ F(s) = \frac{a_1}{s + 1} + \frac{a_2}{s + 2} \]$$

Para encontrar $$\( a_1 \) y \( a_2 \)$$, multiplicamos ambos lados por $$\( (s + 1)(s + 2) \)$$ y evaluamos en $$\( s = -1 \) y \( s = -2 \)$$:

$$\[ a_1 = \left[ (s + 1) \frac{s + 3}{(s + 1)(s + 2)} \right]_{s = -1} = 2 \]$$

$$\[ a_2 = \left[ (s + 2) \frac{s + 3}{(s + 1)(s + 2)} \right]_{s = -2} = -1 \]$$

Por lo tanto, la descomposición es:

$$\[ F(s) = \frac{2}{s + 1} - \frac{1}{s + 2} \]$$

### 3.2. Caso 2: Raíces Reales Repetidas

**Ejemplo 2:**

Función:

$$\[ F(s) = \frac{s^2 + 2s + 3}{(s + 1)^3} \]$$

La descomposición en fracciones parciales:

$$\[ F(s) = \frac{b_1}{s + 1} + \frac{b_2}{(s + 1)^2} + \frac{b_3}{(s + 1)^3} \]$$

Para encontrar $$\( b_1 \), \( b_2 \), y \( b_3 \)$$, multiplicamos ambos lados por $$\( (s + 1)^3 \)$$ y derivamos:

$$\[ b_3 = \left[ (s + 1)^3 \frac{s^2 + 2s + 3}{(s + 1)^3} \right]_{s = -1} = 2 \]$$

$$\[ b_2 = \left[ \frac{d}{ds} \left( (s + 1)^3 \frac{s^2 + 2s + 3}{(s + 1)^3} \right) \right]_{s = -1} = 0 \]$$

$$\[ b_1 = \left[ \frac{1}{2} \frac{d^2}{ds^2} \left( (s + 1)^3 \frac{s^2 + 2s + 3}{(s + 1)^3} \right) \right]_{s = -1} = 1 \]$$

La descomposición es:

$$\[ F(s) = \frac{1}{s + 1} + \frac{0}{(s + 1)^2} + \frac{2}{(s + 1)^3} \]$$

### 3.3. Caso 3: Raíces Complejas Conjugadas

**Ejemplo 3:**

Dada la función:

$$\[ F(s) = \frac{2s + 12}{s^2 + 2s + 5} \]$$

Completamos el cuadrado en el denominador:

$$\[ s^2 + 2s + 5 = (s + 1)^2 + 2^2 \]$$

La descomposición en fracciones parciales será:

$$\[ F(s) = \frac{10 + 2(s + 1)}{(s + 1)^2 + 2^2} = 5 \frac{2}{(s + 1)^2 + 2^2} + 2 \frac{s + 1}{(s + 1)^2 + 2^2} \]$$

## 3. Ejercicios

### 3.1 Función:

$$F(s) = \frac{s^2 + 4s + 5}{(s + 2)^3},$$

descomponer \( F(s) \) en fracciones parciales 

---

### Solución

- **Descomposición en fracciones parciales**:
   $$F(s) = \frac{b_1}{s + 2} + \frac{b_2}{(s + 2)^2} + \frac{b_3}{(s + 2)^3}$$

- **$$\( b_3 \)$$**:

   Multiplicamos ambos lados por  $$\( (s + 2)^3 \) $$ y evaluamos en  $$\( s = -2 \)$$:

   $$b_3 = \left[ (s + 2)^3 \cdot \frac{s^2 + 4s + 5}{(s + 2)^3} \right]_{s = -2}$$
   
   $$b_3 = \left[ s^2 + 4s + 5 \right]_{s = -2} = (-2)^2 + 4(-2) + 5 = 4 - 8 + 5 = 1$$

- **$$\( b_2 \)$$**:

   Derivamos respecto a  $$\( s \) $$ y evaluamos en  $$\( s = -2 \)$$:

   $$\frac{d}{ds} \left[ (s + 2)^3 \cdot \frac{s^2 + 4s + 5}{(s + 2)^3} \right] = b_2 + 2b_1(s + 2)$$

   Evaluando  $$\( s = -2 \) $$:

   $$\left[ \frac{d}{ds} (s^2 + 4s + 5) \right]_{s = -2} = b_2$$

   $$\frac{d}{ds} (s^2 + 4s + 5) = 2s + 4.$$

   Evaluando  $$\( s = -2 \) $$:

   $$2(-2) + 4 = -4 + 4 = 0$$
   $$\( b_2 = 0 \) $$.

- **$$\( b_1 \) $$**:

   Derivamos respecto a  $$\( s \) $$ y evaluamos $$\( s = -2 \) $$:

   $$\frac{d^2}{ds^2} \left[ (s + 2)^3 \cdot \frac{s^2 + 4s + 5}{(s + 2)^3} \right] = 2b_1$$

   Evaluando $$\( s = -2 \) $$:

   $$\left[ \frac{d^2}{ds^2} (s^2 + 4s + 5) \right]_{s = -2} = 2b_1$$

   Calculamos la segunda derivada:

   $$\frac{d^2}{ds^2} (s^2 + 4s + 5) = 2$$


   $$2 = 2b_1 \implies b_1 = 1$$

- **Descomposición final**:

   Sustituimos los valores de  $$\( b_1 \), \( b_2 \), y \( b_3 \) $$:

   $$F(s) = \frac{1}{s + 2} + \frac{0}{(s + 2)^2} + \frac{1}{(s + 2)^3}$$

### 3.2 Función:

$$F(s) = \frac{2s + 5}{(s + 1)(s + 3)},$$

### Solución 

- **Descomposición en fracciones parciales**:

   $$F(s) = \frac{a_1}{s + 1} + \frac{a_2}{s + 3}$$

- **$$\( a_1 \)$$**:

   Multiplicamos ambos lados por $$\( (s + 1) \)$$ y evaluamos en $$\( s = -1 \)$$:

   $$a_1 = \left[ (s + 1) \cdot \frac{2s + 5}{(s + 1)(s + 3)} \right]_{s = -1}$$
   
   $$a_1 = \left[ \frac{2s + 5}{s + 3} \right]_{s = -1} = \frac{2(-1) + 5}{(-1) + 3} = \frac{-2 + 5}{2} = \frac{3}{2}$$

- **$$\( a_2 \)$$**:

   Multiplicamos ambos lados por $$\( (s + 3) \)$$ y evaluamos $$\( s = -3 \)$$:

   $$a_2 = \left[ (s + 3) \cdot \frac{2s + 5}{(s + 1)(s + 3)} \right]_{s = -3}$$


   $$a_2 = \left[ \frac{2s + 5}{s + 1} \right]_{s = -3} = \frac{2(-3) + 5}{(-3) + 1} = \frac{-6 + 5}{-2} = \frac{-1}{-2} = \frac{1}{2}$$

5. **Descomposición final**:

   Sustituyendo los valores de $$\( a_1 \)$$ y $$\( a_2 \)$$:

   $$F(s) = \frac{3/2}{s + 1} + \frac{1/2}{s + 3}$$

