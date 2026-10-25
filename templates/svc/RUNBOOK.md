# <service-name> runbook

## Start and stop

    make up
    make down

## Check health

    make status

Expected: the container is `running` and its health check is `healthy`.

## Logs

    make logs

## Common problems

| Symptom | Likely cause | Fix |
| --- | --- | --- |
| Port already in use | Another process uses <default-port> | `PORT=<alt-port> make up` |
| Container restarts in a loop | Missing or wrong value in `.env` | Compare `.env` with `.env.example` |
| Metrics missing | Exporter disabled | `METRICS=on make up` |

## Reset to a clean state

    make clean

Warning: this deletes the service's volumes and therefore its data.