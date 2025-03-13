# Transformada de Laplace
Daniel Felipe Ladino, Angel David Melo, Valentina Riveros
## Sistema
Se trata de la combinacion de diferentes componentes que actuan en conjunto para lograr un objetivo especifico.
## Sistema dinamico
Es un sistema que tiene la peculiaridad de evolucionar con el tiempo donde su salida en un instante de tiempo depende entradas en otros instantes de tiempo. ademas, su comportamiento o estado depende de una magnitud variable que va cambiando con el tiempo. Estos sistemas se pueden analizar por medio de modelos matematicos.
## Planta
Se trata del sistema fisico el cual se pretende controlar, puede ser cualquier proceso siempre y cuando el sistema responda a entradas externas. Esta puede representarse mediante ecuaciones diferenciales, funciones de transferencia o modelos de espacio de estado, esto para desarrollar controladores que puedan ajustar la respuesta del sistema segun lo requerido.
## Proceso
Es conocido como un sistema capaz de transformar entradas en salidas a lo largo del tiempo que tambien puede verse afectado por factores externos que pueden alterar la salida.
## Modelo dinamico
Se conoce como la descripcion de como se comporta un sistema a lo largo del tiempo
# Recordatorio de calculo diferencial
El calculo diferencial es una rama del calculo que estudia como cambian las funciones segun sus variables independientes, siendo sus concepto principal es la derivada.
### Derivada
Se expresa como:

$$\displaystyle \lim_{h \to 0} \frac{f(x+h)-F(x)}{h}$$


Tambien sigue las siguientes reglas:


$$\frac{\mathrm{d} }{\mathrm{d} x}x^{n}=nx^{n-1}$$


$$(F(x)\cdot g(x))'=F(x)'\cdot g(x)+F(x)\cdot g(x)'$$


$$(\frac{F(x)}{g(x)})'=\frac{F(x)'g(x)-F(x)g(x)'}{g(x)^{2}}$$


## Sistemas lineales y no lineales
Un sistema se considera lineal cunado cumple con el pricipio de superpocision y homogeneidad. Suelen representarse por medio de funciones de tranferencia.
mientras que los sistemas no lineales no cumplen con estos principios y pueden incluir funcionamiento caotico o saturaciones.
## Transformada de Laplace
Se trata de una herramienta que convierte ecuaciones diferenciales en ecuaciones algebraicas en el dominio de la frecuencia (s) esto para facilitar su analisis y solucion de distintos sistemas.
Algunas de sus principales propiedades son:
## Linealidad:
$$L (af(t)+bg(t))=aF(s)+bG(s)$$
## Trasnformada de la derivada:
$$L (f'(t))=sF(s)-F(0)$$
$$L (f''(t))=s^{2}F(s)-sF(0)-F'(0)$$
## Transformada de la integral:
$$L (\int_{0}^{t}f(\tau )d\tau )=\frac{F(s)}{s}$$
## Teorema del valor final
$$\displaystyle \lim_{t \to \infty }f(t)=\displaystyle \lim_{s \to 0}sF(s)$$

# ejercicios

1. Encontrar la transformada de laplace Para la siguiente ecuacion:

$$y'-3y'+2y=e^{t}, y(o)=1, y'(0)=0$$

## solucion

$$L[y'(t)]=sY(s)-y(0)$$

$$L[y''(t)]=s^{2}Y(s)-sy(0)-y'(0)$$

$$L[y''-3y'+2y]=L[e^{t}]$$

$$L[y'']=s^{2}Y(s)-sy(0)-y'(0)=s^{2}Y(s)-s(1)-0=s^{2}Y(s)-s$$

$$L[y']=sY(s)-y(0)=sY(s)-1$$

$$L[y]=Y(s)$$

$$L[e^{t}]=\frac{1}{s-1}$$

$$\frac{1}{s-1}=(s^{2}Y(s)-s)-3(sY(s)-1)+2Y(s)$$

$$\frac{1}{s-1}+s-3=s^{2}Y(s)-s-3sY(s)+3+2Y(s)$$

$$\frac{1}{s-1}+s-3=(s^{2}-3s+2)Y(s)$$

$$\frac{1}{s-1}+s-3=(s-1)(s-2)Y(s)$$

$$Y(s)=\frac{s-3}{(s-1)(s-2)}+\frac{1}{(s-1)^{2}(s-2)}$$

$$\frac{s-3}{(s-1)(s-2)}=\frac{A}{s-1}+\frac{B}{s-2}$$

$$s-3=A(s-2)+B(s-1)$$

$$si s=1$$

$$2=A(-1)$$

$$A=-2$$

$$si s=2$$

$$-1=B$$

$$\frac{s-3}{(s-1)(s-2)}=\frac{2}{s-1}-\frac{1}{s-2}$$

$$L^{-1}[Y(s)]=2e^{t}-e^{2t}$$

2. Hallar la transformada de la ecuacion:

