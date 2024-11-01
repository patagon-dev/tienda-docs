---
title: Platform Definition
description: 
published: true
date: 2024-11-01T00:58:31.860Z
tags: 
editor: markdown
dateCreated: 2024-10-28T20:12:58.479Z
---

# INFORME TÉCNICO

## Resumen

> El siguiente informe puede ser utilizado como insumo para la toma de decisión del proyecto Tienda de Cenabast. 
{.is-info}


## Contexto

> El año 2018 se firmó un acuerdo de colaboración con ChileCompra para la habilitación y puesta en marcha de una Tienda de productos para Cenabast. En esa línea, se sugirió aprovechar la actual plataforma Magento que utiliza ChileCompra para las tiendas de Convenio Marco, para el desarrollo e implementación de una Tienda con medicamentos e insumos médicos para Cenabast. 
>
> Por lo mismo, es relevante conocer la historia del proyecto de Magento en Chilecompra, así como también los “Pros” y “Contras” de dicho proyecto en relación con los requerimientos de negocio de Cenabast. 
> 
> Cabe destacar que el año 2022 se realizó una consulta al mercado para conocer las soluciones disponibles de proveedores a nivel local. 
{.is-success}


# OBJETIVOS DE NEGOCIOS DE CENABAST

Es importante poner en perspectiva los principales requerimientos de la tienda de Cenabast:

> - Plataforma de solicitud de pedidos para instituciones públicas, de productos de distintos proveedores ―multi-vendor, o marketplace B2B― . Se requiere un “backoffice” para que los proveedores puedan gestionar las órdenes de venta. 
> - Ajustar la plataforma tecnológica a los procesos de negocio de Cenabast. Entre otros:
> - Integración con el registro de usuarios de Mercado Público.
> - Integración con Orden de Compra de Mercado Público.
> - Integración con SAP.
> - Múltiples bodegas por proveedor.
> - Checkout con productos de múltiples proveedores.
> - Consolidación de pedidos en el backoffice del proveedor.
> - Restricciones de compra por Organismos Público por Producto.
> - Emisión de Orden de Compra a múltiples proveedores.

El punto (ii), implica que se requiere una plataforma altamente customizable. Sea cual sea la plataforma, ésta será intervenida y personalizada a la medida de los requerimientos de Cenabast con funcionalidades y reglas únicas. Por tanto, la solución escogida debe permitir el acceso al código fuente. 

Indirectamente, el punto (ii) también hace referencia a la necesidad de contar con especialistas locales.  Ya sea licitando el desarrollo, o contratando equipo interno, se requerirá contar con profesionales locales con experiencia en la plataforma escogida.

Adicionalmente, considerando los mecanismos de compra para las instituciones de Gobierno:

> No es posible seleccionar un proveedor directamente, sino que el desarrollo debe ser licitado. 
> 
> Se debe trabajar exclusivamente con proveedores con presencia local. 
{.is-warning}


# MAGENTO

> Dado que la propuesta de colaboración considera la utilización de la plataforma Magento ―o Adobe Commerce―, es necesario explorar en detalle las fortalezas y debilidades de dicha solución. 

**Características**

Magento es una plataforma de ecommerce B2C, líder global con cientos de miles de instalaciones en todo el mundo. Nació en el 2007 y fue la primera solución de código libre con tecnología LAMP.  Fue adoptado por miles de negocios y empresas que deseaban comercializar sus productos de forma rápida y económica. La comunidad entorno a Magento creció exponencialmente por las siguientes ventajas:

> 👉 Es una plataforma muy sencilla de implementar. Una pequeña empresa puede comenzar a vender en un par de días. 
> 
> 👉 Tienes miles de funcionalidades y reglas de negocio ya implementadas. La plataforma intenta resolver todos los tipos de funcionalidades que existen en la industria del ecommerce a nivel global a través de su gigantesco panel de administración.  Esto hace que sea muy sencillo de implementar y adoptar por las empresas, ya que no requieren hacer ningún tipo de desarrollo. 
> 
> 👉 La comunidad es enorme, tanto en el número de empresas que lo están utilizando, como en el número de plugins —o extensiones— disponibles. Todos los medios de pago y proveedores logísticos están accesibles. 
{.is-success}


Por otra parte, cabe mencionar ciertos aspectos que han dificultado su entrada en la industria B2B, en particular en proyectos que requieren realizar cambios a la plataforma:

