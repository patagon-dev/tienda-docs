---
title: applications
description: 
published: true
date: 2024-10-29T14:29:11.578Z
tags: 
editor: markdown
dateCreated: 2024-10-28T20:13:24.094Z
---

# Applications

We need to deploy the following applications in the DEV server:

- PostgreSQL
- Keycloak
- Spree Commerce

> All applications must be deployed using Docker container.
> Ideally, we need to build the image locally.
{.is-info}



# Docker

> Al applications must be deploy as docker images using the followng [Docker-Compose file](https://github.com/Departamento-TI/cenabast-tienda/blob/spree-4-7-development-with-frontend/docker-compose.yml)
{.is-success}

## Docker PostgreSQL

> Both Keycloak and Spree Commerce should use the same postgres service.
{.is-success}


Docker Repo:

https://github.com/docker-library/postgres

## Docker Keycloak

Docker info:

https://www.keycloak.org/server/containers


## Docker Spree Commerce

> This is our custom Spree Project. \
> Please deploy branch `spree-4-7-development-with-frontend`
{.is-info}



https://github.com/Departamento-TI/cenabast-tienda/

