Fundamentos de Seguridad y Auditoria

Reto de Investigacion 1
 Investiga cómo el sistema clasifica los eventos cruzando dos variables: "Facilidad" (Facility, es decir, qué parte del sistema genera el log, como auth, cron o daemon) y "Prioridad" (Severity, desde debug hasta emerg).

Syslog es un protocolo que gestiona los registros del cliente en el servidor que clasifica eventos de dos maneras: 

-Facility: Es el origen del mensaje. Su propósito es permitir que el demonio de registro sepa qué tipo de programa está enviando el dato para decidir dónde guardarlo.

Ejemplos comunes de "facilities":
auth / authpriv: Registros relacionados con la seguridad y los intentos de inicio de sesión (autenticación).
cron: Mensajes generados por el programador de tareas automáticas del sistema.
kern: Mensajes procedentes directamente del núcleo (kernel) del sistema.
mail: Eventos relacionados con el servidor de correo electrónico.
user: Mensajes genéricos de aplicaciones que corren en el espacio de usuario.


¿Por qué es una negligencia grave que el archivo /var/log/auth.log tenga permisos de lectura para usuarios no privilegiados?

Que ese archivo sea legible por usuarios no privilegiados es una negligencia porque expone informacion critica que facilita la fuga de datos importantes y permite al atacante localizar tu red, identificar tus cuentas de usuario y encontarr debilidades en permisos de administrador 


¿Qué información específica (como PIDs, nombres de usuario o direcciones IP) diferencia un intento fallido de conexión remota SSH de un simple fallo de contraseña de un usuario local frente a la pantalla?


Se diferencian por la presencia del demonio en el proceso ssh que gracias a nuestra IP el demonio actua en segundo plano y crea un canal cifrado seguro.


Reto de Investigación 2. ¿Qué ventajas vitales ofrece enviar y custodiar los logs en un servidor externo seguro en lugar de mantenerlos dispersos e indefensos en la propia máquina que podría ser vulnerada?

Ofrece ventajas vitales como garantizar la integridad ante ataques y asegura un cumplimiento legal frente a detectar amenazas superando la fragilidad de tener registros dispersos e inalterables en máquinas locales 



Referencias para la consulta

[1] Modelo de madurez para la gestión de logs en centros de datos
automatización y buenas prácticas. Disponible en: https://dialnet.unirioja.es/servlet/articulo?codigo=10398407

[2] SSH: qué es y cómo funciona este protocolo. Disponible en https://www.arsys.es/blog/ssh



