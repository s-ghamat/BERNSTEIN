# Kubernetes Survey Platform

Container orchestration project for deploying and monitoring a multi-service survey application on Kubernetes.

The platform uses Kubernetes for service management, Traefik for ingress routing, and cAdvisor for container monitoring.

## Overview

This project demonstrates how to deploy a distributed web application in a Kubernetes environment.

The application is composed of multiple services written with Python, Java, and Node.js. Each service runs in a container and is managed through Kubernetes deployments, services, and networking rules.

## Architecture

```text
Client
  ↓
Traefik Ingress
  ↓
Kubernetes Services
  ↓
Python / Java / Node.js Containers
  ↓
cAdvisor Monitoring
```

## Components

| Component  | Role                                      |
| ---------- | ----------------------------------------- |
| Python     | Backend API                               |
| Java       | Business logic service                    |
| Node.js    | Frontend or additional service layer      |
| Kubernetes | Container orchestration                   |
| Traefik    | Ingress controller and reverse proxy      |
| cAdvisor   | Container monitoring and resource metrics |

## Features

* Multi-service Kubernetes deployment
* Containerized application architecture
* Internal service discovery
* Kubernetes services and deployments
* HTTP routing with Traefik Ingress
* Container monitoring with cAdvisor
* Resource usage tracking
* Distributed infrastructure practice

## Monitoring

Monitoring is provided by cAdvisor.

Tracked metrics include:

* CPU usage
* Memory usage
* Container health
* Runtime metrics
* Resource consumption per service

## Requirements

* Docker
* Kubernetes cluster
* kubectl
* Traefik
* cAdvisor

Check your Kubernetes connection:

```bash
kubectl cluster-info
```

Check available nodes:

```bash
kubectl get nodes
```

## Deployment

Apply the Kubernetes manifests:

```bash
kubectl apply -f k8s/
```

Check deployed resources:

```bash
kubectl get pods
kubectl get services
kubectl get ingress
```

## Traefik

Traefik is used as the ingress controller.

It routes external HTTP traffic to the correct internal Kubernetes service.

Check ingress resources:

```bash
kubectl get ingress
```

## cAdvisor

cAdvisor provides container-level monitoring.

Check the monitoring service:

```bash
kubectl get pods
kubectl get services
```

Port-forward if needed:

```bash
kubectl port-forward service/cadvisor 8080:8080
```

Then open:

```text
http://localhost:8080
```

## Project Structure

```text
.
├── k8s/
├── python/
├── java/
├── node/
├── monitoring/
├── traefik/
└── README.md
```

## Learning Outcomes

This project focuses on practical Kubernetes and infrastructure skills:

* Deploying containerized applications on Kubernetes
* Managing pods, deployments, and services
* Configuring ingress routing with Traefik
* Understanding service discovery and internal networking
* Monitoring containers with cAdvisor
* Working with distributed system concepts

## Academic Context

Project type: Kubernetes and container orchestration
Focus: Distributed systems, ingress routing, monitoring, and service management

## Author

Setayesh Ghamat
