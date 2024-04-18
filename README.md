# Proyecto de Backend para Sistema de Tienda

Este proyecto es el MVP asignado como trabajo final integrador de la materia "Ingeniería de Software", 4to año de ISI, UTN-FRT. 

## Características principales

- **Tecnologías utilizadas**: .NET Core, ASP.NET, EF Core con Code First, MediatR para implementar CQRS, FluentValidation para validación de inputs, Mapster para mapeo de comandos y queries, XUnit para pruebas unitarias.
- **Operaciones soportadas**: El backend ofrece todas las operaciones del MVP de venta, incluyendo registro de usuarios, inicio de sesión, creación de nuevas ventas, búsqueda de artículos por código en sucursal, gestión de líneas de venta, consulta de venta actual, métodos de pago (tarjeta y efectivo), gestión de clientes, cancelación y confirmación de ventas.

## Estructura del proyecto
- **Capa de Presentación**: Aloja controladores, requests y responses necesarios para la interacción con el frontend.
- **Capa de Aplicación**: Define los comandos y queries para cada funcionalidad, incluyendo validación opcional, así como los handlers y DTOs correspondientes. Además, define un behavior de validación y uno de startup usando MediatR.
- **Capa de Dominio**: Define los agregados, relaciones entre ellos, errores utilizando ErrorOr, eventos del dominio, excepciones del dominio y contratos de repositorios y gateways.
- **Capa de Infraestructura**: Implementa los repositorios, el generador de tokens, los gateways, los adaptadores y la configuración de la base de datos. También incluye interceptores para la publicación de eventos del dominio.