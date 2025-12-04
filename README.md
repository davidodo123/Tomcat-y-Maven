 - Importamos la maquina de Nginx 2 para hacer Nginx 3.

## Configuracion Nginx
- En la practica Nginx creamos un archivo nuevo llamado conf, donde creare un bloc de notas donde pondre la ruta y un dominio de pruebas.
![Crear Archivo](img/crear%20www.test.png)
- Luego creo el dominio de pruebas. Para acceder a él necesitamos entrar como administrador a C:\Windows\System32\drivers\etc\hosts y añadimos esas dos ultimas lineas, la ruta y el dominio.
![Dominio de pruebas](img/editarhost.PNG)

## Generar un certificado SSL
- Nos descargamos la imagen que genera certificados.
![Descargar generador certificados](img/DescargarStakate.png)
- Creamos certs en nuestra carpeta.
![Certs](img/certs.png)
- Generamos los certificados dentro de certs.
![Generar Certificados](img/dockerrun.png)

## Configuracion
- Ahora que tengo el certificado, le voy a decir a Nginx que use el certificado que he descargado.
- Nos volvemos al .conf que habia creado, y lo configuro añadiendole las rutas creadas dentro del contenedor.
![Editar .test.conf](img/Editarbloc.png)
- Levantamos el Docker para ver si funciona.
![Levantar Docker](img/levantardocker.png)
- Lo ejecutamos en local para asegurarnos http://juanma-davids.test:8080
![Ver si funciona](img/correcto.png)

## Mapeo de puertos y montaje de volumen de certificados
- Cambiamos los puertos
![Cambio de puertos](img/Mapeo.png)

## Docker Compose
- En vez de iniciar con Docker Run, lo hariamos con Docker Compose. Creamos Docker Compose en bloc de notas y añadimos los puertos y los volumenes.
![crear docker compose](img/creardockercompose.png)
- Levantamos con docker compose
![Compose Up](img/composeup.png)
- Compruebo con HTTP
![HTTP](img/HTTP.png)
- Y compruebo con HTTPS, nos saldra que es privada, asi que e daremos a Avanzado, y luego entraremos, significa que funciona correctamente.
![Privada](img/privada.png)
![HTTPS](img/HTTPS.png)