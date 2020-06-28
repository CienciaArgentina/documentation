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

### Verbos HTTP

<table>
  <tr>
    <td>Método HTTP</td>
    <td>POST</td>
    <td>GET</td>
    <td>PUT/PATCH</td>
    <td>DELETE</td>
  </tr>
  <tr>
    <td>Operación</td>
    <td>CREATE</td>
    <td>READ</td>
    <td>UPDATE</td>
    <td>DELETE</td>
  </tr>
  <tr>
    <td>/organizations</td>
    <td>Crea nueva organización</td>
    <td>Lista de organizaciones</td>
    <td>Error</td>
    <td>Elimina todas las organizaciones</td>
  </tr>
  <tr>
    <td>/organizations/1234</td>
    <td>Error</td>
    <td>Muestra la organización 1234</td>
    <td>Si existe, actualiza la organización; sino, devuelve error.</td>
    <td>Borra 1234</td>
  </tr>
</table>

### Headers

- Content-Type: Indicar tipo de contenido que se envía (`ejemplo: application/json`).
- x-request-id: Identificador e2e de request, tipo a usar: uuid. Si no existe generarlo.
- Authorization: Para autorización de clientes externos

### Segurización
- Autenticación: Usamos OAuth2
- Autorización: OpenID Connect (OIC). 
- Protocolo: HTTPS

### Errores

## Error response
{
    "id":"b7c450ed-03e6-4f62-84f8-0cc60045e74f",
    "status": 400,
    "message": "User or password invalid",
    "errors": 
    [
        {
            "detail":"Password required *",
            "code":"password_invalid"
        },
        {   "detail":"User lenght seven characters",
            "code":"user_invalid"
        }
    ] 
}

### Operaciones Bulk

### Versionado

### Paginado y Sort

### Cache

### Acciones

### Status code


Ejemplo /organizations/v2

### Formato
El formato que vamos a utilizar en Ciencia Argentina para los JSON es snake_case

## Dev Agreement versionado de código