> 👉 Las 4.1 millones de líneas de código que componen la plataforma, hacen necesario que exista un período de aprendizaje importante para los nuevos desarrolladores. Es una aplicación monolítica enorme, y fue diseñada según los antiguos conceptos de desarrollo (2007). 
> 
> 👉 Se requiere un profundo conocimiento y expertise de la plataforma para customizar. El desarrollo es complejo, y por tanto, el costo del desarrollo es elevado. 
>
> 👉 El nivel de desarrollo del módulo B2B está aún inmaduro. Magento es en esencia una plataforma B2C, que nació como solución para empresas de retail. 
>
> 👉 No tiene lógica de Marketplace multi-proveedor de forma nativa. Se debe adquirir un módulo de tercero para habilitar esta funcionalidad. 
{.is-warning}


**Historia del Proyecto en Chilecompra (2019 - 2023)**

Aprovechando el conocimiento disponible en ChileCompra, viene al caso mencionar algunos puntos relevantes al estado del proyecto:

> 👉 Se habilitaron “conectores” entre Magento y MercadoPúblico. Estos son: “login de usuarios”, “generación de orden de compra”, “sincronización de ofertas”, “sincronización del estado del proveedor”.  
> 👉 Se han implementado más de 15 tiendas distintas de Convenio Marco, y se han invertido más de 40.000 horas de desarrollo. 
> 👉 Se compró un módulo de terceros (Webkul) para habilitar la funcionalidad de Marketplace.
> 👉 Han pasado 5 distintos proveedores de desarrollo.
> 👉 Se cambió la estrategia de desarrollo desde “suma alzada” (llave en mano) por desarrollo “por horas” para mejorar la calidad de las entregas.

<mark>No es fácil declarar lo malo que ha resultado un proyecto, sobre todo considerando que se ha participado en él desde el inicio. A juicio de este consultor, éstas han sido las principales equivocaciones respecto del proyecto de implementación de Magento en Chilecompra</mark>:

> 👉 Mala elección del plugin de Marketplace. La extensión del proveedor Webkul sustenta el 80% de la tienda de Chilecompra, y sobre ella se han implementado la gran mayoría de las modificaciones de negocio. Es decir, todo el desarrollo implementado por Chilecompra ha sido realizado o extendido sobre la base de un código de tercero, y no sobre el código nativo de Magento. Este plugin ya no puede ser reemplazado, ya que es el pilar que sustenta las más de 40.000 horas de desarrollo invertidas.
> 
> 👉 Partners de baja calidad. Si bien todos los partners tenían certificaciones de Magento, algunos de ellos dejaron código de muy baja calidad.
> 
> 👉 No hacer “code-reviews” a las entregadas del proveedor. Nunca existió una contraparte técnica para validar las entregas de los proveedores. En muchos proyectos existe un “tech-lead” que revisa el diseño de las soluciones que se están implementando. Para el caso del proyecto de Chilecompra, el proveedor es quien realiza sus propias revisiones.
> 
> 👉 Estrategia de pago a “Suma Alzada”. Los incentivos para el proveedor estaban en entregar la funcionalidad al menor costo posible para maximizar su rentabilidad, por lo que generaban soluciones “parches” para muchos de problemas que se veían enfrentados.  
> 
> 👉 Plazos de entrega por sobre diseño de la solución. La presión por entregar una nueva funcionalidad pesa más que la calidad de ésta, y, por tanto, varias de las implementaciones acarreaban errores. La presión del área de Negocios, o normativas legales, imponen fechas de entrega inamovibles, lo que repercute en la implementación de soluciones acorde a los plazos impuestos.
> 
> 👉 Mezclar código de distintas tiendas. Cuando los procesos de negocio son totalmente independientes, y además, muy distintos entre sí, convendría tener soluciones separadas. Esto no fue el caso, ya que los procesos de negocios particulares de cada tienda se mezclaron entre sí, generando en el código un “árbol” de condiciones y funciones difícil de comprender para un desarrollador.
{.is-danger}


# RIESGOS

Si bien Magento asoma como el primer candidato para la implementación del proyecto Tienda de Cenabast, dada la experiencia y desarrollos ya avanzados por parte de Chilecompra, también tiene varios riesgos que deben ser mitigados. 

Se estima que los siguientes riesgos podrían afectar el proyecto, por lo que habría que buscar la forma de mitigarlos:

