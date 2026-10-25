# <service-name>

<One sentence: what this service provides.>

## Quick start

    cp .env.example .env
    make up

## Commands

| Command | What it does |
| --- | --- |
| `make up` | Start the service |
| `make down` | Stop the service |
| `make logs` | Follow the logs |
| `make status` | Show container state and health |
| `make test` | Run the service checks |
| `make lint` | Run the linters |
| `make clean` | Stop and remove containers and volumes |

Options: `PORT=<alt-port> make up` changes the exposed port, `METRICS=on|off` enables or disables the metrics exporter.

## Configuration

See `service.yaml` for ports, dependencies, health check and metrics. Environment variables are listed in `.env.example`.

## Operations

See [RUNBOOK.md](RUNBOOK.md).