---
title: authentication
description: 
published: true
date: 2024-10-31T17:28:20.208Z
tags: 
editor: markdown
dateCreated: 2024-10-28T20:14:24.144Z
---

# API authentication

## Resume

> Dev HOST: <kbd>testaplicacionesweb.cenabast.cl:7001</kbd> 
{.is-info}


## Request

```jsx
POST '{{HOST}}/interoperabilidad/tienda/api/v1/auth' \
--data '{
  "user": "tienda",
  "password": "tienda#2024"
}'
```

## Response

```jsx
{
    "code": 200,
    "isSuccessStatusCode": true,
    "content": "eyJhbGciOiJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGRzaWctbW9yZSNobWFjLXNoYTI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9zaWQiOiIxOSIsImh0dHA6Ly9zY2hlbWFzLnhtbHNvYXAub3JnL3dzLzIwMDkvMDkvaWRlbnRpdHkvY2xhaW1zL2FjdG9yIjoiVXNlciIsImV4cCI6MTcwOTY1ODYzMiwiaXNzIjoiVElFTkRBLVRFU1QtVEkiLCJhdWQiOiJodHRwczovL3Rlc3RhcGxpY2FjaW9uZXN3ZWIuY2VuYWJhc3QuY2w6NzAwMSJ9._yFI6FS65pgale8FRQTDgLiGXgkZpGcZvHXtxA5ThM4"
}
```