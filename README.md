# Enhanced Rclone RC (Remote Control) API docs made with Scalar

Visit live docs here: https://rclone-rc.api.mexhov.com/

<img width="1000" alt="UI for testing API response from rclone rc" src="https://github.com/user-attachments/assets/4b02e089-164b-49b0-ba8f-d4d680db1c67" />

## Motivation
Rclone RC documentation is, with all due respect, not easy to get started with and doesn't have the playground to test.

I made this project so I can test the RC APIs qucikly to learn what it's about and if I want to dig deeper, I can use example in the `examples` folder to test syncing between different servers.

This project also serves as a friendly docs when I need to learn and use Rclone again.

## I. Quick Start

### 1. Clone this repo
```bash
git clone https://github.com/skuong/rclone-rc-api-docs.git
cd rclone-rc-api-docs
```

### 2. Install dependencies
```bash
pnpm i
```

### 3. Spin up dev server

```bash
pnpm dev
```

Visit: http://localhost:5173/

### 4. Playing with Rclone RC APIs
First, let's spin up rclone rc server

Note: **Make sure you installed rclone**.

```bash
rclone rcd --rc-allow-origin='http://localhost:5173' --rc-no-auth
```

or

```bash
rclone rcd --rc-user=rick --rc-pass=astleypass --rc-allow-origin='http://localhost:5173'
```

Now you can play with RC APIs.
<img width="1000" alt="Scalar UI showing sending request to Rclone RC with user and password" src="https://github.com/user-attachments/assets/484bbdde-ab6a-4dd8-9490-16b847b64e4a" />


## II. Explore more with examples (using **Docker**)

**Note**: Make sure you have docker running.

### 1. Get into the `examples` directory
```bash
cd examples
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