> 👉 Dependencia del proveedor o equipo implementador.
> 👉 Incertidumbre respecto del proveedor adjudicado.
> 👉 Estrategia de desarrollo por “hora” en las bases técnicas de Licitación.
> 👉 Selección inadecuada de plataforma base.
{.is-warning}

Respecto del primer riesgo (i), típicamente el equipo implementador adquiere para sí todo el conocimiento del proyecto, generando una dependencia respecto de la mantención y funcionamiento futuro de la plataforma. Para evitar dicha dependencia, se sugiere incorporar en el proyecto una metodología para gestionar el conocimiento, esto es, habilitar procesos y herramientas de tal forma que los equipos estén obligados a documentar de buena forma todo lo relacionado con el proyecto.

Para el caso (ii), la incertidumbre que genera cualquier proceso licitatorio respecto de su resultado 一desierto, adjudicado, etc一, como también de quién será proveedor adjudicado, es también un factor de riesgo relevante. En no pocas ocasiones, los proveedores que se presentan con las más altas credenciales terminan no estando a la altura del desafío. Para abordar este riesgo, se sugiere establecer altos criterios técnicos de participación, así como experiencia comprobable en proyectos de ecommerce B2B. Además, se debe poner especial énfasis, 一 sobre todo en al inicio del proyecto 一, en realizar un control de calidad a las entregas del proveedor a través de un “code-review” realizado por una contraparte técnica.

En relación con la estrategia de desarrollo (iii), en el escenario de que las definiciones de negocio no estén claramente definidas y con el máximo detalle 一como suele ser en la mayoría de los casos一, lo recomendable será abordar la estrategia de desarrollo en una modalidad de pago “por hora” en vez de “suma alzada”. Esto permitirá al proveedor enfocarse en la calidad del trabajo, más que en terminar la tarea a como dé lugar. Al mismo tiempo, para evitar el incentivo del proveedor a abultar las horas, se sugiere imponer a los profesionales una herramienta de “reloj-control” para realizar un control efectivo de las horas efectivamente trabajadas.  

Por último, acerca de una inadecuada selección de la plataforma (iv), y que ésta no se ajuste efectivamente a los requerimientos de la institución, se podría terminar desarrollando una construcción interminable, tratando de adaptar la solución a algo distinto de lo que fue diseñado. Este tránsito resulta muchas veces amargo y tortuoso, debido a que las contínuas correcciones y mejoras derivan en que el negocio se termina adaptando a plataforma, en vez de adaptar la plataforma a los procesos de negocio. Para mitigar este riesgo, es muy importante darse el tiempo necesario para evaluar las distintas soluciones, y no seleccionar cualquier plataforma a la ligera.

# ―OTRAS― PLATAFORMAS DE ECOMMERCE

Como parte del plan de mitigación, vale la pena considerar ㅡy evaluarㅡ, algunas soluciones alternativas que posiblemente se ajustan de mejor forma a los requerimientos de negocio de la institución.  

### **Soluciones Alternativas** 

Una mirada “macro” apunta a diferenciar 2 grupos de plataformas a considerar:
Soluciones empresariales (de código cerrado)
Soluciones de código libre (abierto)

Las diferencias entre ambas tipos de soluciones se pueden ver en el siguiente cuadro:

| **Detalle**   |                                                  **Soluciones empresariales**                                                  |                                                                       **Soluciones de código libre**                                                                       |
|---------------|:------------------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| Soluciones    |                                          SAP Commerce, Oracle Commerce, IBM WebSphere                                          |                                                            Magento, React Commerce, Spree Commerce, Oro Commerce                                                           |
| Código Fuente |                                                             Cerrado                                                            |                                                                                   Abierto                                                                                  |
| Comunidad     |                                         Pocos Proveedores, sólo Partners Certificados.                                         |                                                                     Muchos Proveedores y profesionales.                                                                    |
| Ventajas      | - Garantía y respaldo de la marca. - Proveedores certificados.                                                                 | - Independencia del implementador. - Costos de desarrollo competitivos.- Desarrollo interno o externo. - Flexible a los cambios de alcance. - Sin costo por Licenciamiento |
| Desventajas   | - Dependencia del implementador.  - Altos costos de desarrollo. - Mayores plazos de implementación. - Costo por Licenciamiento | - Sin garantía o respaldo.                                                                                                                                                 |

