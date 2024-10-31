---
title: Cenabast Products
description: 
published: true
date: 2024-10-31T16:24:42.330Z
tags: 
editor: markdown
dateCreated: 2024-10-31T16:24:42.330Z
---

# Resume

> 💣Product distinction 💣
> 
> Basically, there are two types of products:\
> \
> <kbd>ZGEN</kbd> 👉 **Unbranded** <mark>**Generic**</mark> product component request.\
> <kbd>ZCEN</kbd> 👉 **Branded** product, after a Seller has won an [auction](auction).
{.is-info}


# ZGEN

> ZGEN products
> The Unbranded Generic product <kbd>ZGEN</kbd> is **NOT a real product**, just a product definition. (Similar to "Monitor 20 inches" or "Paracetamolum 500 mg"). 
{.is-success}


Some characteristics are:


- Is **Generic**
- Is **Unbranded**.
- It **does** not have a **Seller owner**. 
- It **does not** have a **price**.
- It **does not** have **stock**.
- It **does not** have a real **image**. (Although it might have a representative image)
- Is **has** an internal **SKU**.
- **One ZGEN product might have multiple related <kbd>ZCEN</kbd> products**. 

> ZGEN is used for forecasting
> 
> <kbd>ZGEN</kbd> products definition is used for [forecasting](forecast) the demand and creating a public [bidding auction](auction).
{.is-warning}


## Real <kbd>ZGEN</kbd> products

**Real** <kbd>ZGEN</kbd> JSON sample 👇
    
```json
{
        "CODIGO_PRODUCTO": "100001143",
        "TIPO_PRODUCTO": "ZGEN",
        "GRUPO_ARTICULO": "1IN",
        "CODIGO_SECTOR": "S1",
        "DESCRIPCION_SECTOR": "Fármacos",
        "DENOMINACION": "PARACETAMOL 500 MG CM/CM REC",
        "CODIGO_ATC": "N02B0N02BE01",
        "DENOMINACION_ESTANDAR": "PARACETAMOL",
        "CODIGO_ONU": "51142001",
        "TABLA_BASE": "2.1",
        "JERARQUIA": "0010000100004",
        "UMP": "",
        "FABRICANTE": "",
        "CODIGO_EAN": "",
        "DESCRIPCIONGRUPOARTICULO": "INTERMEDIACION"
    }
```
</div>
</details>

# ZCEN

> ZCEN products
> On the other hand, <kbd>ZCEN</kbd> products are **real branded** products. (ex. "Lenovo Monitor 20 inches IPS 1920x1080", or "Kitadol Paracetamolum 500 mg"). 
{.is-success}

It's characteristics are:

- It has a **brand**.
- It has a **real image**.
- It has a fixed **price**. (Set after the auction)
- It **belongs** to a **Seller**.
- It has a [contract](contract).
- It is related to a single <kbd>ZGEN</kbd> product. 
- Multipe <kbd>ZCEN</kbd> products **can belong** to the same <kbd>ZGEN</kbd> product.


### Real <kbd>ZCEN</kbd> products

**Real** <kbd>ZCEN</kbd> product

   - name: TAPSIN SIN CAFEINA 500 MG CAJ 1000 CM
   - sku: 500000485
   - Seller SKU: 0092121000
   - ean: 7800004508372
   - image:

   ![Kitadol](/images/img/Kitadol_500MG_24C.jpg)
    

  - name: ACAMOL 500 MG CAJ 1000 CM
   - SKU: 500003917
   - Seller SKU: 0079802770
   - ean: 
   - image:

   ![acamol](/images/img/acamol.jpg)

   - name: PARACETAMOL 500 MG CAJ 16 CM
   - SKU: 500005197
   - Seller SKU: 0077596940
   - ean: 7800007124326
   - image:

 ![acamol](/images/img/2024-01-09_15-20.png)

