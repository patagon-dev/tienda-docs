---
title: dev-server
description: 
published: true
date: 2024-12-03T12:21:02.671Z
tags: 
editor: markdown
dateCreated: 2024-10-28T20:12:48.909Z
---

# Dev Server

## Resume

> The current Dev Server is a Ubuntu Server.\
> External IP is `190.215.197.206`
{.is-info}

> The opened port are `80` and `443`.
{.is-warning}

### Tamaño Servidor Dev

> vCPU: 8
> RAM: 32 GB
> Storage: 100GB

## SSH 

> SSH access **requires** VPN access.
> 
> SSH Port: `22`\
> Internal IP Address: `10.8.0.44`
> {.is-warning}
{.is-warning}






## VPN

> Please request a VPN access to Cenabast project manager.
{.is-info}


```jsx
sudo openfortivpn 190.215.197.202:10443 -u "username" -p "XXXXXXX"
```

## Ports

> **Ports opening request:**
> 
> The following ports should be allowed: `22`, `80`, `443`, `587`.
{.is-danger}


## Docker

> Container path is at `/root/containers/cenabast.gob.cl`
{.is-info}

### Useful commands

> **Video intro**:
> 
> Quick video intro => https://youtu.be/lJkh3XUYrRE
{.is-info}


> **Login to Dev Server:**
>
> Login: `ssh username@10.8.0.44`
> Change to root user: `sudo su`
{.is-info}


> **Update code:**
> Go to working directory: `cd /root/containers/cenabast.gob.cl`\
> Pull main branch: `git pull origin main`
{.is-info}


> **Rebuild**:
> Rebuild container: `docker-compose build --no-cache`\
> Store Bunlde install: `docker compose run web bundle install`\
> Store DB migrations: `docker compose run web rake db:migrate`\
> Relauch new containers: `docker compose up -d --build --force-recreate --no-deps`
{.is-info}


> Stop containers: `docker compose down`\
> Start containers: `docker compose up -d`\
> Check Logs containers: `docker compose logs -f`\
> Log into container: `docker exec -it -u root e1cc /bin/bash` where 'e1cc' is the container ID.
{.is-success}

##### Running containers:

![runningcontainers](/images/img/2023-12-20_13-09.png)

### Docker Compose

> Check the [docker-compose.yml](https://github.com/Departamento-TI/cenabast-tienda/blob/develop/docker-compose.yml).
{.is-danger}