En el anexo está el detalle de las distintas plataformas existentes en el mercado. 

**Comparativa de soluciones**

Para el caso de Cenabast, la evaluación de SAP Commerce es necesaria, considerando que la institución ya trabaja con dicha solución como ERP. Ahora bien, la información pública de dicha plataforma es escasa, y, por tanto, no se incluyó en el análisis comparativo de las soluciones de código libre. Luego, se deberá buscar la forma de ver cómo evaluar esta plataforma. 
Respecto de las soluciones de código abierto, existen varios atributos comparables entre sí. Utilizaremos los siguientes atributos para ilustrar de mejor forma las diferencias: 

**Altamente Customizable**

> Implica que sea cual sea la plataforma, ésta será intervenida y personalizada a la medida de los requerimientos de Cenabast, con reglas que son únicas. Por tanto, la solución escogida debe permitir el acceso al código fuente, y, sobre todo, tener un bajo número de líneas de código:
{.is-info}

![2023-11-08_10-00.png](/images/images/2023-11-08_10-00.png)

**Costo de Desarrollo (Eficiencia)** 

> Debido a la gran cantidad de funcionalidades y mejoras que deben realizarse, es necesario que la solución tenga una baja curva de aprendizaje, de tal forma que los nuevos desarrolladores puedan comenzar a producir lo antes posible. Debe ser eficiente, en términos de ser rápido y fácil de implementar, además de no repetir código en distintas secciones.  
{.is-info}


**Especialistas Locales**

> Ya sea para contratar personal directamente o a través de terceros, se requiere contar con profesionales locales y una comunidad de desarrollo accesible. 
{.is-info}


**Multi-Vendor engine**

> La plataforma tiene de forma nativa la característica de Marketplace B2B nativo. 
> 
{.is-info}

El resultado de la comparación de los atributos seleccionados es la siguiente:

![2023-11-08_10-02.png](/images/images/2023-11-08_10-02.png)

**Notas a la comparación:** 

> 👉 La solución multi-vendor de Magento sólo existe en forma de plugin.  
> 
> 👉 No se consideró como atributo de valor el número de funcionalidades. Muchas soluciones de ecommerce (como Magento) tratan de resolver una gran cantidad de funcionalidades, para que éstas puedan ser administrables desde el panel del usuario sin necesidad de tener que desarrollar. De esta forma, se transforman en gigantescas soluciones para abarcar todos los escenarios que requieren las empresas tradicionales de hoy. Si las funcionalidades que requiere Cenabast se encontraran dentro de los estándares de ecommerce, entonces sí tendría lógica escoger una solución que incluya una gran cantidad de funcionalidades, sin embargo, los requerimientos de Cenabast son especiales y únicos, y, por tanto deben ser desarrolladas. El gran número de funcionalidades de Magento y Oro Commerce, queda reflejado en el número de líneas de código de cada uno. 
> 
> 👉 Para el caso de los especialistas locales, se marcó como “️⚠️” aquellos escenarios en que hay desarrolladores para el lenguaje (Python o Ruby on Rails) pero que no tiene experiencia con la aplicación. Sin embargo, a diferencia de Magento, al ser plataformas con pocas líneas de código, no es necesario tener experiencia previa con la plataforma. 

# PROPUESTA O SUGERENCIA

Si bien desde el inicio del levantamiento del proyecto se hizo hincapié en que la elección de la plataforma ya estaba confirmada, sería muy poco profesional por parte de este consultor, no levantar los riesgos que supone dicha decisión. A todas luces, utilizar Magento para el caso de Negocio de Cenabast es una elección riesgosa ya que, en comparación con otras soluciones:

> 👉 Agrega mayor complejidad al desarrollo proyecto.
> 👉 Dificulta la búsqueda de profesionales y proveedores especializados.
> 👉 Aumentan los plazos de implementación.
> 👉 No tienen la funcionalidad de Marketplace B2B nativo, por lo que debe desarrollarse dicha funcionalidad, o comprar una extensión de terceros. 
{.is-success}


Dicho de otra forma, Magento es una excelente plataforma, pero se ajusta de mejor manera a casos de Negocio de retail (B2C). Para caso de negocio B2B, en que se requiere alta customización, lo recomendable será utilizar una plataforma más liviana, que permita un desarrollo y customización a la medida.

**Sí o sí Magento**

