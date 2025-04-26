# Ollama Docker Setup

This repository contains a Docker Compose configuration for running Ollama, an open-source large language model server.

## Prerequisites

- Docker
- Docker Compose

## Quick Start

1. Start the Ollama container:
```bash
docker-compose up -d
```

2. Pull a model (example using TinyLlama):
```bash
docker exec -it ollama ollama pull tinyllama
```

3. Run the model:
```bash
docker exec -it ollama ollama run tinyllama
```

## Configuration

The Docker Compose file includes the following configuration:

- Uses the latest Ollama image
- Exposes port 11434 for API access
- Persists data using a named volume `ollama_data`
- Container automatically restarts unless explicitly stopped

## Available Models

You can pull and run various models. Some popular options include:

- tinyllama
- llama2
- mistral
- codellama
- neural-chat

To see all available models, visit the [Ollama Model Library](https://ollama.ai/library).

## Ports

- `11434`: Main API port for Ollama

## Data Persistence

The model data is persisted in a Docker volume named `ollama_data`. This ensures your models and settings are preserved between container restarts.

## Stopping the Container

To stop the container:
```bash
docker-compose down
```

To stop and remove the volume (this will delete all downloaded models):
```bash
docker-compose down -v
```

## Additional Resources

- [Ollama Documentation](https://github.com/ollama/ollama)
- [Docker Documentation](https://docs.docker.com/)
- [Docker Compose Documentation](https://docs.docker.com/compose/) 
