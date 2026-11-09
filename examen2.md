#Gonzalo García Chavez
#20120985
 
##1
###A)
Cree que la API en sí separa al cliente del servidor, lo cual está bien. Después cree que Docker convierte a su servidor en microservicios, o al menos que separa los servidores entre sí, lo cual está muy mal. En sí podría usar Docker para crear diferentes servidores más fácilmente pero no es lo que hace los microservicios en sí, solo pone todo el código en un contenedor para poder deployarlo más fácilmente.
###B)
En algún punto se le tendría que llamar a otra parte, a un contenedor externo u otro servidor a través de alguna conexión.
###C)
La del pizarrón no habla de tecnologías (pero la respuesta del compañero sí las menciona), habla de los límites de alcance de las diferentes partes del programa (el usuario llega hasta el frontend, el API lo conecta con el backend, y los microservicios lo conectan con otras partes o servicios).
 
##2
###A)
Las rutas sí sirven para organizar el código y separar las partes, pero no evita que todo esté pegado en el mismo programa. Las réplicas sirven para aguantar más carga o por si se cae una instancia que las demás sigan funcionando, pero en sí cada réplica tiene todo el código completo, así que no separan mucho (al menos le da redundancia).
###B)
Nunca dejó de ser monolito porque sigue siendo todo el código junto, solo que ahora es como que fueran 3 monolitos.
###C)
Ocuparían mínimo 3 imágenes diferentes en el compose (una para usuarios, otra para pedidos y otra para recomendar). Tienen que ser 3 porque cada pedazo debe tener solo su propio código y su propio trabajo, y no se caiga todo junto.
 
##3
###A)
No es un Gateway porque hace DEMASIADO. Si un gateway es un recepcionista que solo te dice a donde ir dependiendo de a donde tienes acceso (hey mi llave es del 603 y aqui está mi id - ah ok, ve al piso 6 a la derecha), este es un todologo que tarda en enviar el correo y las demás cosas, así que dejaría su puesto solo.
###B)
1. Se traga todo el procesador en tareas más pasadas, si se está entrenando también va a empezar a alucinar pronto porque se le están poniendo a hacer muchas cosas (o tal vez no alucinar en sí pero va a mezclar sus tareas).
2. El mismo problema con los monolitos de que algo cae y todo cae.
3.  Si vas a hacer un cambio mínimo tienes que cargar el modelo pesado otra vez.
###C)
Que el recepcionista solo se dedique a eso, que otro servicio se encargue del SQLite, y un Worker para los correos
