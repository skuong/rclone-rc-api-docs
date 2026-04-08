# Rclone RC (Remote Control) API docs made with Scalar

## I. Local Development: API Docs 

### 1. Install dependencies
```bash
pnpm i
```

### 2. Spin up dev server

```bash
pnpm dev
```

## II. Local Development: Rclone RC server (using Docker)

### 1. Get into the `example` directory
```bash
cd example
```

### 2. Run docker services using Docker Compose file
```bash
docker compose -f local-file.docker-compose.yaml --env-file .env.example up
```

or

```bash
docker compose -f minio-s3.docker-compose.yaml --env-file .env.example up
```

or

```bash
docker compose -f webdav.docker-compose.yaml --env-file .env.example up
```

## III. Local Development: Rclone RC server (using Rclone binary)
Note: **Make sure you installed rclone**.

```bash
rclone rcd --rc-allow-origin='http://localhost:5173' --rc-no-auth
```

or
```bash
rclone rcd --rc-user=admin --rc-pass=secret --rc-allow-origin='http://localhost:5173'
```
