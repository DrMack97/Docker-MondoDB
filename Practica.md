# Preguntes teòriques

1) Quina és la diferència entre docker run i docker compose up?

# docker run: 

crea y ejecuta un único contenedor especificando todas las configuraciones en la línea de comandos.

# docker compose up:

lee un archivo docker-compose.yml para desplegar, conectar y ejecutar múltiples contenedores que forman una aplicación completa con un solo comando.

# ambito

Usa docker run: Cuando necesites probar una imagen rápidamente, ejecutar un comando puntual (como un contenedor efímero para correr una migración) o gestionar servicios totalmente independientes.

Usa docker compose up: Cuando tu proyecto requiera unir varias piezas (por ejemplo: tu servidor web, una base de datos y un sistema de caché) y quieras automatizar todo el proceso de inicio con una sola instrucción.

2) Per a què serveix la instrucció depends_on? 
Garanteix que el servei dependent estigui completament operatiu?

# depends_on 

sirve para definir el orden de arranque (arranca MongoDB antes que Mongo Express).

No garantiza que MongoDB esté completamente operativo (solo que el contenedor está iniciado).

3) Explica cuál es la diferencia entre una red bridge por defecto y una red personalizada (con nombre) en Docker Compose.

# Bridge por defecto:

Contenedores se comunican por IP, no por nombre.

Menos aislada.

# Red personalizada (ej. red-tienda):

Contenedores se comunican por nombre de servicio.

Mayor aislamiento y control.