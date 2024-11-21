---
title: Buyer Users Relations
description: 
published: true
date: 2024-11-21T20:36:38.356Z
tags: 
editor: markdown
dateCreated: 2024-10-28T20:14:41.722Z
---

# Buyer User relations

## Resume

> The following API returns all the related institutions for a particular **buyer** user.
{.is-info}


## Request

```jsx
GET '{{host}}/interoperabilidad/tienda/api/v1/destinatarios/88888888' \
--header 'Authorization: Bearer {{token}}'

```

# Respuesta {.tabset}

## JSON
```json
{
    "code": 200,
    "isSuccessStatusCode": true,
    "content": [
        {
            "rutUsuario": 0,
            "idRelacion": 3724,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 200911,
            "destinatario": "CONS.DR.ALEJANDRO DEL RIO",
            "canal": 1,
            "nombreCanal": "INTERMEDIACION",
            "direccionDespacho": "GANDARILLAS 105"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 28437,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 200911,
            "destinatario": "CONS.DR.ALEJANDRO DEL RIO",
            "canal": 67,
            "nombreCanal": "ECOMMERCE",
            "direccionDespacho": "GANDARILLAS 105"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 184,
            "rutSolicitante": 61606918,
            "solicitante": "HOSPITAL PARRAL",
            "rutDestinatario": 201497,
            "destinatario": "HOSPITAL PARRAL GENERAL",
            "canal": 1,
            "nombreCanal": "INTERMEDIACION",
            "direccionDespacho": "ANIBAL PINTO 1225"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 28431,
            "rutSolicitante": 61606918,
            "solicitante": "HOSPITAL PARRAL",
            "rutDestinatario": 201497,
            "destinatario": "HOSPITAL PARRAL GENERAL",
            "canal": 67,
            "nombreCanal": "ECOMMERCE",
            "direccionDespacho": "ANIBAL PINTO 1225"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 711,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 201717,
            "destinatario": "FARMACIA SOLIDARIA PUENTE ALTO",
            "canal": 1,
            "nombreCanal": "INTERMEDIACION",
            "direccionDespacho": "BALMACEDA 265"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 28436,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 201717,
            "destinatario": "FARMACIA SOLIDARIA PUENTE ALTO",
            "canal": 67,
            "nombreCanal": "ECOMMERCE",
            "direccionDespacho": "BALMACEDA 265"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 5666,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 201752,
            "destinatario": "CORP.MUNIC.PUENTE ALTO GENERAL",
            "canal": 1,
            "nombreCanal": "INTERMEDIACION",
            "direccionDespacho": "TOCORNAL 70"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 28438,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 201752,
            "destinatario": "CORP.MUNIC.PUENTE ALTO GENERAL",
            "canal": 67,
            "nombreCanal": "ECOMMERCE",
            "direccionDespacho": "TOCORNAL 70"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 14630,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 205536,
            "destinatario": "CESFAM SAN GERONIMO",
            "canal": 1,
            "nombreCanal": "INTERMEDIACION",
            "direccionDespacho": "SAN PEDRO 1203"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 28439,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 205536,
            "destinatario": "CESFAM SAN GERONIMO",
            "canal": 67,
            "nombreCanal": "ECOMMERCE",
            "direccionDespacho": "SAN PEDRO 1203"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 14631,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 205537,
            "destinatario": "CESFAM VISTA HERMOSA",
            "canal": 1,
            "nombreCanal": "INTERMEDIACION",
            "direccionDespacho": "EL VOLCAN 04549"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 28440,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 205537,
            "destinatario": "CESFAM VISTA HERMOSA",
            "canal": 67,
            "nombreCanal": "ECOMMERCE",
            "direccionDespacho": "EL VOLCAN 04549"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 14632,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 205538,
            "destinatario": "CESFAM BERNARDO LEIGHTON",
            "canal": 1,
            "nombreCanal": "INTERMEDIACION",
            "direccionDespacho": "MIGUEL ANGEL 1929"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 28441,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 205538,
            "destinatario": "CESFAM BERNARDO LEIGHTON",
            "canal": 67,
            "nombreCanal": "ECOMMERCE",
            "direccionDespacho": "MIGUEL ANGEL 1929"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 14633,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 205539,
            "destinatario": "CESFAM CARD RAUL SILVA HENRIQU",
            "canal": 1,
            "nombreCanal": "INTERMEDIACION",
            "direccionDespacho": "SAN PEDRO 3345"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 28442,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 205539,
            "destinatario": "CESFAM CARD RAUL SILVA HENRIQU",
            "canal": 67,
            "nombreCanal": "ECOMMERCE",
            "direccionDespacho": "SAN PEDRO 3345"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 14634,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 205580,
            "destinatario": "CESFAM PADRE MANUEL VILLASECA",
            "canal": 1,
            "nombreCanal": "INTERMEDIACION",
            "direccionDespacho": "LUIS MATTE LARRAIN 02312"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 28443,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 205580,
            "destinatario": "CESFAM PADRE MANUEL VILLASECA",
            "canal": 67,
            "nombreCanal": "ECOMMERCE",
            "direccionDespacho": "LUIS MATTE LARRAIN 02312"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 14635,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 205581,
            "destinatario": "CESFAM KAROL WOJTYLA",
            "canal": 1,
            "nombreCanal": "INTERMEDIACION",
            "direccionDespacho": "CURACO DE VELEZ 4110"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 28444,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 205581,
            "destinatario": "CESFAM KAROL WOJTYLA",
            "canal": 67,
            "nombreCanal": "ECOMMERCE",
            "direccionDespacho": "CURACO DE VELEZ 4110"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 14636,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 205582,
            "destinatario": "CESFAM LAURITA VICUNA",
            "canal": 1,
            "nombreCanal": "INTERMEDIACION",
            "direccionDespacho": "EJERCITO LIBERTADOR 2433"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 28445,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 205582,
            "destinatario": "CESFAM LAURITA VICUNA",
            "canal": 67,
            "nombreCanal": "ECOMMERCE",
            "direccionDespacho": "EJERCITO LIBERTADOR 2433"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 14637,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 205583,
            "destinatario": "CEP SAN LAZARO",
            "canal": 1,
            "nombreCanal": "INTERMEDIACION",
            "direccionDespacho": "SARGENTO MENADIER 1092"
        },
        {
            "rutUsuario": 0,
            "idRelacion": 28446,
            "rutSolicitante": 70856400,
            "solicitante": "CORP.MUNIC.PUENTE ALTO",
            "rutDestinatario": 205583,
            "destinatario": "CEP SAN LAZARO",
            "canal": 67,
            "nombreCanal": "ECOMMERCE",
            "direccionDespacho": "SARGENTO MENADIER 1092"
        }
    ],
    "errorMessage": null
}
```

