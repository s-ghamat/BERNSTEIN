### T-DOP-603-STG_18
---
Setayesh GHAMAT and Massoud SHAMS

Language: Kubernetes, Yaml

---

**Orchestration** refers to arranging various components of a system so they can be executed seamlessly by a unified infrastructure, much like a conductor organizes an orchestra. **Leonard Bernstein**, renowned for his exceptional compositions such as the soundtrack of West Side Story, was a maestro of his craft.

In this project, we will become the Leonard Bernstein of container orchestration!

We will be using one of the most popular platforms for this task: [**Kubernetes**](https://kubernetes.io/). Kubernetes is an open-source platform designed for managing containerized applications and services at scale and automatically.

Our task is to deploy an **application on a multi-host cluster** using Kubernetes and to utilize **Traefik** as a reverse proxy and load balancer. The application we will work on is a simple **web poll application**.

### Application Components:
1. **Poll**: A Flask Python web application that gathers votes and pushes them into a Redis queue.
2. **Redis Queue**: Holds the votes from the Poll application, waiting to be processed by the Worker.
3. **Worker**: A Java application that consumes votes from the Redis queue and stores them in a PostgreSQL database.
4. **PostgreSQL Database**: Persistently stores the votes processed by the Worker.
5. **Result**: A Node.js web application that retrieves votes from the database and displays the results.

### Environment:

To set up your environment, you will need at least one Kubernetes master and two nodes (workers). While you can run it locally, it is highly recommended to use a “Kubernetes as a Service” platform for ease and scalability.

Recommended platforms include:
- Amazon Elastic Kubernetes Service (EKS)
- Google Kubernetes Engine (GKE)
- Digital Ocean Kubernetes

Setting up a full Kubernetes cluster locally can be complex, and Minikube is not designed for multi-node clusters, which are required for this project.

