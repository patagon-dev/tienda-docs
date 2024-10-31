---
title: seller-user-info
description: 
published: true
date: 2024-10-31T17:40:41.492Z
tags: 
editor: markdown
dateCreated: 2024-10-28T20:14:37.848Z
---

# Seller User Info

## Resume

> The following API returns the Seller User information.
{.is-info}


## Request

```jsx
GET {{HOST}}/interoperabilidad/tienda/api/v1/proveedor/usuario/55555555' \
--header 'Authorization: Bearer {{token}}'

```

## Response

```jsx
{
    "code": 200,
    "isSuccessStatusCode": true,
    "content": {
        "rutUsuario": 55555555,
        "dv": "5",
        "nombres": "Prueba",
        "apellidoPaterno": "Prueba",
        "apellidoMaterno": "Prueba",
        "nombreCompleto": "Prueba Prueba Prueba",
        "email": "pedroz21@gmail.com",
        "telefono": "",
        "movil": "",
        "activo": true
    }
}
```