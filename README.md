# 26.01.2026.PE06-Parte_II-Arrays-Y-Cadenas-Interfaz_Lista-Javitos


INTERFAZ LISTA Implementa la interfaz Lista mediante arrays
En programación, una lista enlazada o lista es una estructura de datos dinámica. Consiste en una
secuencia de nodos, en los que se guardan datos de cualquier tipo (en nuestro ejercicio,
consideraremos valores numéricos) y una referencia (llamada puntero) al nodo siguiente. El principal
beneficio de las listas enlazadas respecto a los arrays convencionales es que el orden de los elementos
enlazados puede ser diferente al orden de almacenamiento en la memoria o el disco, permitiendo que
el orden de recorrido de la lista sea diferente al de almacenamiento.
Vamos a simular una lista mediante arrays. Para ello, definir la interfaz Lista con las siguientes
operaciones:
Lista
<<interface>>
+ getTamanyo() : int
+ insertarAlFinal(int valor): void
+ insertarAlPrincipio(int valor) : void
+ insertarEnLaPosicion(int posicion, int valor) : void
+ eliminarLaPrimera() : void
+ eliminarLaUltima(): void
+ eliminar(int posición): void
+ buscar(int n) : int //Devuelve la posición
+ unirDosListas(Lista lista2) : void
+ imprimirLista() : String

A continuación, implementa la clase ListaNimerica, que implementa la interfaz Lista.

ListaNumerica
+ lista: int[]
+ TAM_MAX : int = 100 (final)
+ tamanyo : int //Guarda el tamaño de la lista en cada momento
+ ListaNumerica()
+ getTamanyo() : int
+ insertarAlFinal(int valor): void
+ insertarAlPrincipio(int valor) : void
+ insertarEnLaPosicion(int posición, int valor) : void
+ eliminarLaPrimera() : void
+ eliminarLaUltima(): void
+ eliminar(int posición): void
+ buscar(int n) : int //Devuelve la posición
+ unirDosListas(Lista lista2) : void
+ imprimirLista() : String //Equivale al toString
+ toString() : String






Complejo Rural “Los Javitos” (Proyecto de clase)
El Complejo rural Los Javitos es conjunto de alojamientos turísticos ubicados en una finca
situada en la Sierra de Huelva, y que combinan la arquitectura tradicional con comodidades
modernas, ofreciendo una experiencia auténtica y tranquila en contacto con la naturaleza, y
que incluye servicios de valor añadido como restauración y/o actividades al aire libre
(senderismo, tirolina, descenso, tiro con arco, paseos a caballo…). 

Los datos que se almacena de cada alojamiento son:
• Nombre.
• Capacidad (nº de personas).
• Tarifa por noche.
• Si tiene o no chimenea.
• Si tiene o no jacuzzi.
• Si está o no actualmente alquilado.
• Número de veces alquilado.

Los datos que se almacena de cada cliente son:
• Nombre y apellidos.
• DNI.
• Email.
• Lugar de residencia.
• Número de veces alojado.

Se pide:
• Implementar el programa con arrays. Para simplificar la prueba de la aplicación, se
supone una cantidad máxima de 100 de clientes y 15 alojamientos.

Las clases a implementar serán:
o Clase Alojamiento:
▪ Atributos (todos privados):
• Nombre (String).
• Capacidad (nº de personas). Entero.
• Tarifa por noche. Decimal.
• Si tiene o no chimenea. Booleano.
• Si tiene o no jacuzzi. Booleano.
• Si está o no actualmente alquilado. Booleano.
• Número de veces alquilado. Entero.
▪ Métodos: constructor, get, set, toString.

• Implementa un método compareTo que reciba como parámetro otro
alojamiento y devuelva -1 si el alojamiento es menor que el pasado como
parámetro, +1 si es mayor que el pasado como parámetro y 0 si son iguales.

El criterio de comparación es el nombre del alojamiento.
o Clase Cliente:
▪ Atributos (todos privados):
• Nombre. String.
• DNI. String. Debe cumplir la expresión regular asociada a cualquier DNI
(8 dígitos y 1 carácter).
• Email. String. Debe cumplir la expresión regular asociada a cualquier
email.
• Lugar de residencia. String.
• Número de veces alojado. Entero.
▪ Métodos: constructor, get, set, toString. IMPORTANTE:
• En el constructor de Cliente y en los sets correspondientes, se debe
comprobar que el dni y el email cumplen con el patrón correspondiente
(expresiones regulares).

• Implementa un método compareTo que reciba como parámetro otro cliente
y devuelva -1 si el cliente es menor que el pasado como parámetro, +1 si es
mayor que el pasado como parámetro y 0 si son iguales. El criterio de
comparación es el nombre del cliente.

o Clase Javitos:
▪ Atributos:
• alojamientos: array de 15 objetos de la clase Cliente
• clientes: array de 100 objetos de la clase Cliente.
• numAlojamientos: entero (int) que informa del número de alojamientos
existentes actualmente en el array, inicialmente a 0, y un máximo de 15.
• numClientes: entero (int) que informa del número de clientes existentes
actualmente en el array, inicialmente a 0, y un máximo de 100.
▪ Métodos: constructor, toString y los métodos:
• altaCliente ➔ dar de alta un nuevo cliente (añadir al array). Se le pasa
como parámetro el nuevo cliente.
• bajaCliente ➔ dar de baja un cliente (dado su dni), es decir, eliminar del
array. Se pasa como parámetro el dni.
• altaAlojamiento ➔ dar de alta un nuevo alojamiento (añadir al array). Se le
pasa como parámetro el nuevo alojamiento.
• bajaAlojamiento ➔ dar de baja un alojamiento (dado su nombre), es decir,
eliminar del array. Se pasa como parámetro el nombre del alojamiento a
borrar.
• listadoAlojamientos ➔ imprime un listado ordenado por orden alfabético
de alojamientos (copia el array de alojamientos en otro array, lo ordenas
alfabéticamente por el nombre del alojamiento y lo imprimes ).
• listadoClientes ➔ imprime un listado ordenado por orden alfabético de los
clientes (copia el array de clientes en otro array, lo ordenas alfabéticamente
por el nombre del cliente y lo imprimes ).
• topClientes ➔ imprime un listado de clientes ordenado por el atributo “nº
de veces alojado”, de mayor a menor (copia el array de clientes en otro
array, lo ordenas por “nº de veces alojado” y lo imprimes).
• topAlojamientos ➔ imprime un listado de alojamientos ordenado por el
atributo “nº de veces alquilado”, de mayor a menor (copia el array de
clientes en otro array, lo ordenas por “nº de veces alquilado” de mayor a
menor, y lo imprimes).

o Clase Principal, que contiene el método main en la que se probarán todas las clases y
métodos anteriores.