## Visibilidad Tabla Resumida

| rutUsuario | idRelacion | rutSolicitante | solicitante            | rutDestinatario | destinatario                   | canal | nombreCanal    | direccionDespacho        |
|------------|------------|----------------|------------------------|-----------------|--------------------------------|-------|----------------|--------------------------|
| 0          | 3724       | 70856400       | CORP.MUNIC.PUENTE ALTO | 200911          | CONS.DR.ALEJANDRO DEL RIO      | 1     | INTERMEDIACION | GANDARILLAS 105          |
| 0          | 184        | 61606918       | HOSPITAL PARRAL        | 201497          | HOSPITAL PARRAL GENERAL        | 1     | INTERMEDIACION | ANIBAL PINTO 1225        |
| 0          | 711        | 70856400       | CORP.MUNIC.PUENTE ALTO | 201717          | FARMACIA SOLIDARIA PUENTE ALTO | 1     | INTERMEDIACION | BALMACEDA 265            |
| 0          | 5666       | 70856400       | CORP.MUNIC.PUENTE ALTO | 201752          | CORP.MUNIC.PUENTE ALTO GENERAL | 1     | INTERMEDIACION | TOCORNAL 70              |
| 0          | 14630      | 70856400       | CORP.MUNIC.PUENTE ALTO | 205536          | CESFAM SAN GERONIMO            | 1     | INTERMEDIACION | SAN PEDRO 1203           |
| 0          | 14631      | 70856400       | CORP.MUNIC.PUENTE ALTO | 205537          | CESFAM VISTA HERMOSA           | 1     | INTERMEDIACION | EL VOLCAN 04549          |
| 0          | 14632      | 70856400       | CORP.MUNIC.PUENTE ALTO | 205538          | CESFAM BERNARDO LEIGHTON       | 1     | INTERMEDIACION | MIGUEL ANGEL 1929        |
| 0          | 14633      | 70856400       | CORP.MUNIC.PUENTE ALTO | 205539          | CESFAM CARD RAUL SILVA HENRIQU | 1     | INTERMEDIACION | SAN PEDRO 3345           |
| 0          | 14634      | 70856400       | CORP.MUNIC.PUENTE ALTO | 205580          | CESFAM PADRE MANUEL VILLASECA  | 1     | INTERMEDIACION | LUIS MATTE LARRAIN 02312 |
| 0          | 14635      | 70856400       | CORP.MUNIC.PUENTE ALTO | 205581          | CESFAM KAROL WOJTYLA           | 1     | INTERMEDIACION | CURACO DE VELEZ 4110     |
| 0          | 14636      | 70856400       | CORP.MUNIC.PUENTE ALTO | 205582          | CESFAM LAURITA VICUNA          | 1     | INTERMEDIACION | EJERCITO LIBERTADOR 2433 |
| 0          | 14637      | 70856400       | CORP.MUNIC.PUENTE ALTO | 205583          | CEP SAN LAZARO                 | 1     | INTERMEDIACION | SARGENTO MENADIER 1092   |
| 0          | 28437      | 70856400       | CORP.MUNIC.PUENTE ALTO | 200911          | CONS.DR.ALEJANDRO DEL RIO      | 67    | ECOMMERCE      | GANDARILLAS 105          |
| 0          | 28431      | 61606918       | HOSPITAL PARRAL        | 201497          | HOSPITAL PARRAL GENERAL        | 67    | ECOMMERCE      | ANIBAL PINTO 1225        |
| 0          | 28436      | 70856400       | CORP.MUNIC.PUENTE ALTO | 201717          | FARMACIA SOLIDARIA PUENTE ALTO | 67    | ECOMMERCE      | BALMACEDA 265            |
| 0          | 28438      | 70856400       | CORP.MUNIC.PUENTE ALTO | 201752          | CORP.MUNIC.PUENTE ALTO GENERAL | 67    | ECOMMERCE      | TOCORNAL 70              |
| 0          | 28439      | 70856400       | CORP.MUNIC.PUENTE ALTO | 205536          | CESFAM SAN GERONIMO            | 67    | ECOMMERCE      | SAN PEDRO 1203           |
| 0          | 28440      | 70856400       | CORP.MUNIC.PUENTE ALTO | 205537          | CESFAM VISTA HERMOSA           | 67    | ECOMMERCE      | EL VOLCAN 04549          |
| 0          | 28441      | 70856400       | CORP.MUNIC.PUENTE ALTO | 205538          | CESFAM BERNARDO LEIGHTON       | 67    | ECOMMERCE      | MIGUEL ANGEL 1929        |
| 0          | 28442      | 70856400       | CORP.MUNIC.PUENTE ALTO | 205539          | CESFAM CARD RAUL SILVA HENRIQU | 67    | ECOMMERCE      | SAN PEDRO 3345           |
| 0          | 28443      | 70856400       | CORP.MUNIC.PUENTE ALTO | 205580          | CESFAM PADRE MANUEL VILLASECA  | 67    | ECOMMERCE      | LUIS MATTE LARRAIN 02312 |
| 0          | 28444      | 70856400       | CORP.MUNIC.PUENTE ALTO | 205581          | CESFAM KAROL WOJTYLA           | 67    | ECOMMERCE      | CURACO DE VELEZ 4110     |
| 0          | 28445      | 70856400       | CORP.MUNIC.PUENTE ALTO | 205582          | CESFAM LAURITA VICUNA          | 67    | ECOMMERCE      | EJERCITO LIBERTADOR 2433 |
| 0          | 28446      | 70856400       | CORP.MUNIC.PUENTE ALTO | 205583          | CEP SAN LAZARO                 | 67    | ECOMMERCE      | SARGENTO MENADIER 1092   |
