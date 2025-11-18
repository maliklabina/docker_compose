# Project Name

This project sets up service using Docker with multiple custom networks for better service isolation and communication.

---

## Table of Contents

- [Overview](#overview)  
- [Prerequisites](#prerequisites)  
- [Setup](#setup)  
- [Networks](#networks)  
- [Running the Services](#running-the-services)  
- [Stopping the Services](#stopping-the-services)  

---

## Overview

This project is based on https://github.com/monisyousuf/youtube-tutorials.git.  
The Docker configuration has been customized to use multiple networks, allowing services to communicate securely and efficiently while isolating them when necessary.

Key features:
- Custom Docker networks for service segregation
- Easy deployment via Docker Compose
- Modular service setup

---

## Prerequisites

Make sure you have the following installed:
- [Docker](https://www.docker.com/)  
- [Docker Compose](https://docs.docker.com/compose/) 

---

## Setup

1. Clone the repository:

```bash
https://github.com/maliklabina/docker_compose.git
cd your-repo
```

2. Build the Docker images:
```bash
docker compose up --build
```

3. docker network ls
```bash
docker network ls
```



## Networks
This setup uses multiple networks to separate and manage service communications:

frontend_network: For web-facing services (e.g., front-end, load balancer)

backend_network: For internal services like databases or APIs

shared_network: Optional network for services that need to communicate across networks

Network configurations can be found in docker-compose.yml under the networks section.




## Running the Services
Start all services:
```bash
docker compose up -d
```

Check running containers:
```bash
docker ps
```



## Stopping the Services
```bash
docker-compose down
```


