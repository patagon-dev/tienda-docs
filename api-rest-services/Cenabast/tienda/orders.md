---
title: orders
description: 
published: true
date: 2024-10-31T17:29:50.229Z
tags: 
editor: markdown
dateCreated: 2024-10-28T20:14:31.984Z
---

# Historic Orders

> This is a share API with [forecast](./forecast.md), but for Historic Orders, we should ONLY select values which producto ID is 50000*
{.is-warning}


## Request 

> This endpoints fetchs all orders for a given institution. 
{.is-info}


```jsx
GET '{{host}}}}/interoperabilidad/servicios/v1/tienda/demandaprogramada/{{rut-solicitante}}/{{rut-destinatario}}/{{mes}}/{{año}}' \
--header 'Authorization: Bearer {{token}}'
```

## Response

> Only select values which `CodigoGenericoCodigoGeneric` starts with `50000*`. Only then the `NombreGenerico` product name corresponds to the [ZCEN](../../../business/products.mdx) product.
{.is-warning}


> As order date, please consider the value of `ValidoDesde`
{.is-success}


```jsx
[
    {
        "Oferta": "0308371951",
        "Posicion": "000010",
        "RutSolicitante": "0069070900",
        "NombreSolicitante": null,
        "RutDestinatario": "0000200024",
        "NombreDestinatario": "CESFAM CARLOS GODOY",
        "OrganizacionVenta": "5000",
        "Canal": "01",
        "Direccion": "AVDA CONQUISTADORES 1565",
        "Sector": "S1",
        "CodigoGenerico": "000000000500000097",
        "NombreGenerico": "ABECIDIN ACD SOL.ORAL 30 ML CAJ 25 FRA",
        "ValidoDesde": "20230201",
        "ValidoHasta": "20230228",
        "CantidadUnitariaProgramada": 7.000,
        "ValorizadoProgramado": 141925.00,
        "MotivoRechazo": " ",
        "Comuna": "MAIPU",
        "Region": "METROPOLITANA DE SANTIAGO"
    },
    {
        "Oferta": "0308372708",
        "Posicion": "000010",
        "RutSolicitante": "0069070900",
        "NombreSolicitante": null,
        "RutDestinatario": "0000200024",
        "NombreDestinatario": "CESFAM CARLOS GODOY",
        "OrganizacionVenta": "5000",
        "Canal": "01",
        "Direccion": "AVDA CONQUISTADORES 1565",
        "Sector": "S1",
        "CodigoGenerico": "000000000500000113",
        "NombreGenerico": "FERRIGOT 125MG/ML SOL ORAL 30ML CAJ25FRA",
        "ValidoDesde": "20230201",
        "ValidoHasta": "20230228",
        "CantidadUnitariaProgramada": 1.000,
        "ValorizadoProgramado": 15850.00,
        "MotivoRechazo": " ",
        "Comuna": "MAIPU",
        "Region": "METROPOLITANA DE SANTIAGO"
    },
    ...
```