# keycloak-local-cluster

A playground for keycloak 24.0 cluster running in separate networks to test cache with TCP connection.

This is usefull where UDP Multicast is not a available!

## Requirements

* Docker and docker compose

## keycloak version

24.0

## Tutorial

Run the cluster:

`./start.sh`

Check the configuration:

`./show-config.sh`

Check the cluster:

`./check-cluster.sh`

