# 10) JPA Procedure, Chart.js, PDF-Viewer, Descargar arreglo de bytes

```jsx
npm install @angular/flex-layout --save
```

para manejar css cards

para manejar operaciones con fechas en  javascript fácilmente. (aunque actualmente está desaconsejado)

```jsx
npm install moment --save
```

0:00 detalle de la consulta.

16:00 - 50:35 chart.js (gráficos estadísticos)

```jsx
npm i chart.js --save
```

se crea un procedimiento almacenado

un componente para mostrar el chat.

se crea el backend necesario que llame al procedimiento almacenado  que entregará la data necesario para el chart.

50:36 - 1:10:00 Jasper Studio (Reportería) Crear reporte y agregarlo al backend

jasper studio (crear reportes como un ide.)

ireport antes

1:10:00 - 1:19:00 Descargar PDF de reporte.

1:19:00 - 1:28:00 Mostrar Reporte en pantalla de angular

### Procedure

```jsx
CREATE OR REPLACE FUNCTION fn_listarResumen () 
 RETURNS TABLE (
 cantidad INT,
 fecha TEXT
) 
AS $$
DECLARE 
    var_r record;
BEGIN
FOR var_r IN(
    select (count(*)::int) as cantidad, to_char(c.fecha, 'dd/MM/yyyy') as fecha from consulta c 
    group by to_char(c.fecha, 'dd/MM/yyyy') order by to_char(c.fecha, 'dd/MM/yyyy') asc 
    )  
 LOOP
        cantidad := var_r.cantidad; 
         fecha := var_r.fecha;
        RETURN NEXT;
 END LOOP;
END; $$ 
LANGUAGE 'plpgsql';

SELECT * FROM fn_listarResumen();
```

### Enlaces de interes

https://www.freeformatter.com/mime-types-list.html

https://github.com/VadimDez/ng2-pdf-viewer

https://www.chartjs.org/docs/latest/getting-started/usage.html

### Tarea 2

- Realizar UN CRUD con Angular y Spring de las tablas Persona y Producto de la tarea1
- Realizar una interfaz para Venta|Detalle similar a lo realizado en clase (escoger cualquiera de las tres formas que hemos visto)

Considerar el uso de switchMap en el método modificar, registrar y eliminar según lo realizado en clase [componente especialidad-edicion]

Enviar el repo backend y frontend al correo cursos@mitocodenetwork.com
