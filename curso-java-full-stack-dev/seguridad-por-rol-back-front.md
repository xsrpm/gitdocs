# 12) Seguridad por Roles en back-end, Seguridad en Front-end (Gestión de Tokens JWT, Menus por Roles, Guard)

01:00 - Seguridad por roles en backend

Luego de una correcta autenticación se puede limitar el acceso a las rutas con determinados roles con la siguiente anotación sobre el Mapping del controller seleccionado para agregar una barrera de autorización

02:00 - De forma estática.

- De forma dinámica usando una clase intermedia.

@PreAuthorize("hasAuthority('ADMIN') or hasAuthority('DBA')")

ó mas personalizado

@PreAuthorize("@authServiceImpl.tieneAcceso('listar')")

AuthServiceImpl.tieneacceso sería una clase y método que consulta la autenticación y autorización bajo cierta configuración

Se obtendrá la respuesta access_denied en caso se intente acceder con un rol incorrecto.

15:43 - Guardando tokens en base de datos

Clase SecurityConfig, metodo tokenStore()

Creacion de tablas necesarias en base de datos.

20:00 - Creando Componente Frontend para logging

- página de inicio el login

30:00 - creando service login para lógica de inicio de sesión

41:00 - Almacenando token en frontend

45:00 - autenticando componentes con tokens usando: (@auth0/angular-jwt) (instalar npm install este paquete)

52:00 - redireccionando de login a alguna ruta.

54:00 - diferenciando rutas según rol (decodificando token)

57:00 - creando tabla menu-rol, opciones de menú para dar acceso a opciones del front (backend)

1:04:00 - entidades de menu en front, servicio menu

1:10:00 - decodificando token para pintar opciones de menú dinámicamente, producto del login usando (@auth0/angular-jwt) (autenticación)

1:18:00 - filtrando autorización (paths de url) Guards

- si está logueado

1:26:00 - si token está expirado

1:28:00 - si tienes el rol necesario

1:35:00 - creando ruta not 403

1:38:30 - validando mostrar menu

1:40:00 - cerrar sesión

1:41:00 - activando base de datos para tokens
