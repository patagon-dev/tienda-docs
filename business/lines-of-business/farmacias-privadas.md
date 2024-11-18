---
title: Farmacias Privadas
description: 
published: true
date: 2024-11-18T16:35:52.932Z
tags: 
editor: markdown
dateCreated: 2024-10-31T15:19:31.103Z
---

# Resumen
> Linea de negocio de Farmacias Privadas
{.is-success}

# Modelo de Negocio

> En la actualidad las Farmacias Privadas que solicitan a CENABAST, poder adquirir medicamentos, <kbd>tienen que cumplir con algunos requisitos legales, Sanitarios y financieros</kbd>,  los cuales una vez cumplidos, se procede a la firma de un Convenio bilateral entre la Farmacia y CENABAST.
{.is-danger}


## Habilitación en SAP SD XD 01 Maestro Clientes 

> Posteriormente a las farmacias se les asignan permisos para acceder a  una plataforma web de programación, a la cual  acceden  una vez por semana durante 3  días.
{.is-info}


> **Pedidos de Compra**:  para Farmacias  Cantidad asignada a línea farmacia
> Inteligencia de negocios estimación de demanda para Farmacias
> 
> **Distribución mensual**: Sí, generan 18 posiciones 
> 
> Mensualmente **se ajustan los contratos** para solicitar a los proveedores las cantidades requeridas, conversando con  el proveedor, dando mayor flexibilidad a la demanda
> 
> **Responsabilidad proveedor**: igual al centro 5000 sólo distribuyen al OL mensualmente. 
{.is-success}


> Los productos que son disponibilizados para las farmacias, son adquiridos por Cenabast vía licitación conjunta, es decir se compra a través de una licitación para al menos tres líneas de negocio (PM, Intermediación y Farmacias privadas). La definición de cantidades que se asignan a esta línea de operación es de acuerdo a XXXXXX
{.is-info}

> Balanceo de cantidades entre diferentes líneas: Si  si falta o sobra en Intermediación .
> 
> La plataforma permite la publicación de productos con stock disponible y cada farmacia selecciona uno o varios productos en las cantidades que requiere y se generan solicitudes 
> (carritos de  martes a jueves), pueden generar varios carritos hay límites de mínimos de compra: 100 mil pesos por carrito.
{.is-warning}


> Solo farmacias independientes. 

## Descripción SAP: 

Captura demanda en plataforma web

a)Ingresos de material: en logística del giro (farmacias)  
mensualmente se ajustan los pedidos y se contacta al proveedor
Logística-contratos administran los contratos y los stock Transacción ME23N
RPA  bot ajusta mensualmente y masivamente los pedidos de compra a los proveedores
Manualmente se ingresan los stock con la confirmación del OL Novofarma: Cantidades, lote , fecha vencimiento
Listo materiales para vender

b) Inyección ofertas en SAP: Stock por RFC que lee el stock del almacén 6101 centro 6000 
Para poder vender se publica el stock disponible para venta en plataforma

b1. publicación
b2. captura de los carritos
b3.- Inyección a SAP: botón que PZúñiga habilitó. Equipo NConcha encienden y apagan la plataforma. Y hay otro botón que indica carga a SAP


Validación: de funcionamiento. Hoy plataforma  tiene 10 disponibles y permite comprar más
c) Distribución: para generación de ofertas en SAP (ZSD_MON_REP_1000) , valida habilitación del cliente, de los materiales para centro 6000. 
Antes de integrar los registros a SAP Pedro Zúñiga (administración de plataforma)  realiza una consolidación por DM por ZGEN y ZCEN.
Esta oferta revisa si tiene stock disponible por flujos de materiales de bodega OL. Semanalmente se valida nuevamente.
Generación de pedido de venta: ZSDIS004N toma las ofertas y les asigna stock: distribuye
Con la generación del Pedido de venta se genera automáticamente una Entrega de Salida (ZSDIS004N ). se puede hacer manualmente pero si se hace con un JOB
Carga a Novofarma: listado de pedidos que tiene que preparar y distribuir a las farmacias.
Validación de stock con Novofarma por no estar en línea antes de enviarle a OL

Por página web del Operador Logístico (OL) usando planilla excel y/o por transacción en SAP (interoperabilidad)  carga de entregas, transacción VL71. Cada vez que se cierra la plataforma se le carga a novofarma. 
La carga contempla Cenabast define fecha de entrega, material,  cantidades 
Opcionalmente se puede entregar  lote y serie. El OL confirma a través de interoperabilidad sistémicamente las cantidades y el lote asignado. Con esto se contabiliza el stock, se rebaja y se genera la guía de despacho por cada entrega (viene del doc de venta , de la oferta y de la consolidación de carritos por cliente) Si un cliente programa más de 12 productos se genera otra oferta.

Plazos de despacho: tiempo en tránsito por contrato. Se le dan 2 días hábiles para preparar pedidos. Lista (mati)

