# Auditoria de sistemas y redes

## Indice

* Introducción
* Controles básicos
* Auditado la red física
* Auditando la red lógica

## Introducción

La información transita de un pagar a otro de la red.

Por eso, se deben establecer protocolos y métodos de contención para asegurar que la información transmitida desde el origen sea idéntica que la recibida en el destino.

Existen diversas formas en la que la información puede variar:

* Por causas propias de la tecnología
    * Alteración de bits (Se destaca con un código de redundancia cíclico (CRC))
    * Ausencia de tramas o paquetes (Se arregla con numeración y reenvió)
    * Alteración de secuencias (La capa de transporte lo soluciona)
* Por causas intencionadas
    * Indagación (Consulta de un mensaje por terceros)
    * Suplantación (Un tercero simula ser su emisor/receptor)
    * Modificación (Un tercero modifica en contenido del mensaje)

Para evitar o complicar ataques, es deseable que los sistemas de comunicación no "recuerden" las rutas de comunicación anteriores.

De existir y detectar un fallo en las comunicaciones, la capa de aplicación es la responsable de decidir como recuperarse. 
Existen dos vertientes, *Continuacion* (FTP) y *Reinicio* (Transacción electrónica).

### Conceptos **TCP/IP**

* **Intranet:** Red interna y segura de una compañía
* **Extranet:** Red externa, privada y segura que comparten varias empresas (Red de hacienda)
* **Internet:** Red interna, publica y no segura
* **DMZ:** Red local entre la red interna de una organización y una red externa

## Controles básicos

Para auditar una red, se deben tener en cuenta varios factores:

* Accesos no autorizados (Vulnerabilidades)
* Puertas traseras
* Transacción de contraseñas y su cifrado
* Vulnerabilidades de confianza de nodos (Spoofing)
* Control de SW maligno y actualizaciones de SW

Se debe auditar la responsabilidad de la organización en garantizar:

* *Gestion de la red:* Inventario de equipos y normativa de seguridad
* *Monitorizacion de comunicaciones:*
* *Revision de costes:*
* *Decisiones sobre necesidades actuales y futuras de comunicaciones:*

## Auditando la red física

* Importante revisar las instalaciones físicas del edificio ademas de los sistemas usados para acceder a la red interna desde fuera (VPN, Correo electrónico interno)
* En caso de un desastre (Vulneración del sistema por parte maligna), que redes/sistemas se podrían usar (Plan de contingencia)

Los objetivos a los que una organización debería llegar son:

* Áreas seguras para los equipos de comunicaciones, previniendo accesos no autorizados
* Protección y tendido adecuado de cables y lineas de comunicación
* Mantenimiento y gestión de equipos de red
* Controles de utilización de los equipos de monitorización y pruebas de red
* Revisión del plan de desastres
* Controles específicos, en caso de que se utilicen salidas directas al exterior (Firewall)

## Auditando la red lógica

Segmentación de red, para evitar el uso inapropiado de la red (DDoS, DoS) y evitar que secciones de la red puedan comunicarse cuando no deberían.

Los objetivos a los que una organización debería llegar son:

* Política de uso de servicios de red documentada
* Autenticación de usuarios obligatoria
* Autenticación de equipos
* Control de puertos abiertos y acceso remoto
* Segmentación de la red con puntos de control (Firewall)
* Control de privilegios de usuario de conexión a la red (IAM)
* Control de flujos de información, encaminamiento y redundancia (Control de errores y reenvío)
* Registro de la actividad de red, para ayudar a reconstruir incidencias
