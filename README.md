# PRACTICA Python, Flask y Gunicorn #

## Instalamos Python ##
- Dentro de la máquina virtual, instalamos el gestor de paquetes de Python y la herramienta de entornos virtuales:
- Actualizar repositorios e instalar pip:
![InstalarPython](img/InstalarPython.png)
- Instalar pipenv:
![InstalarPipe](img/InstalarPipe.png)
- Comprobamos que este instalado:
![comprobarpipe](img/comprobarpipe.png)
- Instalamos dotenv:
![Usuario](img/doten.png)

- Configurar el PATH para reconocer Pipenv:
![Local](img/nano.png)


- Creamos la estructura de directorios y gestionamos los permisos para el servidor web:
![usuarios](img/app.png)
- Y le damos permisos para el root, sin esto no funcionaria bien:
![Comprobar](img/permisos.png)


## Configuracion de Python y Flask ##
- Iniciamos el entorno 
![ErrorNano](img/shell.png)
- Dentro del entorno descargamos flask
![ErrorNano](img/flask.png)
- Creamos los archivos .py
![ErrorNano](img/creamospy.png)
- Abrimso application.py, wsgi.py y los editamos
![ErrorNano](img/apli.png)
![ErrorNano](img/ws.png)

## Instamalos Maven ##
Maven permite compilar, empaquetar y desplegar aplicaciones de forma automática sin usar la interfaz web.
- Se descarga el gestor de dependencias en la máquina Debian.
![maven](img/instalarmaven.png)
- Se edita settings.xml de Maven para incluir las credenciales del usuario con rol manager-script.
![Servers](img/servers.png)
- Creación de una aplicación web de prueba mediante el uso de arquetipos de Maven.
![Aplicacion](img/aplicacion.png)
- Se integra el plugin tomcat7-maven-plugin para habilitar la comunicación entre Maven y el servidor Tomcat.
![plugin](img/plugin.png)
- Se ejecutan comandos de despliegue (deploy), actualización de la aplicación (redeploy) y retirada de la misma (undeploy).
![despliegue](img/despliegue.png)
- Volvemos a desplegarla
![Redeploy](img/redeploy.png)
- Retiramos la aplicaicon
![undeploy](img/undeploy.png)

## Tarea ##
Como ejercicio final se realiza el ciclo completo: obtención de código fuente, cambio de versión y despliegue automático.
- Se descarga el código fuente del juego "Rock-Paper-Scissors" desde GitHub y se selecciona la rama patch-1.
![Clonar](img/clonar.png)
- Adaptación del pom.xml del juego para incluir las credenciales de nuestro servidor local.
![Pluginnuevo](img/pluginnuevo.png)
- Acceso final a la aplicación funcionando correctamente en la dirección http://192.168.56.10:8080/juego.
![Juego](img/juego.png)