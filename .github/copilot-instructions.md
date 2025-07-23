# JS-Notebook Project Instructions

This document provides essential context for AI agents working with this JavaScript Jupyter Notebook project.

## Project Overview

This is a JavaScript-based Jupyter Notebook environment powered by IJavascript kernel. The project uses Docker for consistent notebook execution environments.

## Architecture & Components

- **Jupyter Environment**: Uses `jupyterlab-ijavascript` Docker image for JavaScript kernel support
- **Package Management**: Uses `pnpm` as the package manager
- **Dependencies**: Uses Axios for HTTP requests

## Development Environment Setup

### Docker Setup
The project uses Docker Compose for running the Jupyter environment:
```bash
docker-compose up -d
```

Key configurations:
- JupyterLab runs on port 8888
- No authentication required (token and password disabled)
- Node modules are mounted from local directory
- Working directory set to `/home/node/notebooks`

### Dependencies
Install dependencies using pnpm:
```bash
pnpm install
```

## Project Structure

- `2nd.ipynb`: Main Jupyter notebook containing JavaScript code cells
- `docker-compose.yml`: Docker configuration for JupyterLab environment
- `package.json`: Node.js project configuration and dependencies

## Development Workflow

1. Start the Jupyter environment using Docker Compose
2. Access notebooks at http://localhost:8888
3. JavaScript code can be executed directly in notebook cells
4. Node modules from local installation are available in notebooks

## Dependencies & Integration

- The project uses Node.js modules through the IJavascript kernel
- External npm packages can be used in notebook cells after installing via pnpm
- Axios is available for making HTTP requests

## Conventions

- Use JavaScript (not TypeScript) in notebook cells
- Docker environment provides a clean, isolated execution context
- Node modules should be installed locally and will be mounted into the container
