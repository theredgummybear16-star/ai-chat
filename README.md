# Ollama WebUI Project

This project allows you to run a local AI with a web interface using [Ollama](https://ollama.ai) and [Open WebUI](https://github.com/open-webui/open-webui).

## Prerequisites

- [Docker Desktop](https://www.docker.com/products/docker-desktop/) or [Docker Engine](https://docs.docker.com/engine/install/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

1.  **Clone the repository:**
    ```bash
    git clone <your-repo-url>
    cd github-ai
    ```

2.  **Start the application:**
    ```bash
    docker-compose up -d
    ```

3.  **Access the WebUI:**
    Open your browser and navigate to `http://localhost:3000`.

4.  **Wait for Ollama to initialize:**
    The WebUI will connect to the Ollama service. You'll need to pull a model like `llama3` or `mistral` through the WebUI's interface.

## GitHub Actions

This repository includes a GitHub Action workflow (`.github/workflows/ci.yml`) that automatically validates your `docker-compose.yml` file on every push or pull request to the `main` branch.

## Troubleshooting

- If the WebUI can't connect to Ollama, ensure both containers are running with `docker compose ps`.
- Check logs for any issues: `docker compose logs -f`.
