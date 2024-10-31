---
title: buyer-user-info
description: 
published: true
date: 2024-10-31T17:27:43.862Z
tags: 
editor: markdown
dateCreated: 2024-10-28T20:14:26.071Z
---

# Buyer User info

## Resume

:::info
The following API returns the buyer user information.
:::

## Request

```jsx
GET {{HOST}}/interoperabilidad/tienda/api/v1/establecimiento/usuario/88888888' \
--header 'Authorization: Bearer {{token}}'
```

## Response

```jsx
{
    "code": 200,
    "isSuccessStatusCode": true,
    "content": {
        "rutUsuario": 88888888,
        "dv": "8",
        "nombres": "PRUEBA 8",
        "apellidoPaterno": "PRUEBA",
        "apellidoMaterno": "PRUEBA",
        "nombreCompleto": "PRUEBA 8 PRUEBA PRUEBA",
        "email": "pzuniga@cenabast.cl",
        "telefono": "956393313",
        "movil": "956393313",
        "activo": true
    }
}
```