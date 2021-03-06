# 3) Buenas prácticas servicios REST



[Buenas prácticas en servicios REST](Buenas%20prácticas%20REST.pdf)

### Tarea 1

Crear un simple backend con estás indicaciones (SERVICIOS REST)

Persona  [CRUD]

idPersona

nombres        : string

apellidos    : string

Producto [CRUD]

idProducto     : int

nombre         : string

marca        : string

Venta [Crear]

idVenta        : int

fecha        : LocalDateTime

idPersona    : Persona

importe        : double

DetalleVenta

idDetalleVenta        : int

idVenta            : Venta

idProducto        : Producto

cantidad        : int

JSON EJEMPLO Consulta - DetalleConsulta (similar para este caso)

```jsx
{
    "paciente" : {
        "idPaciente" : 1
    },
    "medico" : {
        "idMedico" : 1
    },
    "especialidad" : {
        "idEspecialidad" : 1
    },
    "fecha" : "2018-06-19T05:00:00.000Z",
    "detalleConsulta" : [
        { "diagnostico" : "FIEBRE", "tratamiento" : "PARACETAMOL"},    
        { "diagnostico" : "AMIGDALITIS", "tratamiento" : "ANTIBIOTICOS"}
    ]
}
```

Obviamente para que pueda funcionar debe primero hacer inserciones para data de producto y persona con sus servicios REST creados [POST]

Deberá subir el código de los servicios REST a su cuenta de bitbucket, gitlab o github y enviar el link del repositorio al correo.

cursos@mitocodenetwork.com

PDA: Los crud son para las entidades Persona y Producto, la tabla Venta y DetalleVenta solo programar la funcionalidad de registrar

- Todo es muy similar a lo visto en clase
