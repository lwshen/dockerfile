# MongoDB

This repository contains two Docker Compose configurations for running MongoDB with a web-based UI:
- A basic setup without authentication
- A secure setup with username/password authentication

## Environment Variables

Create a `.env` file in the same directory with the following variables:

```env
MONGO_VERSION=6.0
# Required only for password-protected setup
MONGO_INITDB_ROOT_USERNAME=admin
MONGO_INITDB_ROOT_PASSWORD=your_secure_password
```

## Basic Setup (No Authentication)

To start MongoDB without authentication:

```bash
docker compose -f docker-compose.yml up -d
```

## Secure Setup (With Authentication)

To start MongoDB with password protection:

```bash
docker compose -f docker-compose-with-password.yml up -d
```

## Accessing the Services

- **MongoDB**: Available at `localhost:27017` for default
- **MongoDB UI**: Access through your web browser at `http://localhost:4321` for default

## Stopping the Services

To stop and remove the containers:

```bash
# For basic setup
docker compose -f docker-compose.yml down

# For password-protected setup
docker compose -f docker-compose-with-password.yml down
```