> Si definitivamente no hay más opciones que utilizar Magento como plataforma, se debe tener en cuenta que dicha decisión significa:

> 👉 Mayores costos de desarrollo que otras soluciones.
>
> 👉 Mayores tiempos de implementación de nuevas funcionalidades.
>
> 👉 Mayor complejidad para la implementación de los requerimientos de Negocio.
>
> 👉 Para tener en consideración en caso de seguir este camino:
> 
> 👉 **Aislar la plataforma al máximo**, para que en el futuro pueda ser reemplazada. Esto implica que la plataforma no debe usarse como fuente de datos de ningún tipo (clientes, productos, etc).
> 
> 👉 Evaluar muy bien los plugins de terceros que se van a instalar. A medida que avanza el desarrollo de los nuevos requerimientos, cada vez es más complejo reemplazar los pilares (plugins) que sustentan dicha funcionalidad.
>
> 👉 Seleccionar un proveedor de desarrollo altamente calificado.
> 
> 👉 Tener un “code-reviewer” como contraparte a las entregas del proveedor.
>
> 👉 No sobreponer los requerimientos de Negocio por sobre el diseño de la solución. Cuando los desarrollos se hacen “a la rápida”, en el mediano plazo terminan impactando gruesamente. 
{.is-warning}


**Alternativas**

En caso de abrir la discusión para evaluar otras alternativas, se sugiere:
Destinar una parte del presupuesto en la implementación y desarrollo de pruebas de concepto o “pilotos” para comparar objetivamente los resultados entre distintas soluciones. En caso de hacer “competir” 2 o más plataformas, se establecen los parámetros de medición, y al final del piloto se “botan” los peores proyectos, y se adjudica el mejor.

# ANEXO 1 - MERCADO DE SOLUCIONES (PLATAFORMAS)
> **Consultor**
> Nicolás Mella es Ingeniero Civil industrial PUC con casi 20 años de experiencia en el área de las Tecnologías de la información. En 2001 cofundó Kepler, empresa líder en Recuperación de Datos. El 2010 emprendió en el mundo del ecommerce con modelos de dropshipping y marketplaces B2B y B2C. A partir del 2016, es consultor independiente para distintas empresas. 

**Cuadrante de Gartner 2023**
El estudio de Gartner muestra los principales proveedores de soluciones para “Comercio Digital”:

![2023-11-08_18-19.png](/images/images/2023-11-08_18-19.png)

**Local (Chile)**

A nivel local, la preferencia de las grandes cadenas de retail en Chile han optado por plataformas B2C:

> 👉 Oracle Commerce o ATG, que es utilizado por Falabella, Sodimac, VTR entre otras empresas.
> 👉 VTEX, en empresas como Jumbo.cl, El Mundo del Vino, Unimarc, Rosen, Colloky, Corona.
> 👉 SalesForce Commerce Cloud: Lapolar.cl, hites.com, cruzverde.cl, cic.cl
> 👉 Magento: Empresas de retail más pequeñas: marmot.cl, casaroyal.cl, northface.cl, casaideas.cl.
> 👉 Oro Commerce: Prisa.cl, destacado proveedor B2B. 

Adicionalmente, el año 2022 Cenabast realizó una consulta al mercado respecto de los costos de mantención y operación de una nueva tienda. Dicha consulta arrojó las siguientes estimaciones de los proveedores para la implementación y mantención anual:

|     Proveedor     |     Solución    | Implementación (UF) | Mantención Anual (UF) |
|:-----------------:|:---------------:|---------------------|:---------------------:|
| TicBlue           | Solución Propia |         2800        |          8666         |
| Sistemas Expertos | Solución Propia |         7525        |          4891         |
| SAP               |   SAP Commerce  |        23375        |          9657         |
| Prologística      | Solución Propia |         4340        |          3600         |
| Liferay           |     Liferay     |         7316        |          2125         |
| Linets            |  Adobe/Magento  |         7140        |          5900         |
| Summa             |  Adobe/Magento  |         6729        |          5900         |
| TekPro            |  Adobe/Magento  |         3550        |          5900         |

**Internacional**

A nivel internacional, muchos de los principales ecommerce del mundo tienen soluciones propias (customizadas a la media). Sitios como Amazon, Otto.de, Alibaba, MercadoLibre, Ebay, Wallmart, Apple, utilizan soluciones propias. 

