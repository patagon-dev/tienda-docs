---
title: Captura Documento Cedible
description: 
published: true
date: 2024-11-21T14:24:25.251Z
tags: 
editor: markdown
dateCreated: 2024-11-20T19:24:41.034Z
---

# Resumen
> Procesos que capturan el documento emitido por los proveedores.
> 
> Actualmente existen 3 procesos que permiten capturar el documento cedible.
{.is-success}

> Por las bases 87, los proveedores **<mark>están obligados</mark>** a utilizar: o el método de API proveedores, o la captura del documento Tributario (XML) para informar la generación del documento electrónico.
{.is-info}


# 1. WebDimPro (<kbd>deprecado</kbd>)

> Es una plataforma para que los proveedores informen manualmente su documento cedible. Requería subir una foto del documento firmado por el receptor. Si bien está operativo, este proceso está depecrado en las bases 87.
{.is-danger}


# 2. API proveedores

> Existen **2 versiones** de la API de proveedores. 
> 
> A diferencia de la captura por Documento Tributario, la API proveedores solicita más información, como el número de lote, y el código Cenabast del artículo (ZGEN)
{.is-info}

## v1

> Se puede utilizar la API pública para pregunta si existe un documento asociado. Es obligatorio utilizar el Número de Pedido Cenabast para preguntar a la API.
{.is-warning}


- [API proveedores V1 *Swagger UI*](https://aplicacionesweb.cenabast.cl/webapi/swagger/ui/index#!/Public/Public_Get_Cedible)
{.links-list}

## v2

> A diferencia de la V1, en esta versión se requiere utilizar credenciales.
> 
{.is-info}

- [API proveedores V2](https://testaplicacionesweb.cenabast.cl/WebApi2/documentacion/index.html#!/Public/Public_Get_Cedible)
{.links-list}

# 3. Captura Documento Tributario (XML)

> Es un proceso que toma los documentos XML que se copian al correo `copiafactura@cenabast.cl`. Dicho proceso toma los documentos, los procesa, y luego los "inyecta" a SAP.
