# Simplifying Kubernetes Deployments using Kustomize

 I use Kustomize Bases and Overlays to deploy 3 different versions (Baseline, Staging, and Production) of the same sample web application into a provided Kubernetes cluster. 

Kustomize is a tool for customizing Kubernetes configurations, simplifying the rollout and deployment of applications into clusters. It has the following features to manage application configuration files:

- generating resources from other sources
- setting cross-cutting fields for resources
- composing and customizing collections of resources


## Base

`cd kustomize`

`kubectl kustomize base`

`kubectl apply -k base`

`kubectl get all`



## Staging
`cd kustomize/overlays/staging`

`kubectl kustomize .`

`kubectl apply -k .`

`kubectl get all -l env=staging`

## Production

`cd kustomize/overlays/production`

`kubectl kustomize .`

`kubectl apply -k .`

`kubectl get all -l env=prod`
