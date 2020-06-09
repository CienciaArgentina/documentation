# Bases de datos

## Nomenclatura de los nombres de las bases de datos
Para poder identificar a qué entorno pertenece cada DB debería quedar estandarizado que:

- El nombre productivo va a ser la base para el resto de los entornos (ej. `user`)
	
- La base de datos de pruebas equivalente, NO local, **tiene** que terminar con el sufijo "dev" con la letra "d" en minúscula (ej. `userdev`)

## Naming conventions para Ciencia Argentina
- El nombre de tablas en singular
- El nombre de las columnas en snake case
- Los campos de Id numéricos, salvo que sea necesario que deberían ser del tipo `BIGINT`