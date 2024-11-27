---
title: Informe Levantamiento Situación Actual
description: 
published: true
date: 2024-11-27T13:16:02.325Z
tags: 
editor: markdown
dateCreated: 2024-11-14T19:26:01.519Z
---

# Informe Levantamiento Situación Actual

## Resumen
> El siguiente informe ilustra el estado actual del proyecto Tienda Web, justo antes de dar inicio a la segunda etapa del proyecto. (versión digital [aquí](https://docs.google.com/document/d/1nHaCtGx6YScHOs3NP-RpLYWhXNjNIRgP0MWpPFCMmjA/edit?usp=sharing)
> 
> **🗎 Versión descargable** [informe_levantamiento_situación_actual.pdf](/adjuntos/informe_levantamiento_situación_actual.pdf)
{.is-success}


# Antecedentes previos

## Historia

> Para entender el contexto actual proyecto, es necesario conocer el pasado del proyecto. A continuación se muestra una línea de tiempo con los principales hitos que ha tenido este proyecto a lo largo de su vida.

> <kbd>2018</kbd>: Se firmó un acuerdo de colaboración con ChileCompra para la habilitación y puesta en marcha de una Tienda de productos para Cenabast. En esa línea, se sugirió aprovechar la actual plataforma Magento que utiliza ChileCompra para las tiendas de Convenio Marco, para el desarrollo e implementación de una Tienda con medicamentos e insumos médicos para Cenabast.
> 
> <kbd>2020</kbd>: Se realiza un piloto habilitando una tienda de Cenabast dentro de Mercado Público. Finalmente este piloto fue descartado.
> 
> <kbd>2022</kbd>: Se realizó una consulta al mercado para conocer las soluciones disponibles de proveedores a nivel local.
> 
> <kbd>2023</kbd>: Se levanta requerimiento de un nuevo piloto o MVP a través del Convenio Marco de Desarrollo de Software. Esta vez, se solicitó realizar el proyecto sobre la plataforma Spree Commerce con un diseño modularizado y escalable. 
{.is-info}


## MVP (Etapa 1: Enero 2024 – Abril 2024)

> Considerando el historial previo, se propuso cambiar la plataforma previamente sugerida (Magento) por una solución más liviana y flexible (Spree Commerce). Para ello se realizó un informe técnico en donde se mencionaron las ventajas y desventajas de una y otra solución. 
{.is-warning}

> Los objetivos de este nuevo proyecto piloto, fueron 4:
> 
> 1. Validar que la herramienta Spree Commerce cumpliera con las funcionalidades mínimas requeridas. En particular esto apuntaba a la funcionalidad de “Marketplace”, característica que permite que terceros (proveedores) vendan a través de la plataforma. En general esta funcionalidad no existe de forma nativa en otras plataformas de ecommerce de código abierto.
> 
> 2. Validar la velocidad de desarrollo del framework Ruby on Rails (RoR). Ruby se destaca de otros frameworks por la velocidad para realizar nuevas cosas. Así por ejemplo, lo que en otro framework toma 4 días para una persona, en Ruby se puede realizar en 2 días. 
> 
> 3. Diseñar una arquitectura escalable y resiliente. El proyecto piloto se pensó desde sus inicios como una solución modularizada, en que cada componente está separado del otro. Este permite adaptar de mejor manera y controlada los cambios que se requieren para la tienda. En particular, el proyecto piloto descompuso la solución en 6 grandes componentes:
> - Spree Commerce: Tienda Web
> - Keycloak: Servicio de Single Sign On (SSO) integrado con clave única.
> - Mageai: Servicio de data pipeline para la sincronización de datos.
> - Elasticsearch: Servicio de motor de búsquedas.
> - Sidekiq: Servicio para gestión de tareas y colas.
> - PostgreSQL: Base de datos relacional.
> 
> Adicionalmente, el proyecto se concibió desde el principio utilizando contenedores Docker, de tal forma que el conjunto de servicios puedan ser desplegados en un cluster de Kubernetes, servicio que actualmente es un estándar en la industria.
> 
> 4. Conservar el conocimiento del proyecto. Para evitar o minimizar el riesgo de dependencia del proveedor o de las personas, todos los procesos del proyecto fueron documentados en una plataforma de gestión de conocimiento. 

Una vez finalizada la primera etapa del proyecto, se procedió a levantar las bases técnicas de requerimientos para la segunda etapa, bases que dieron lugar a un proceso de Licitación pública, concurso que se publicó el 27 de agosto del 2024.

# Situación Actual
## Objetivo
> Como objetivo de corto plazo, se ha solicitado la implementación del canal de Farmacias de Cadena en ambiente de producción para el mes de Enero del 2025. 
> 
> Dado lo ambicioso de dicho objetivo (2 meses), y para cumplir con la fecha propuesta, originalmente se pensó utilizar el canal de compra espontánea 一desarrollado en la etapa 1一 como canal para Farmacias de Cadena. Posteriormente sin embargo, se consideró que lo mejor sería habilitar un nuevo canal para Farmacias de Cadena, para así separar las reglas de negocio del canal de compra espontánea.
{.is-info}

## Etapa 2 (Noviembre 2024 - )
> La segunda etapa del proyecto iniciará el miércoles 27 de noviembre con la reunión de kick-off con el proveedor AcidLabs. El proveedor fue adjudicado a través del proceso de licitación 2268-34-LQ24.
> Se trata del mismo proveedor que previamente había realizado el proyecto “Piloto” o “MPV” de la 
> Etapa 1 de Tienda a principios de año, lo que facilitará el proceso de capacitación técnico y de negocios.
> 
> El desarrollo de la Etapa 2 con el proveedor adjudicado, tiene un plazo de ejecución de 24 meses y un presupuesto estimado de 240 millones (impuestos incluidos). Dado que el contrato es por horas de trabajo, la Etapa 2 finalizará cuando se cumpla la primera de las dos restricciones: plazo o presupuesto. 
> 
> Previo a la llegada del proveedor, se trabajó en un plan de trabajo que contempló múltiples áreas. A continuación detallamos los preparativos y actividades que se realizaron para abordar el proyecto de la mejor manera posible.

## Subdivisión del proyecto 
> Para ordenar el proyecto Tienda, éste se subdividió en 8 sub-proyectos que agrupan las distintas tareas y actividades de trabajo. Cada subproyecto está asociado a un equipo o grupo de personas en particular. Esto permitirá tener un mejor control y seguimiento de los requerimientos por cada área. Una mirada general es la siguiente:
{.is-info}

![2024-11-27_10-09.png](/images/2024-11-27_10-09.png)

## Equipo
> Cabe mencionar que los 8 subproyectos arriba mencionados están siendo liderados por Gloria Venegas, quien además cuenta con el apoyo de Claudio Soto y Natalia Martínez para la gestión y seguimiento. Además cuentan con la asesoría y supervisión del consultor externo.
> 
> Adicionalmente el equipo de proyectos reporta los avances y riesgos del proyecto de forma semanal a los jefes de área Diego Martínez y Rodrigo Castro.
{.is-info}

## Gantt
> Antes de la llegada del proveedor adjudicado, se levantaron las distintas actividades para cada una de las divisiones del proyecto. La Gantt completa de actividades se puede consultar acá. La siguiente imagen es una muestra de la Gantt para el proveedor AcidLabs y los primeros requerimientos:
{.is-info}


![2024-11-27_10-11.png](/images/2024-11-27_10-11.png)

> Cada una de las tareas levantadas tiene el detalle del requerimiento, fecha de entrega, prioridad y equipo (o persona) asignada. Los tiempos propuestos de la Gantt actual son estimativos, y deben ser validados por el proveedor.
## Levantamiento de información de Negocios
> Se participó en diferentes reuniones con los equipos de negocio, para levantar información relativa a los flujos de operación de los canales de Farmacias de Cadena y Farmacias Privadas. La información de ambos flujos está siendo procesada y subida a la plataforma de documentación . 
> 
> El 4 de noviembre se levanta con el consultor de Novis la viabilidad de utilizar el canal 67 de compra espontánea habilitado en Tienda, para el canal de Farmacias de Cadena. Se revisan los puntos de conflicto. Por el momento al parecer dicha idea no es la óptima, por lo cual se solicitó mayor información al equipo de Daniella Gonzalez para habilitar nuevos canales para Tienda en SAP. Esta información está pendiente por el momento.
> 
> El 21 de noviembre se conocen los distintos modelos de captura del documento cedible con el equipo de Sergio Brito. (documentación)
> 
> El día 21 de noviembre, se visita el Centro de Distribución logístico de Novofarma (documentación). En dicha reunión se solicitó acceso a los sistemas de Novoforma que permitan leer el stock de los productos, así como el seguimiento del despacho. Lamentablemente no existe un API para leer el stock, pero sí una API para el tracking de los envíos. 
> 
> Paralelamente todos los lunes por la mañana se realizan reuniones de seguimiento de forma presencial en San Eugenio 40. Igualmente se participa todos los miércoles en la reunión de seguimiento y avances con el equipo ampliado. 
## Documentación
> Se migró la documentación del proyecto Tienda a la nueva herramienta de documentación. Asimismo, toda la información que surgió del levantamiento de información fue incorporada en la herramienta de documentación.
{.is-success}

## Herramientas de gestión
> Se trabajó en la habilitación de 4 herramientas de gestión para un mejor seguimiento y control del proyecto:

> proyectos.cenabast.cl
> Esta herramienta de gestión de tareas y seguimiento de proyecto, permitirá llevar un mejor control de las actividades y flujo de trabajo. Entre otras cosas entregará reportería, priorización de actividades, bloqueos, etc. Con todo, permitirá una mejor gestión de las tareas para los equipos del proyecto.
{.is-warning}



> chat-interno.cenabast.cl
> La herramienta de Chat es una solución muy similar a Slack, es decir, una solución de comunicaciones. Esto nos permitirá tener un registro de todas las conversaciones del proyecto. Decisiones que pueden haberse tomado, problemas, o simplemente proveer información de contexto de alguna tarea. 
{.is-warning}


> docs.cenabast.cl
> La solución de documentación dejará un registro de la información que vaya surgiendo del proyecto. La idea es que se utilice la plataforma para documentar todo lo relativo al proyecto. Será utilizada tanto por equipo interno como externo.
{.is-warning}


> tickets-tienda.cenabast.cl
> Esta herramienta de tickets (o ticketera), se habilitó para evaluar la factibilidad de llevar un control y seguimiento de los requerimientos técnicos entre el proveedor y Cenabast. Deberá validarse con el proveedor el uso de esta solución, y, en caso de que no se use, será dada de baja. 
{.is-warning}


> Cabe destacar lo importante que significa el uso de este conjunto de herramientas, ya que permitirá tener una mejor visibilidad del proyecto completo, así como un registro completo de todo el proceso de implementación. Dado que el código de estas soluciones es libre, la información está en control y propiedad de Cenabast, además de que cualquier funcionario de la institución puede acceder a ellas ya que no hay restricción de licencias. 
{.is-danger}


## Infraestructura
> Desde un principio el proyecto se visualizó para ser resiliente y escalable, y, por lo mismo, el diseño de la arquitectura se pensó para ser implementado utilizando un servicio de Kubernetes. 
> Sin embargo, dada la ausencia de este tipo de servicios en la infraestructura interna, de forma provisoria los servicios y aplicaciones de la Tienda fueron implementados en una máquina virtual. Cabe destacar que habilitar contenedores en una máquina virtual tiene varios inconvenientes de manejo y escalabilidad versus una solución de orquestación de contenedores (Kubernetes). Por un lado el despliegue automatizado es más complejo, no es factible el escalamiento y tampoco es una servicio de alta disponibilidad (HA). 
>
> Kubernetes en cambio, es un servicio de alta disponibilidad (HA) que permite el despliegue y escalado automático de aplicaciones, haciendo que sea más eficiente el flujo de desarrollo. 
> Por consiguiente, lo deseable sería habilitar el ambiente de producción de la Tienda bajo un servicio de Kubernetes y no de máquinas virtuales. 
# Riesgos
> Se trabajó en una matriz de riesgos para identificar las áreas o actividades que podrían impactar negativamente la ejecución del proyecto. Para cada uno de los riesgos levantados, se propusieron acciones de mitigación.
{.is-info}

![2024-11-27_10-14.png](/images/img/2024-11-27_10-14.png)

> Por ahora el único riesgo de alto impacto es la dificultad en SAP para priorizar modificaciones o adecuaciones relacionadas con la Tienda. La Tienda depende totalmente de los servicios e información que provee SAP, y son muchas las funcionalidades de SAP que la Tienda requiere para operar adecuadamente. 
{.is-success}



# Conclusiones
> A grandes rasgos la institución está preparada para abordar esta nueva etapa del proyecto. 
> Sin embargo, será necesario ir subsanando, ordenando y construyendo aquellas áreas o zonas grises que no están del todo definidas, o bien se requieren ciertos “resguardos”.
{.is-info}


## Tienda: Un nuevo producto

> Como cabría esperar, cuando se desarrolla un nuevo producto al interior de una organización no existen los roles ni perfiles asociados al producto. Luego no está claro quién es responsable de qué parte, y por lo tanto, el manejo o aceptación del producto se vuelve más complejo. Y esto sucede actualmente con el proyecto Tienda: no hay equipo de negocios para “recibir” las entregas de desarrollo.
>
> Luego, a medida que vaya avanzando el proyecto, será necesario ir definiendo quién será responsable de Negocio de cada uno de los aspectos de la tienda. Algunos ejemplos de ello son:
> - Diseño y UX. Homepage.
> - Flujo de compra y experiencia de usuario para cada uno de los canales.
> - Portal del proveedor.
> - Portal del comprador.
{.is-info}

# Dependencia de terceros críticas
> La tienda se “alimenta” de los datos provenientes de otros sistemas internos. Algunos incidentes o problemas que podría surgir de estas dependencias son:
>
> Actualización de datos de sistemas internos (lentitud, o sincronización tardía). Por ejemplo, al modificar un producto en SAP, la información será reflejada en la Tienda al día siguiente.
>
> Datos inconsistentes o faltantes. Falta ejecutar muchas pruebas con los datos de distintos usuarios que proveen las API, para corregir o habilitar aquellos flujos no determinados. Por ejemplo, si en la respuesta de la API de los datos de un usuario no viene el email o éste no tiene el formato adecuado, la Tienda no captura dicha información. 
> Actualmente la Tienda no tiene acceso a la documentos cedibles, ya que los Pedidos de Venta que “inyecta” la Tienda en SAP, no están estructurados para recepcionar este tipo de documentos por parte de los proveedores.
>
> Se requieren ciertas funcionalidades en SAP que aparentemente tomará tiempo implementar, como la habilitación de nuevos canales. Esta dependencia es insalvable, y por tanto, crítica para el éxito del proyecto Tienda. Se deben buscar los recursos necesarios para que no sea un “bloqueante” para la Tienda
{.is-danger}


