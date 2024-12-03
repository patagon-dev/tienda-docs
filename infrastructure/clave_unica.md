---
title: clave_unica
description: 
published: true
date: 2024-12-03T12:30:35.744Z
tags: 
editor: markdown
dateCreated: 2024-10-28T20:12:46.979Z
---

# Clave Única IdP

## Resume

> All Government institutions, are required to use a unique password for all Chilean citizen. This service is provided by [Clave Unica](https://claveunica.cl/).
{.is-info}


> 💡
> 
> Clave Unica is integrated as an Identity Provider (idP) within [Keycloak](applications/keycloak.md)
{.is-success}


## Domain

> The domain `login-dev.cenabast.gob.cl` will be used for authentication with Clave Unica. (**Development**)\
> The domain `login.cenabast.gob.cl` will be used for authentication with Clave Unica. (**production**)
{.is-info}


## Clave Unica Developement Credentials

```ruby
Client ID SANDBOX: 9c52faccf4324a52808f7e4739b58b41
Client Secret SANDBOX: ed711883169b4b82beaf9b7925697529

Client ID QA: 9e0ad6ebedb342c08640ddd94ee4a80c
Client Secret QA: c587e1dce57a4c209bed73d776ea9990

Client ID Producción: 191686e57a3e4b8994f63b7b4e90014c
Client Secret Producción: 1e8c36c5dc22450bbf999fce62a22a72
``` 

### Usuarios de prueba Clave Unica

> Testing RUT values
> Clave Unica test users:
> 
> RUN: 44.444.444-4 contraseña: testing
> RUN: 55.555.555-5 contraseña: testing
> RUN: 88.888.888-8 contraseña: testing
> RUN: 99.999.999-9 contraseña: testing
{.is-warning}



### Technical Documentation

> [Here](https://digital.gob.cl/transformacion-digital/estandares-y-guias/guia-tecnica-para-integracion-de-claveunica/) you can find the latest technical document regarding Clave Unica.
{.is-info}

:::
