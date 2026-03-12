# Docker Compose Development Setup

This repository includes a Docker Compose configuration for running all 8 applications (16 services) in isolated containers with hot-reload support.

## Applications

| App | Client Port | Server Port |
|-----|-------------|-------------|
| Blog Platform | 5173 | 5005 |
| Calendar App | 5174 | 5002 |
| Code Snippets | 5175 | 5003 |
| Music Playlist | 5176 | 5007 |
| News Aggregator | 5177 | 5001 |
| Real Estate | 5178 | 5006 |
| Todo App | 5179 | 5000 |
| Weather App | 5180 | 5004 |

## Quick Start

```bash
# Start all services (with logs)
npm run dev

# Start all services in background
npm run dev:detached

# Rebuild and start
npm run dev:build
```

## Management Commands

```bash
# Stop all services
npm run stop

# View logs
npm run logs

# Restart services
npm run restart

# Clean stop (removes volumes)
npm run clean
```

## Direct Docker Commands

```bash
# Start all services
docker compose up

# Start in background
docker compose up -d

# Stop all services
docker compose down

# View logs
docker compose logs -f

# Restart specific service
docker compose restart blog-platform-server

# Rebuild specific service
docker compose up -d --build blog-platform-server
```

## Features

- **Hot Reload**: Code changes are reflected immediately via mounted volumes
- **MongoDB**: Shared MongoDB instance with persistent storage
- **Isolated Networking**: All services communicate via internal Docker network
- **Environment Variables**: Each service configured via docker-compose.yml

## Troubleshooting

### Port Conflicts
If ports are already in use, modify the port mappings in `docker-compose.yml`:
```yaml
ports:
  - "NEW_PORT:CONTAINER_PORT"
```

### MongoDB Connection Issues
Ensure MongoDB container is running:
```bash
docker compose ps mongodb
```

### Rebuild After Dependency Changes
```bash
docker compose up -d --build
```

## Architecture

```
┌─────────────────────────────────────────────────────────┐
│                    Docker Network                        │
│  ┌─────────────┐    ┌──────────────────────────────┐   │
│  │   MongoDB   │◄───┤  All 8 Server Containers     │   │
│  │   (27017)   │    │  (5000-5007)                 │   │
│  └─────────────┘    └──────────────────────────────┘   │
│                            │                            │
│                            ▼                            │
│                    ┌──────────────┐                     │
│                    │ All 8 Client │                     │
│                    │ Containers   │                     │
│                    │ (5173-5180)  │                     │
│                    └──────────────┘                     │
└─────────────────────────────────────────────────────────┘
```
