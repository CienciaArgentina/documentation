# Table of content

- [Bases de datos](#bases-de-datos)
	- [Nomenclatura de los nombres de las bases de datos](#nomenclatura-de-los-nombres-de-las-bases-de-datos)
	- [Naming conventions para las bases de datos de Ciencia Argentina](#naming-conventions-para-las-bases-de-datos-de-ciencia-argentina)
- [JSON](#json)
	- [Formato](#formato])

## Bases de datos

### Nomenclatura de los nombres de las bases de datos
Para poder identificar a qué entorno pertenece cada DB debería quedar estandarizado que:

- El nombre productivo va a ser la base para el resto de los entornos (ej. `user`)
	
- La base de datos de pruebas equivalente, NO local, **tiene** que terminar con el sufijo "dev" con la letra "d" en minúscula (ej. `userdev`)

### Naming conventions para las bases de datos de Ciencia Argentina
- El nombre de tablas en singular
- El nombre de las columnas en snake case
- Los campos de Id numéricos, salvo que sea necesario que deberían ser del tipo `BIGINT`

## JSON

### Formato
El formato que vamos a utilizar en Ciencia Argentina para los JSON es snake case