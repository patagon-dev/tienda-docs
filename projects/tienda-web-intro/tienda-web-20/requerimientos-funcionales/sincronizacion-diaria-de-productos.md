---
title: Sincronización de Productos de la Tienda
description: 
published: true
date: 2024-12-09T21:59:53.262Z
tags: 
editor: markdown
dateCreated: 2024-12-09T21:59:53.262Z
---

# Resumen
> Your content here
{.is-success}



# Lógica o secuencia

> El siguiente flujo recorre los productos disponibles en la Tienda Web, y luego por cada uno de ellos realiza una consulta para obtener los datos de Stock y fechas de fin de contrato.
{.is-info}


```mermaid
sequenceDiagram
    Mageai ->> Tienda Web: Obtener listado de<br>productos activos
    Tienda Web -->> Mageai: Retorna un listado con códigos ZCEN
    Mageai ->> API Cenabast: Consulta por cada ZCEN
    Mageai -->> Tienda Web: Actualiza información en Tienda Web
    
```