# Minimal Apache Guacamole Docker Compose Setup

A **minimal, ready-to-run Docker Compose setup for [Apache Guacamole](https://guacamole.apache.org/)**, designed to quickly test and explore browser-based remote access via RDP, SSH, or VNC. This setup uses a PostgreSQL backend and is ideal for learning, homelabs, or testing Guacamole without setting up a full production environment.

---

## Features

- Browser-based remote access (RDP, SSH, VNC)  
- PostgreSQL backend for authentication  
- Fully containerized using Docker Compose  
- Easy to run and tear down for experimentation  

---

## Requirements

- [Docker and Docker Compose](https://docs.docker.com/engine/install/)

---

## Setup

1. Clone the repository:

```bash
git clone https://github.com/code-loading/guacamole-docker-compose.git
cd guacamole-docker-compose
```

2. Start the stack:
```bash
docker compose up -d
```

3. Access the guacamole web interface:
```bash
http://localhost:8080/guacamole
```
Don't forget to add /guacamole

4. Login via default username and password
```bash
guacadmin
```
(It's best to change this ASAP!)

## Volumes / Mounting Points
`initdb`: Initialization scripts for PostgreSQL and Guacamole

(Optional. Currently commented out) `${HOME}/guacamole/postgres-data`: Persistent PostgreSQL database data

## Notes / Recommendations
You can change the host port `8080` if it conflicts with other services

Run the following to tear down the project:
```bash
docker compose down
```
