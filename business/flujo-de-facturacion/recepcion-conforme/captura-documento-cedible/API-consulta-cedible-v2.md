---
title: API Proveedores V2 - Ejemplo Consulta Cedible
description: 
published: true
date: 2024-11-21T21:12:20.891Z
tags: 
editor: markdown
dateCreated: 2024-11-21T21:12:20.891Z
---

# Resumen
Your content here


# Ejemplo

## Autenticación

```ruby
curl --location 'https://testaplicacionesweb.cenabast.cl/WebApi2/api/v2/login/authenticate' \
--header 'Content-Type: application/json' \
--data '{
  "Username": "1",
  "Password": "a"
}'
``` 

### Respuesta Autenticacion

```json
"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1bmlxdWVfbmFtZSI6IjEiLCJyb2xlIjoiUHJvdmVlZG9yIiwibmJmIjoxNzMyMjIzMTYzLCJleHAiOjE3MzIyMjQ5NjMsImlhdCI6MTczMjIyMzE2MywiaXNzIjoiaHR0cDovL2xvY2FsaG9zdC8iLCJhdWQiOiJodHRwOi8vbG9jYWxob3N0LyJ9.9uT-Qs4NyvbQDdtOBzfmvR_Nz1zkuIs3LLMijxflMIw"
```



## Consulta Cedible V2

```ruby
curl --location 'https://testaplicacionesweb.cenabast.cl/WebApi2/api/v2/Public/cedible/300000000' \
--header 'Authorization: Bearer {{token}}'
```

### Respuesta

```json
[
    {
        "IdDistribucionCedible": 1921373,
        "Doc_Cenabast": 300000000,
        "Rut_Proveedor": "1",
        "Documento": "{{base64 code -- convertir a PDF}}",
        "FechaCreacion": "15-11-2024 9:02:31",
        "FechaActualizacion": "15-11-2024 9:02:31"
    }
]
```