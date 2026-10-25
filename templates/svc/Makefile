# Standard service Makefile (contract v1).
# Override from the command line: PORT=<alt-port> METRICS=off make up

PORT    ?= <default-port>
METRICS ?= on

export PORT

COMPOSE := docker compose
ifeq ($(METRICS),on)
  COMPOSE += --profile metrics
endif

.PHONY: up down logs status test lint clean

up:
	$(COMPOSE) up -d --wait

down:
	$(COMPOSE) down

logs:
	$(COMPOSE) logs -f

status:
	$(COMPOSE) ps

test: up
	@echo "Add service checks here (for example a query or an HTTP call)."

lint:
	yamllint .
	# Uncomment if the service has a Dockerfile:
	# hadolint Dockerfile
	# Uncomment if the service has shell scripts:
	# shellcheck scripts/*.sh

clean:
	$(COMPOSE) down -v
