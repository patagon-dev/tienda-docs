---
title: seller-relations
description: 
published: true
date: 2024-10-31T17:33:22.842Z
tags: 
editor: markdown
dateCreated: 2024-10-28T20:14:35.878Z
---

# Seller User Relations

## Resume

> The following API returns all the related Companies for a particular Seller. 
{.is-info}


## Request

```jsx
GET {{HOST}}/interoperabilidad/tienda/api/v1/usuario/55555555/proveedor' \
--header 'Authorization: Bearer {{token}}'

```

## Response

```jsx
{
    "code": 200,
    "isSuccessStatusCode": true,
    "content": {
        "rutUsuario": "55555555",
        "rutProveedor": "76191389",
        "nombreProveedor": "SERVICIOS Y MAQUILA SERVICE LTDA.  ",
        "activo": true
    }
}
```