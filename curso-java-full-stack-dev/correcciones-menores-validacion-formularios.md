# 14) Correcciones Menores, Themeforest, Menu Multinivel, Angular Update CLICore, Validación de Formularios

01:36 - Cargando data para servicios paginados (70 registros)

03:00 - SERVICIOS PAGINADOS

- agregando nuevo método listarPageable a interfaz de service, impl, logica a controller

- en ResourceServerConfig se modifica a permiteAll() la ruta a modificar /pacientes temporalmente

08:00 - Ruta ejemplo: localhost:8080/pacientes/pageable?page=6&size=10 viendo nueva respuesta de servicio.

09:30 - modificando frontend angular

12:30 - capturando eventos paginator de angular para llamar a servicio de backend (restablece mas la configuracion en ResourceServerConfig)

- cambios en front: paciente service, paciente component

- * Cuando se trabaja con pageable, ya no es necesario el matpaginator.

25:00 - THEMEFOREST(plantillas) para diferentes tecnologías, reacts, angular, etc.

- buscar angular 8 (material si es que quieren)

32:22    - Luego de comprar una plantilla les llegará un rar con un rar dentro de nombre (seed) plantilla con componentes mínimos y una completa.

- Sobre el proyecto seed (semilla) debería iniciarse un proyecto y tomar de referencia el proyecto completo para agregar componentes.

- iniciar como cualquier proyecto angular ng s --o, pero antes un npm install para restablecer node_modules.

38:00 - ACTUALIZANDO VERSION DE ANGULAR (de 5 (1.6)- 8 )

50:20 - Resumen de actualización de versión de angular

51:55 - MULTI LEVEL MENU componente adicional a Angular material (ng-material-multilevel-menu)

59:20 - VALIDACION DE CAMPOS EN FRONT (campo requerido, longitud máxima, etc)

1:06:00 Digital Ocean (introducción)

### Links de Interés

https://github.com/ShankyTiwari/ng-material-multilevel-menu

https://themeforest.net

https://update.angular.io
