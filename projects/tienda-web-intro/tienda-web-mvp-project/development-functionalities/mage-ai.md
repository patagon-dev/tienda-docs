---
title: Mage AI
description: 
published: true
date: 2024-11-13T21:24:02.591Z
tags: 
editor: markdown
dateCreated: 2024-10-28T20:13:45.425Z
---

# Overview

> This doc explains how the MageAI is used in the Cenabast proyect
{.is-info}


See also:
* [MageAI Documentation](/infrastructure/applications/mageai)
* [Product Sincronizacion](/projects/tienda-web-intro/tienda-web-mvp-project/development-functionalities/product-sync)
* [API tienda V2](/apis/home/tienda-web)
{.links-list}

> MageAI is be used as a Middleman in charge of recolecting information from Cenabast APIs and ingesting them into the Spree aplication via its Rest API.
{.is-warning}


## Implementation

> MageAI is currently used for the product sincronization service
> 
{.is-info}

A data pipeline can be created for each pipeline we want to create.

> Data pipeline creation Guidelines:
> 
> * The pipeline is scheduled to run every X hours
> * The pipeline requests a token, request information from 1-N APIs, and merge that information
> * The pipeline injects the information to the Spree Aplication via an API request
> * Spree native API must be used. Prefering to decorate the less amount possible.
{.is-info}


### Deployment

> MageAI service is present in the docker-compose.yml file.
> By default it will run when starting the services.
> 
> On dvelopment environments, it can be accessed via http://localhost:6789/.
{.is-success}


### Important environment variables

```ruby
* CENABAST_API_BASE_URL
    * Root URL to use

* CENABAST_API_BASE_PATH
    * Base path that points to the root of the API to use

* CENABAST_API_USER
    * API User to obtain a token from

* CENABAST_API_PASSWORD
    * Password of the API user
```