Dentro de las soluciones para empresas B2B a nivel internacional, destacan las soluciones de SAP, Intershop, Sana Commerce y Oracle.

**Plataformas de ecommerce descartadas**

Visto que existen múltiples soluciones disponibles en el mercado, y, considerando las necesidades de negocio de la institución, se pueden descartar de la evaluación las siguientes plataformas: 

| Plataforma            |                           Motivo                           |
|-----------------------|:----------------------------------------------------------:|
| Elasticpath Commerce  | Solución Cloud que no permite el acceso al código fuente.  |
| InterShop             | Solución Cloud que no permite el acceso al código fuente.  |
| VTEX                  | Solución Cloud que no permite el acceso al código fuente.  |
| Solución Propia       | Riesgo de producto poco maduro.                            |
| Shopify               | Solución Cloud que no permite el acceso al código fuente.  |
| SalesForce Commerce   | Solución Cloud que no permite el acceso al código fuente.  |
| BigCommerce           | Solución Cloud que no permite el acceso al código fuente.  |


## **Soluciones de eCommerce evaluadas**


La siguiente sección muestra un breve análisis respecto de 6 soluciones de ecommerce “compatibles con los requerimientos de negocio para Cenabast”,  con sus ventajas y desventajas. 

### **Reaction Commerce **

Reaction Commerce es una solución “Headless commerce”, es decir, no tiene frontend ni backend, sino que es básicamente un motor o API que permite administrar todas las funcionalidades del ecommerce. Esto permite conectarse a múltiples sistemas y no está atado a una solución de frontend y backend.  

**Ventajas**:

- Su mayor ventaja es el desarrollo, ya que contiene una lógica apuntada a los desarrolladores, en que no se necesita tener conocimientos especiales en ningún sistema en particular, sino que utiliza un estándar de comunicación “universal”.  

Dado que sólo es el “motor”, permite construir los flujos y reglas a la medida. Posiblemente es la solución que permite el más alto nivel de customización.  
Contiene lógica de Marketplace multi-proveedor de forma nativa. 

**Desventajas**:

- Su mayor desventaja es que no tiene ningún diseño para el frontend y backend. 
- Aún tiene una comunidad de desarrolladores pequeña. 
- Pocos empresas utilizan Reaction Commerce. 

### **Spree Commerce** 

La solución de Spree Commerce fue creada el 2007 y está basada en el lenguaje de programación Ruby on Rails. Es una solución de código abierto y a la fecha tiene aporte de más 840 colaboradores al código (Magento en comparación, tiene 1436 contribuyentes).  Sus principales ventajas son: 

> 👉 Tiene una estructura liviana (188 mil líneas de código, en comparación con las 4.1 millones de líneas de código de Magento), por lo que es de fácil adopción. 
> 
> 👉 El lenguaje de programación Ruby on Rails es popular por su regla DRY —Don’t Repeat Yourself—, apunta a que la información del código debe ser clara y única para el resto del sistema. El propósito es disminuir la repetición de código al máximo, para que sea más sencillo el desarrollo. 
> 
> 👉 No es necesario que los nuevos desarrolladores tengan conocimiento ni experiencia en Spree Commerce. Basta que tengan experiencia en Ruby on Rails, ya que el framework es el mismo. Esto hace que los nuevos desarrolladores puedan comenzar a producir mucho antes que otros lenguajes. 
>
> 👉 La eficiencia del desarrollo es mucho mayor al de otras soluciones, y por tanto el costo del desarrollo es menor. 
>
> 👉 Tiene lógica de Marketplace multi-proveedor de forma nativa. 
{.is-success}



Y sus desventajas: 

> 👉 La comunidad de desarrolladores es mucho menor que PHP.  
> 👉 No hay soporte de la marca. 
> 👉 Empresas en Chile que utilizan Spree Commerce: Macoline.cl, Salcobrand.cl, Preunic.cl, andesgear.cl 
{.is-warning}

### **Shuup** 

Shuup es una solución de código abierto desarrollada en Django y Python. Tiene aproximadamente 392 mil líneas de código y fue lanzada el año 2012.  

**Ventajas** 

El framework Django y el lenguaje Python están dentro de los lenguajes más populares (es el primer lenguaje que se enseña en la escuela de informática de las principales universidades del mundo) 

Tiene lógica de Marketplace multi-Proveedor de forma nativa, aunque dicho módulo requiere un pago anual por licenciamiento. 

