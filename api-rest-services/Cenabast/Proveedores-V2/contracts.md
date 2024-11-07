---
title: Contrats
description: 
published: true
date: 2024-11-07T19:37:44.588Z
tags: 
editor: markdown
dateCreated: 2024-10-28T20:14:10.487Z
---

# Resume

> After an auction, the winner bidder signs a contract with Cenabast.
{.is-success}


# API example

> **Request API for producto ZGEN: 100003753**
{.is-info}

> One product **can have multiple contracts** or PedidoCompra.
{.is-danger}



```jsx
POST {{host}}/WebApi2/api/v2/Public/contrato \
  --header 'Authorization: {{token}}' \
  --data '{
"ZGEN": "100003753"
}'
```

> **Response:**

```jsx
[
  {
    "PedidoCompra": "4500026400",
    "IdMercadoPublico": "621-1224-SE21     ",
    "ordenDeCompra": "621-460-LR21      ",
    "Posicion": "120",
    "fechaEntrega": "01-12-2022 0:00:00",
    "ZGEN": "100003753",
    "NombreZgen": "FINGOLIMOD 0,5 MG CP                    ",
    "GrupoArticulo": "3RI      ",
    "ZCEN": "500007740",
    "NombreZCEN": "EMINOD (FINGOLIMOD) 0,5 MG CAJ 30 CP    ",
    "Cantidad": 30,
    "UnidadVenta": "CAJ",
    "NombreProveedor": "ASCEND LABORATORIES SPA",
    "RutProveedorSinDv": 76175092,
    "RutProveedorConDv": "76175092-5",
    "ValorNeto": 21000.0,
    "Valoriva": 3990.0,
    "ValorTotal": 24990.0,
    "FInicialContrato": "202201",
    "FFinalContrato": "202306"
  },
  {

  }
 ]
```

> 
> <mark>When listing all available contracts, the information given is related to the programmed purchase, which shows the QTY per month</mark>. So in the example above, the position <kbd>120</kbd> represents December (Month: 12).
{.is-success}


![2023-11-06_18-25_1.png](/images/images/2023-11-06_18-25_1.png)