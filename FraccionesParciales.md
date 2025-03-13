# Descompocision en fracciones parciales
Daniel Felipe Ladino, Angel David Melo, Valentina Riveros
## Que es?
Las fracciones parciales son un método de integración que se utiliza para descomponer una fracción algebraica compleja en una suma de fracciones más simples.
Este proceso permite:
- Permite resolver integrales de funciones racionales que no se pueden resolver por otros métodos 
- Facilita la resolución de ecuaciones diferenciales lineales
Este procedimiento tiene la funcion de descomponer una fraccion racional y transformarla en una suma de fracciones mas simples, esto basandose en distintos casos que pueden llegar a presentarse al momento de utilizar este metodo.
Las situaciones que nos podemos encontrar son:


## Factores lineales distintos:


$$\frac{P(x)}{(x-a)(x-b)}=\frac{A}{x-a}+\frac{B}{x-b}$$

## Factores lineales repetidos:

$$\frac{P(x)}{(x-a)^{n}}=\frac{A_{1}}{x-a}+\frac{A_{2}}{(x-a)^{2}}+\cdot \cdot \cdot +\frac{A_{n}}{(x-a)^{n}}$$

## Factores cuadraticos irreducibles:

$$\frac{P(x)}{(x^{2}+bx+c)}=\frac{Ax+B}{(x^{2}+bx+c)}$$

# Ejercios
1. resolver el siguiente ejercicio:

$$ \frac{3x^{2}+5x-17}{(x+3)(x-2)^{2}}$$

## solucion
$$\frac{3x^{2}+5x-17}{(x+3)(x-2)^{2}}=\frac{A}{(x+3)}+\frac{B}{(x-2)}+\frac{C}{(x-2)^{2}}$$

$$3x^{2}+5x-17=A(x-2)^{2}+B(x-2)(x+3)+C(x+3)$$

$$si x=-3$$

$$27+15-17=A(-5^{2})$$

$$25=25A$$

$$A=1$$

$$si x=2$$

$$12-10-17=c(5)$$

$$-15=5C$$

$$C=-3$$

$$3x^{2}-5x-17=1(x-2)^{2}+B(x+3)(x-2)+(-3)(x+3)$$

$$3x^{2}-5x-17=(x^{2}-4x+9)+B(x^{2}+x-6)-3x-9$$

$$3x^{2}-5x-17=(x^{2}-4x+9)+Bx^{2}+xB-6B-3x-9$$

$$3=1+B$$

$$B=2$$

$$\frac{3x^{2}+5x-17}{(x+3)(x-2)^{2}}=\frac{1}{(x+3)}+\frac{2}{(x-2)}-\frac{3}{(x-2)^{2}}$$

$$\frac{1}{(x+3)}+\frac{2}{(x-2)}-\frac{3}{(x-2)^{2}}\to e^{-3t}+2e^{2t}-3te^{2t}$$

2. hallar la ecuacion para la siguiente ecuacion:

$$G(s)=\frac{x^{2}-3}{x^{3}-x^{2}-4x-1}$$

## solucion

$$G(s)=\frac{x^{2}-3}{x^{3}-x^{2}-4x-1}=\frac{x^{2}-3}{(x-1)(x^{2}+1)}=\frac{A}{x-1}+\frac{Bx+C}{x^{2}+1}$$

$$x^{2}-3=A(x^{2}+1)+Bx+C(x-1)$$

$$si X=1$$

$$-2=A(2)$$

$$A=-1$$

$$si x=0$$

$$-3=A-C$$

$$C=1+3$$

$$C=4$$

$$si x=-1$$

$$-2=-2+2B-4$$

$$2B=-2+2+4$$

$$4=2B$$

$$B=2$$

$$\frac{x^{2}-3}{(x-1)(x^{2}+1)}=-\frac{1}{x-1}+\frac{2x+2}{x^{2}+1}$$

$$-\frac{1}{x-1}+\frac{2x+2}{x^{2}+1}\to -e^{t}+2cos(t)+2sin(t)$$
