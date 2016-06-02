# Guia de estilo
Guía de estilo para mi código en C++

Con etiquetas de Doxygen para incluirlo directamente en la documentación del proyecto. Para que en el caso de
que colabore otra persona pueda seguirla.

Con el tiempo se va modificando y ajustando, por eso me gusta incluir la fecha de la ultima modificación

    /**
    \page codingStyle Guia de estilo
    \author Jonathan López
    \date 1 de Abril de 2016
    
    Este es un resumen del estilo de codificación que se ha intentado seguir al
    escribir el código.
    
    \section general Indicaciones generales
    
     - Nunca se utilizan rutas absolutas dentro del código.
     - Se intenta compilar con el nivel máximo de alertas disponible en el
     compilador y eliminar todos los avisos que aparezcan.
    
    \section comentarios Comentarios
    
     - En la cabecera del fichero hay que incluir los siguientes datos en un bloque
     de comentarios:
    	- Nombre y correo electrónico del autor.
    	- Fecha de creación. Mes y año.
    	- Versión.
    	- Licencia que se aplica.
     - Usará un generador de documentación automático (por ejemplo "Doxygen") para
     documentar el programa.
     - Se documentará los ficheros, funciones, clases y bloques de código para
     ofrecer información útil sobre su funcionalidad o uso. Siendo lo más breve y
     escueto posible.
     - Cuando se comenta el código se trata de explicar qué hace o cual es su
     propósito. No cómo lo hace. El código debería ser autoexplicativo.
     - Sobre todo se tratará de documentar las clases, métodos y funciones públicas.
     - Se minimizará lo máximo posible los comentarios que no se vayan a incluir en
     la documentación final del programa.
    
    \section sangrado Sangrado (Identación)
    
     - Se usan tabulaciones.
     - El tamaño de las tabulaciones es de 4 espacios.
    
    \section variables Declaración de variables
    
     - Se declara cada variable en una línea separada.
     - Si se usan nombres de una sola letra, será \b sólo para los contadores y
     donde su próposito es evidente.
     - El nombre de las variables y funciones empiezan con una letra minúscula. Las
     siguientes palabras que componen el nombre de la variable empiezan por
     mayúsculas. Notación "lowerCamelCase".
     - Se evitan las abreviaturas si los nombres de las variables no son muy largos.
     - Nombres de variables auto-explicativos.
     - Los nombres de las variables estarán formados por sustantivos, pudiendo
     calificarse con adjetivos.
     - Se evitará el uso de prefijos.
    
    Ejemplos:
    \verbatim
    	// incorrecto
    	QString k; // Cadena temporal para procesar los datos de entrada
    	int valor1, valor2, valor3;
    	QByteArray Muestrasnuevas;
    	QString inter;  // Interface que vamos a utilizar
    
    	// correcto
    	QString cadenaTemporal;
    	int valor1;
    	int valor2;
    	int valor3;
    	QByteArray muestrasNuevas;
    	QString interface;
    \endverbatim
    
    \section espaciado Espacios en blanco y saltos de línea
    
     - Limite el largo de las líneas a 80 carácteres. Insertar saltos de línea si
     son necesarios.
     - Tras cada punto y coma (';') siempre hay un salto de línea. Una instrucción
     por línea.
     - Se usa una línea en blanco para agrupar declaraciones.
     - Se usa una línea en blanco antes y otra después de cada estructura
     condicional o bucle.
     - No hay espacios en blanco entre un carácter y un paréntesis '(' y ')'.
     - Cuando se cierra el paréntesis, tras este sí se deja un espacio.
     - Se deja un espacio en blanco antes y después de los símbolos, punteros y
     referencias ('<', '>', '<=', '>=', '&&', '||', '<<', '*', '&'). Pero no entre
     '*' o '&' y el nombre de la variable.
     - Se deja un espacio en blanco después de las comas.
     - Siempre hay un salto de línea \b antes y \b después de las llaves ('{' y
     '}').
    
    Ejemplo \b incorrecto:
    \verbatim
    	QString cadenaTexto;
    	char* caracter;
    	const char* const temperatura = "celsius";
    	if(!cadenaTexto.isEmpty()){
    		int valor1 = 10;
    		int valor2 = 23;
    		while(valor1<=valor2){
    			....
    		}
    		// más código
    	} cadenaTexto.clear();
    
    \endverbatim
    
    Ejemplo \b correcto:
    \verbatim
    	QString cadenaTexto;
    	char *caracter;
    	const char * const temperatura = "celsius";
    
    	if(!cadenaTexto.isEmpty())
    	{
    		int valor1 = 10;
    		int valor2 = 23;
    
    		while(valor1 <= valor2)
    		{
    			....
    		}
    
    		// más código
    	}
    
    	cadenaTexto.clear();
    \endverbatim
    
    \section llaves Llaves
    
     - Usar llaves en todas las declaraciones condicionales y bucles. Sin excepciones.
    
    \section parentesis Paréntesis
    
     - Usar paréntesis para agrupar expresiones.
     - Usar paréntesis siempre que ayuden a aclarar u organizar una expresión
     compleja.
    
    \section switch Declaraciones Switch
    
     - El 'case' debe estar identado respecto a la columna del 'switch'.
     - Cada declaración 'case' debe tener un 'break' (o 'return') al final o un
     comentario de por qué intencionadamente no lo hay.
    
    Ejemplo:
    \verbatim
    	switch (myVariable)
    	{
    		case valor1:
    			hacerAlgo();
    			break;
    		case valor2:
    			hacerAlgo2();
    			break;
    		case valor3:
    			hacerOtraCosa();
    			// se necesita ejecutar además el 'default'
    		default:
    			funcionDefault();
    			break;
    	}
    \endverbatim
    
    
    */
  
