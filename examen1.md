#Gonzalo García Chavez
#20120985
 
##A1
 
El entorno virtual es útil pero principalmente para iterar y programar cómodamente. Docker es mejor si van a llevarlo a producción para que cada vez que se instale e inice tenga la misma configuración exacta. También, darle a runserver un montón de veces solo va a causar problemas de concurrencia y no es realmente escalable, pero puede servir si es para hacer pruebas o un proyecto muy pequeño.
 
##A2
 
- A. El .venv es solo el entorno virtual, no guarda el código en sí, sino más bien las instalaciones específicas de Python que se usan para el proyecto. El código sigue intacto pero en general es buena idea no perder la carpeta aun así.
- B. Se tiene que crear otro entorno virtual, para este punto espero que el requirements.txt esté actualizado y bien escrito, porque así puedes solo iniciar otro entorno y aplicar el pip install -r requirements.txt y ya lo tienes configurado. Esto solo SI está completo y actualizado, si no, suerte con la búsqueda de versiones específicas y todas las dependencias.
- C. Es que eso solo pone las variables de entorno en esa terminal, para poder trabajar directamente de ahí, pero no las instala en el entorno global.
 
##A3
 
- A. /app está dentro del entorno de Linux del contenedor, no en tus archivos normales, PERO el COPY . . copia todos los archivos de nuestro proyecto al entorno de Linux, así que puedes así modificar los archivos de allá adentro (por así decirlo) y saber que hay allá.
- B. Excluir el .venv sirve para que los archivos compilados no pasen al entorno de Linux, por si estas trabajando en Windows y por eso no fueran compatibles, o MacOS, o en general es buena practica para evitar problemas. Lo de la base de datos específicamente es para que no sobreescriba la base de datos en producción, que sería horrible si hubieras borrado algo o agregado algo para hacer pruebas.
 
##B1
 
- A. Si la aplicación móvil no usa JavaScript porque prefiere usar algo nativo, es probable que difiera con el otro backend de alguna manera, y eso se tendría que arreglar. También, incluso si no difiere, ahora cada cambio que haces en un backend tienes que hacerlo en el otro también, casi duplicando el trabajo.
-B. El Backend solo entrega los datos procesados y el frontend los muestra en sí. Aunque también, obviamente si hay cambios drásticos en la manera en la que el backend da los datos, se tendría que cambiar mucho el frontend también, pero en general debería de ser más cómodo.
