# Factorial de un Numero

Hoy vamos a ver cómo se calcula el factorial de un número. Calcular factoriales es muy sencillo, vamos a ver en qué consiste:

### ¿Qué es la función factorial?

La función factorial se representa con un signo de exclamación “!” detrás de un número. Esta exclamación quiere decir que hay que multiplicar todos los números enteros positivos que hay entre ese número y el 1.

Por ejemplo:

![image](https://github.com/user-attachments/assets/b1f64314-1287-499c-a130-df7ad13650ee)

A este número, 6! le llamamos generalmente “6 factorial”, aunque también es correcto decir “factorial de 6”.

En tu calculadora podrás ver una tecla con “n!” o “x!”. Esta tecla te servirá para calcular directamente el factorial del número que quieras.

### Algunos ejemplos de factoriales

Vamos a ver algunos ejemplos más de factoriales:

![image](https://github.com/user-attachments/assets/8bdda357-2ab0-4560-9375-67d0925857cc)

Como ves, 100! es enorme…

Y, ¿qué hacemos con los números más pequeños? 1 factorial es, lógicamente, 1, ya que multiplicamos 1 x 1:

![factoriales-3-222x85](https://github.com/user-attachments/assets/039469e5-6e8b-47ba-8e45-ee3836bd7b34)

Pero, ¿cómo podemos calcular el 0 factorial? Bueno, esto no tiene sentido cuando aplicamos la norma de que hay que multiplicar todos los números enteros positivos entre el 0 y el 1, ya que 0 x 1 es 0.

Al final, por convenio se ha acordado que lo más útil es que el 0 factorial sea igual a 1. Así que recuerda:

![image](https://github.com/user-attachments/assets/62c63d48-331a-4e0e-9a0a-5bb3b52137fb)

## En Kotlin seria de esta forma:

~~~
fun factorial(n: Int): Long
{
    if (n <= 1)
  {
    return 1
  }
  return n * factorial(n - 1)
}
fun main()
{
  val number = 5
  println("El factorial de $number es ${factorial(number)}")
}
~~~

Este codigo en Kotlin calcula el factorial de un numero utilizando recursividad.

### Funcion factorial

~~~
fun factorial(n: Int): Long {
~~~

* Esta linea define una funcion llamada _factorial_ que toma un parametro n de tipo _Int_ y devuelve un valor de tipo _Long_. Se utiliza _Long_ para permitir el manejo de numeros grandes que pueden resultar del calculo del factorial.

### Condicion Base

~~~
 if (n <= 1) {
    return 1
  }
~~~

* Aqui se verifica si _n_ es menor o igual a 1. Si lo es, la funcion devuelve 1. Esto se debe a que el factorial de 0 y 1 es 1, y esta es la condicion base que detiene la recursion.

### Llamada recursiva

~~~
return n * factorial(n - 1)
~~~

* Si _n_ es mayor que 1, la funcion calcula el factorial de _n_ multiplicando _n_ por el resultado de llamar a si misma con _n - 1_. Esta llamda recursiva continuara hasta que _n_ llegue a 1 o 0, momento en el que se cativara la condicion base.

### Funcion main

~~~
fun main() {
  val number = 5
  println("El factorial de $number es ${factorial(number)}")
}
~~~

* La funcion _main_ es el punto de entrada del programa. Aqui se declara una variable _number_ con el valor de 5.
* Luego, se imprime el resultado del factorial de _number_ utilizando la funcion _factorial_ La expresion _${factorial(number)}_ llama la funcion _factorial_ y muestra el resultado en la salida. 
