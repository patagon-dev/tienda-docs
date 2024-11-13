---
title: mageai - Data Pipeline
description: 
published: true
date: 2024-11-13T21:31:24.406Z
tags: 
editor: markdown
dateCreated: 2024-10-28T20:13:28.010Z
---

# Mage.ai

> Check the [Mage.ai Implementation](/projects/tienda-web-intro/tienda-web-mvp-project/development-functionalities/mage-ai) for more info.\
> Also check the [Mage.ai Product Syncronization](/projects/tienda-web-intro/tienda-web-mvp-project/development-functionalities/product-sync) for running sync.
{.is-info}


> [Mage.ai](https://github.com/mage-ai/mage-ai) will being used as a data pipeline for data sincronization.
{.is-info}

# Web Access

> Within the VPN network, Mage.ai development is available at [http://10.8.0.44:6789/](http://10.8.0.44:6789/)
{.is-info}


# SSH port forwarding

> Mage.ai does not have a public view.
{.is-warning}


To access the Mage.ai application, a SSH port forwarding must be used between the [DEV server](../dev-server.md) and your local machine.

Once the VPN conection has been made, you can use the following command for tunneling port 6789:

```jsx
ssh nmella@10.8.0.44 -L 6789:10.8.0.44:6789
```

Then, just head up to `http://127.0.0.1:6789/`:

![Mage.ai Dashboard](/images/img/2024-02-23_09-54.png)