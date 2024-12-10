---
title: Tienda Web Applications
description: 
published: true
date: 2024-12-10T15:40:05.149Z
tags: 
editor: markdown
dateCreated: 2024-10-28T20:13:24.094Z
---

# Applications

> All applications must be deployed using Docker container.
> Ideally, we need to build the image locally.
{.is-info}

- [Keycloak *Single Sign On*](/infrastructure/applications/keycloak)
- [Postgresql](/infrastructure/applications/postgresql)
- [Mageai *Data Pipeline*](/infrastructure/applications/mageai)
- [Sidekiq *Queue service*](/infrastructure/applications/sidekiq)
- [Spree Commerce *Ecommerce service*](/infrastructure/applications/spree)
- [SAP *SAP info related to Tienda Web*](/infrastructure/applications/SAP)
{.links-list}



# Docker

> Al applications must be deploy as docker images using the followng [Docker-Compose file](https://github.com/Departamento-TI/cenabast-tienda/blob/spree-4-7-development-with-frontend/docker-compose.yml)
{.is-success}

## Docker PostgreSQL

> Both Keycloak and Spree Commerce should use the same postgres service.
{.is-success}


Docker Repo:

- https://github.com/docker-library/postgres
{.links-list}

## Docker Keycloak

Docker info:

- https://www.keycloak.org/server/containers
{.links-list}

## Docker Spree Commerce

> This is our custom Spree Project. \
> Please deploy branch `spree-4-7-development-with-frontend`
{.is-info}

- https://github.com/cenabast-ti/cenabast-tienda/
{.links-list}
