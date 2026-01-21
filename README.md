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
- Comprobamos si Gunicorn arranca.
![ErrorNano](img/gunicorn.png)
![ErrorNano](img/desplegada.png)

## Crear el servicio en Systemd ##
Para que la aplicación no se detenga al cerrar la terminal, hay que crear un servicio del sistema.
- Creamos el archivo y ajustamos el contenido:
![ErrorNano](img/ruta.png)
- Y iniciamos el servidor:
![ErrorNano](img/iniciar.png)


## Configurar Nginx como Proxy Inverso ##
Ahora configuramos Nginx para que reciba las peticiones por el puerto 80 y las pase al archivo app.sock que creó Gunicorn.
- Instalamos Nginx
![ErrorNano](img/Nginx.png)
- Luego creamos el archivo sites-available, y lo configuramos para que responda a app.izv y www.app.izv:
![ErrorNano](img/log.png)
- Para finalizar reiniciamos Nginx:
![ErrorNano](img/reiniciar.png)


## Configurar el archivo HOSTS en Windows ##
- Desplegamos la web con la ruta http://app.izv/:
![ErrorNano](img/desplegado.png)