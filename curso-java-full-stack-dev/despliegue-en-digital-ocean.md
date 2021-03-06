# 15) Despliegue en DigitalOcean (Independientes y Front en WAR)

### Guía Digital Ocean

[Despliegue en Digital Ocean](DigitalOcean.pdf)

PREPARANDO LOS REQUERIMIENTOS

Primero creas un proyecto, es como una carpeta donde dentro tendrás vps para los distintos servidores que necesites.

Segundo creas droplets (servidores)

- en una nueva distro: sudo apt-get update para refrescar los paquetes que esten en linux.
- instalar una versión de tomcat (zip) (copiando y pegando en una carpeta, en este caso /opt

19:00

- instalar jdk antes oracle-jdk, ahora openjdk-8-jdk

20:00 - Iniciando tomcat.

23:00 - instalar nginx - para rutear el puerto 80 al 8080.

25:00 - editando la tabla de ruteo.

28:30 - instalando postgre, creando base de datos necesaria, creando tablas necesarias.

# DESPLIEGUES (2 formas)

## 1 - Frontend y backend que funcionan por separado y que se comunican.

32:00 - Preparar el proyecto backend para que corra como war.

38:00 - transfiriendo war a carpeta webapps de tomcat para despliegue

43:00 - Insertando data de prueba en tablas generadas por JPA.

45:00 - Desplegando front

46:00 - actualizar enviroment.prod.ts (en app.module, se tiene valores fijos q se pueden escribir en enviroments)

47:50 - ng build --prod (referencia a enviroment.prod, minifica y ofusca el código).

generado se encuentra en carpeta dist (dentro del proyecto).

55:00 - configuracion para encontrar archivos SPA

56:00 - desplegando en servidor: mover la carpeta dentro de dist, dentro de la carpeta webapp del servidor.  Copiar el front end a la misma altura del backend en el server.

58:00 - Indicar al servidor que la aplicación no es de servlet tradicional sino un SPA con Angular.

59:00 - Configurando proyecto de angular, agregando estrategia de generación y recompilar el proyecto para producción

- - 1:04:00

## 2 - Frontend dentro del war.

1:06:00 - Colocando el generado del frontend dentro de la carpeta src del proyecto backend

1:08:00 - configurando maven para indicar al backend la ubicación del frontend, mvn clean, mvn install

1:10:00 - transfiriendo el war generado al server.

1:13:00 - Discutiendo ventajas de ambos enfoques.

- Existen casos de servidores que no permiten tener archivos sueltos de vistas (html, css, js), solo desplegar un war.

En ese caso es conveniente usar el segundo método para tener empaquetado todo el proyecto en un war.

- En la mayoría de casos es mejor mantener el front y el back por separado en el despliegue, asi es mas facil mantener y rápido el cambio de un antiguo frontend por otro, sin dar de baja el backend.

Para este caso se despliega el backend en un servidor de aplicaciones java y el front en un tomcat o en un simple servidor apache.

1:17:00 - Adicional: pom.xml  para despliegue en Webfly (jboss) con java 11

1:19:00 - Agregando nombre de dominio (Godaddy - Digital Ocean)

# Notas

## Al desplegar:

- la primera vez que se crea la bd se tiene que insertar en la bd los inserts de las tablas de seguridad y la data necesaria (migrations)

## Cada vez que se levanta (enciende) el droplet:

dentro de tomcat/bin

sh startup.sh

dirigirse a la url pública y ver que está levantado tomcat.

revisar catalina.out por errores.
