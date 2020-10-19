3 La PEC consiste en una grabación de 5 minutos como máximo (2 como mínimo)
sobre un tema/herramienta específica del bloque de apartados del tema 1, 
exponiendo sus ventajas y desventajas. 
Se valorara la capacidad de síntesis y la claridad de exposición.

# Datos de la PEC

* *Herramienta:* Graphite

## Que es Graphite?

Graphite es una herramienta para **almacenar y visualizar cualquier tipo de dato numérico**.
Graphite **no es una herramienta de monitorización**.
Esa parte y la de avisos o alertas, es delegada a los usuarios de Graphite.
Estos mismos usuarios deben configurar las aplicaciones que usan en su stack para enviar los registros a Graphite. (Es una herramienta de colección de datos *pasiva* o *push*)

## Ventajas

* **completamente desacoplada de las herramientas de monitorización y de aviso** (Alert), que por lo tanto, delega esa responsabilidad a los usuarios.
    * Sistema flexible de ingesta y visualización de datos
    * Tiene la capacidad de analizar todos los datos puntuales numéricos que el usuario quiera insertar en el sistema de forma continua mediante el uso de gráficos.
* **Añadir monitorización** de una aplicación existente a Graphite es **trivial**.
    * Simplemente se tiene que editar la linea que se quiere registrar para que contenga el **identificador, el valor y la fecha de ese registro**.
    * Al ser popular, muchos programas de monitorización ya incluyen la opción de generar los logs en formato Graphite.
* El **sistema de inclusión y organización de registros es jerárquico** y simple de entender. (entorno.maquina.servicio.log)

## Desventajas
 
* **Escalado**
    * En instancias con maquinas aleatorias, como en la nube, puede darse el caso de que al reiniciar una maquina, se pause el registro de esa maquina, para iniciar el registro de la nueva maquina, pero el servicio que monitoriza sigue siendo el mismo.
* Si **no** se ha recibido un **registro**, No queda claro si el problema es de Graphite o del propio servicio
* **Centraliza el proceso de registro** del sistema entero, de forma que si la maquina proporciona el servicio de Graphite desaparece de la red, no hay registros ni datos centralizados.
* **Sistema de visualización y monitorización básico**, pero se puede usar grafana para remediar eso.
