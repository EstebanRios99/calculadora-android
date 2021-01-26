# Calculadora Nativa - Android Studio

Creadores del Proyecto: 
- Esteban Ríos 
- Marvin Zambrano

El proyecto trata de una calculadora con Android Studio, con 7 funcionalidades:
- Suma
- Resta
- Multuplicación
- División
- Potencia
- Raíz Cuadrada
- Funciones Triginometricas (Seno y Coseno) 

# Explicación de las Funciones Implementadas

Dentro del programa las funciones necesarias son las que permiten realizar las operaciones.

Suma, Resta, Multiplicación:
- Es una funcion privada de tipo double/float que recibe como parámetros dos elementos del mismo tipo (en este ejemplo 2 doubles)
- Retorna la operación entre los parametrós que ingresan.
División:
- Es una funcion privada de tipo double/float que recibe como parámetros dos elementos del mismo tipo (en este ejemplo 2 doubles)
- Se hace la validación del que no sea el denominador = 0;
- Retorna la operación entre los parametrós que ingresan.
Potencia y Raiz:
- Es una funcion privada de tipo double/float que recibe como parámetros un elemento del mismo tipo en este caso recibe la base.
- Se llama a la función Math que permite realizar las operaciones matemeticas que son mas complejas. para la Potencia es pow(base,exponente) y para la Raíz es sqrt(base).
- Retornamos el valor obtenido
Función trigonométrica Seno y Coseno:
- Es una funcion privada de tipo double/float que recibe un parametro que es ángulo a evaluar.
- Se llama a la funcon Math que permite resliar las dos aplicaciones trigonométricas como seno y coseno, la unica observación es que el valor lo devuelve en radianes.
- Obs: Se puede transformar de radianes a grados con la fórmula radianes*180/PI
- Retornamos el valor en radianes.


Con las funciones principales, se configuran los metodos que van a usar los botones.

Dentro del metodo general OnCreate que instancia los metodos de la pantalla, se procede a realizar cada una de las tareas que realizan los botones, a continuación se detalla cada uno:

- Primero vamos a tomar el valor que almacena tanto el campo de ingreso, el campo de visualizacion y botones, usando el metodo findById, el cual buscara el Id del elemento en pantalla y captura el valor que posee y se guarda en un tipo de dato definido al inicio del programa.
- Para los botones se crea un método o proceso que OnClickListener que se activará al momento que sea llamado mediante el botón al que se asignó.
- Para los botones de Suma, Resta, Multiplicación, División al momento de llamar al respectivo botón se guardan los parámetros, dentro del metodo OnClick:
  - Se guarda el valor que se ingresa en el campo de texto.
  - Se almacena en una variable un String que indentifica la operación que se realiza.
  - Se limpia el texto.
- Para los botones de Potencia, Raíz, Seno, Coseno al momento de llamar al respectivo botón se guardan los parámetros, dentro del metodo OnClick:
  - Se Llama el metodo de potencia.
  - Se obtiene el valor de la caja de texto y se lo envía como parámetro al método llamado.
  - Se realiza un setText al TextView para visualizar el resultado.
- Para el botón Igual dentro del método OnClick, se realiza las siguintes operaciones:
  - Se realiza una condición donde se compara el valor de la operación que se guardo al inicio con la operación respectiva.
  - Se Llama el metodo respectivo, segun el tipo de operación.
  - Se obtiene el valor de la caja de texto y se lo envía como parámetro al método llamado, junto con el otro parámetro que está almacenado al dar clic en el botón que realiza la operación.
  - Se realiza un setText al TextView para visualizar el resultado.



