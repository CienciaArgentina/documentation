# Table of content

- [Bases de datos](#bases-de-datos)
	- [Nomenclatura de los nombres de las bases de datos](#nomenclatura-de-los-nombres-de-las-bases-de-datos)
	- [Naming conventions para las bases de datos de Ciencia Argentina](#naming-conventions-para-las-bases-de-datos-de-ciencia-argentina)
- [JSON](#json)
	- [Formato](#formato)

## Bases de datos

### Nomenclatura de los nombres de las bases de datos
Para poder identificar a qué entorno pertenece cada DB debería quedar estandarizado que:

- El nombre productivo va a ser la base para el resto de los entornos (ejemplo: `user`) y la nomenclatura es camelCase.
	
- La base de datos de pruebas equivalente, NO local, **tiene** que terminar con el sufijo "dev" con la letra "d" en minúscula (ej. `userdev`).

### Naming conventions para las bases de datos de Ciencia Argentina
- El nombre de tablas en singular
- El nombre de las columnas en snake_case
- Los campos de Id numéricos, salvo que sea necesario que deberían ser del tipo `BIGINT`

## Dev agreement Api

### Naming 
- Recursos en plural con nomenclatura spinal-case (ejemplo: `/user-profile`).
- No usar verbos para el nombre de los recursos, solo sustantivos.
- Recursos en inglés. 
- Debe evitarse pero en casos necesarios el nivel máximo de anidamiento es dos (ejemplo: `/organizations/:id/institutes/:id`). 
En caso de usarse debe ir lo más general a lo más especifico. 
- No filtrar atributos a través del endpoint (ejemplo: `/user-profile/:id/name`).
- No usar caracteres especiales (&,#,ñ, etc) (ejemplo: `/job&offers`). 
- No usar nombres ambiguos (ejemplo: `/results`,`/responses`).

### Nombre entidad / tag

### Paginado y Sort

### Verbos HTTP

### Headers

### Errores

### Operaciones Bulk

### Versionado

### Cache

### Acciones

### Status code


Ejemplo /organizations/v2

### Formato
El formato que vamos a utilizar en Ciencia Argentina para los JSON es snake_case

## Dev Agreement versionado de código
