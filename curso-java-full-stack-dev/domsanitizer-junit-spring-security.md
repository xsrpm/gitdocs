# 11) DomSanitizer Angular, JUnit, Spring Security + JWT + OAUTH2

## **00:00 Manejando imagenes (DOM Sanitizer)**

Backend/ front end (Archivos-Files)

Subir archivos a la base de datos, bajar de la base de datos.

Leer y pintar archivos de la base de datos.

Lo explicado acá es un caso muy particular, lo más general y recomendado es guardar el enlace al archivo en la base de datos.

Guardar el archivo en un ftp.

base64-image.de

https://codebeautify.org/base64-to-image-converter

## **47:00 - Spring Security Introducción**

A partir de la versión Spring boot 2 se obliga que especifique la versión de Spring security jwt y oauth2 a usar.

Spring security: seguridad en spring a nivel el proyecto.

Spring jwt: forma de codificar información mediante un token (entre 2 partes)

https://jwt.io

Spring OAUTH2

Forma de identificación con oauth y token jwt

https://docs.apigee.com/api-platform/images/management-api/oauth-first-request.png

## **56:15 - Modificando Backend**

## **1:00:00 - Usando Junit para insertar usuarios**

Filtros en orden:

CORS

Spring Security Filter Change

OAUTH2

inyección de dependencias es válidos en atributos, interfaces y métodos

1:20:00 Clase SecurityConfig (configuración principal de seguridad)

1:25:30 Clase AuthException (manejar rutas no existentes)

1:26:20 Clase ResourceServerConfig (que rutas voy a proteger)

Clase propia de OAUTH2 (autenticación usuarios y autorización de recursos)

1:28:20 AutorizationServerConfigurerAdapter (configuracion y creacion de token)

1:32:44 UsuarioServiceImpl (clase de Spring que especifica donde se guardan los usuarios y roles)

1:38:00 Usando scripts para poblar roles en la bd

1:40:00 Pruebas con postman con autorización

1:45:00 concluyendo y preguntas

Autenticación / Autorización con Spring Security, OUATH, JWT

Clases que añaden este comportamiento

com.xsrsys

AuthException : Notificar que no se tiene acceso al recurso por falta de Autenticación/AUtorización

AuthorizationServerConfig

SecurityConfig

ResourceServerConfig: Señalar rutas a proteger por autenticación

com.xsrsys.model

Rol: Roles para autorización

USuario : Usuarios para autenticación

com.xsrsys.repo

IUsuarioRepo

### Links de interés

base64-image.de

https://codebeautify.org/base64-to-image-converter

https://jwt.io

https://docs.apigee.com/api-platform/images/management-api/oauth-first-request.png

https://github.com/auth0/angular2-jwt

https://stackoverflow.com/questions/48506618/spring-security-oauth2-is-it-possible-to-change-table-and-column-names

[Token Postman](https://drive.google.com/file/d/1Tatevg0sjiveSg90emJn_Jr2K_Zx93hz/view?usp=sharing)