**Desventajas** 

- La baja popularidad de Shuup hacen que aún su comunidad sea pequeña. 
- La solución provee un módulo de Marketplace que requiere licenciamiento. 
- Pocas empresas utilizan Shuup actualmente. 

### **OroCommerce** 

OroCommerce es el único ecommerce opensource que nació el año 2012 con foco en el B2B y marketplace. En Chile, Prisa.cl lo implementó el 2022. La solución utiliza código PHP y fue fundada por parte del equipo original que desarrolló Magento, por lo que tiene varias similitudes con éste. Ventajas:

Solución B2B nativo. 

Incluye lógica de compras similar a las soluciones de “procurement”, esto es, lógica de Centros de Costos, restricciones de compra, distintos flujos de compras, etc. 
Incorpora de forma nativa la lógica de Marketplace multi-vendor. 
**Desventajas** 
Tiene 1.3 millones de líneas de código, por lo que se requiere desarrolladores con experiencia y conocimiento en la plataforma antes de poder comenzar a programar. 
El diseño de la solución está pensado en resolver todo tipo de funcionalidades que hoy utilizan las empresas B2B, por tanto, incluye muchas reglas que no se necesitan en el caso de Cenabast.  
**Saleor**

Saleor es una plataforma enfocada en ser Headless API. Es una solución muy reciente (lanzada el 2012) y está basada en el popular lenguaje Python, lo que inmediatamente la convierte en un framework de desarrollo rápido e intuitivo. Es la solución más pequeña en términos de líneas de código, ya que sólo contiene 45 mil líneas. Ventajas:

Solución basada en Python. No requiere experiencia de los desarrolladores, por lo que es muy fácil y rápido desarrollar sobre él. 

Está pensado para construir sobre él, es decir, al ser un “headless API”, permite que cada equipo de desarrolladores utilice el lenguaje de programación que mejor le acomode, y con él se consuma los servicios de la API. 

Alta comunidad de desarrolladores locales. 

**Desventajas**:

No hay casos de éxito en Chile. 
Su diseño y arquitectura es de última generación, por tanto, podría haber aún etapas que madurar. 
No hay soporte de la Marca. 

**Adobe Magento - Cotización (2018)**

En el proceso de Gran Compra ID 43235, realizado el año 2018, Adobe entregó la siguiente tabla de precios según el tramo de venta anual:


### **Comentarios Chilecompra**

> Como parte del análisis, se levantó la opinión de algunas personas respecto del caso de Magento en Chilecompra. 
> 
> Jovanna Mammani (Jefe de Proyecto)
{.is-warning}


> “Estamos en una etapa de madurez del proyecto. Recién ahora, después de varios años, hemos comenzado a ver oportunidades de mejora. Inicialmente había poco conocimiento de la plataforma, y todo era más difícil. Y el partner es sumamente bastante relevante… En el día a día estamos contínuamente en el incendio…sacando tiendas.
> 
> Habiendo logrado migrar todas las tiendas… estamos 100% con Magento como estrategia. Podemos hacer como una retrospectiva de cómo hemos hecho las cosas. Nos hemos reunido con Adobe para ver las oportunidades de negocio… La tendencia es tratar de no customizar tanto el core. Tratar de usar lo más nativo posible. Si hay que hacer una modificación, tratar de hacerlo modular…Hoy día estamos con mucha refactorización. El desafío para el 2024 es modularizar. 
> 
> Recomendación para Cenabast: Tener un buen partner. Hacer a Adobe parte de la definición para  poder implementar lo que quiere el Negocio (Nunca íbamos revisando que cosas estaba sacando Magento). Nosotros seguimos con lo que teníamos. El resultado es.. mantenciones más complejas…. Desarrollos más largos… dependencia entre tiendas…pruebas cross costosas…
> 
> Si parten de cero, parte de la estrategia que incorporen a Adobe. 
> 
> El Negocio es cambiante (respecto de los requerimientos)… pero no se ajusta con nuestro plazo de desarrollo. Tenemos que ver como ir a la par con el negocio, para no tener que decir al Negocio que sea creativo. Tenemos que negociar con los plazos. Ya estamos con el equipo más maduro…conocen las reglas de negocio. Ya ven las oportunidades de Negocio.  Lo ideal es poder avanzar con el misma velocidad del negocio. “
