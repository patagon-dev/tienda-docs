# Design

## Production Infrastructure Design (proposal)

:::warning
👉 This is the desired production infrastructure. The application was build in order to be deployed to a Kubernetes cluster.\
👉 Each service lives in its own container image.\
👉 All static assets (ex.: images) are saved on an external storage service (AWS S3)
:::

![infraestructura](/images/img/k8s-mvp.png)

## Service Diagram

:::info
The following service diagram, shows each service interaction.
:::

![](/images/img/service-diagram.png)
