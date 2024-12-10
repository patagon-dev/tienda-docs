---
title: keycloak
description: 
published: true
date: 2024-12-10T15:39:31.467Z
tags: 
editor: markdown
dateCreated: 2024-10-28T20:13:26.006Z
---

# Keycloak

## Admin Access (DEV)

> Keycloak Admin access
> 
> URL: https://login-dev.cenabast.gob.cl/admin/ \
> KEYCLOAK_USER: `admin`\
> KEYCLOAK_PASSWORD: <kbd>owwIZLI#6m65</kbd>
{.is-info}


> **Docker Image:**
> 
> 👉 Check Keycloak [docker-compose.yml](https://github.com/cenabast-ti/cenabast-tienda/blob/main/docker-compose.yml).\
> 👉 Keycloak image is build from file [Dockerfile.keycloak](https://github.com/cenabast-ti/cenabast-tienda/blob/main/Dockerfile.keycloak)    
{.is-info}


### Keycloak user & database

The first time Keycloak is deploy, a `keycloak` user and role must be created in the postgres database.
The password must match the password of `KC_DB_PASSWORD` at the [Dockerfile.keycloak](https://github.com/cenabast-ti/cenabast-tienda/blob/main/Dockerfile.keycloak).

```jsx
CREATE ROLE keycloak;
CREATE USER keycloak WITH PASSWORD 'password';
GRANT ALL PRIVILEGES ON DATABASE keycloak to keycloak;
GRANT ALL PRIVILEGES ON ALL TABLES IN SCHEMA public TO keycloak;
GRANT ALL ON SCHEMA public TO keycloak;
```


### Keycloak Setup

> **Setup**:
> 
> After Keycloak docker is deployed, the following configurations needs to be done in order to integrate with [Clave Unica](../clave_unica.md).\
{.is-info}


### Create Cenabast Realm

Create a new realm:

![createrealm](/images/img/Peek2023-12-19-17-10.gif)


### Create "cenabast-ecommerce" client

> **Import Client Config**
> 
> The initial OIDC client configuration can be imported using the following file [cenabast-ecommerce.json](/images/img/cenabast-ecommerce.json).\
> The client value must match the `KEYCLOAK_CLIENT_ID` in the .ENV file.
{.is-danger}


![import-config](/images/img/2024-03-11_13-38.png)

### Create Clave Unica IdP


> **Clave Unica Discovery Endpoint**:\
> https://accounts.claveunica.gob.cl/openid/.well-known/openid-configuration
{.is-success}


![Add-ClaveUnica_idp](/images/img/Peek2023-12-19-17-16.gif)

### Redirect directly to IdP

> In order to skip Keycloak Login form, we can **redirect** inmediatly to the ClaveUnica Identity Provider.\
> In the browser authentication flow, just configure the alias of your idp (in this case, "**oidc**" is the alias)
{.is-warning}


![Redirect-to-idp](/images/img/Peek2023-12-19-17-18.gif)

### Disable Review Profile

> Disable the "Review Profile" action from the "first broker login" flow.
{.is-info}

![DisableReviewProfile](/images/img/Peek2023-12-19-18-01.gif)

### Disable Profile form


> In order to prevent Keycloak from requesting filling the profile form, we need to disable the "**Update Profile**" required action.
{.is-warning}

![Disable-profile-form](/images/img/Peek2023-12-19-17-19.gif)

### Test Login

> **Testing RUT values**
> Clave Unica test users:
> 
> RUN: 44.444.444-4 	contraseña: **testing**\
> RUN: 55.555.555-5	contraseña: **testing**\
> RUN: 88.888.888-8 	contraseña: **testing**\
> RUN: 99.999.999-9 	contraseña: **testing**
{.is-warning}


> Login URL test:
> https://login-dev.cenabast.gob.cl/realms/cenabast/account/#/
{.is-info}

![testing](/images/img/Peek2023-12-19-18-00.gif)
