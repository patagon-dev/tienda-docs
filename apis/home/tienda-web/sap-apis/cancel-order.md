---
title: cancel-order
description: 
published: true
date: 2024-10-31T17:39:18.129Z
tags: 
editor: markdown
dateCreated: 2024-10-28T20:14:55.663Z
---

# Cancel Order

## Resume

> Dev HOST: <kbd>testaplicacionesweb.cenabast.cl:7001</kbd>
{.is-info}


## Request

```jsx
PATCH '{{HOST}}/interoperabilidad/tienda/api/v1/pedido/CancelarPedido/{{PV}}'
```
Donde PV = id de pedido de venta SAP

## Response

```jsx
{
  "code": 200,
    "isSuccessStatusCode": true,
    "content": [
    {
      "pedidoId": 25,
      "fechaCreacion": "2024-04-05T14:59:15.0426499-03:00",
      "zcen": "500006843",
      "pedidoVentaId": 55005002
    }
  ]
}
```
