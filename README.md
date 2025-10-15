# Perses migration examples

This directory contains examples of how to use Perses and Percli to migrate from Grafana to Perses.

## Prerequisites

- A running Perses instance to run the migration online.
- A Grafana json dashboard file to migrate.

## Usage

1. Install Percli by following the [docs](https://perses.dev/perses/docs/cli/)
2. Login to your Perses instance using Percli:
   ```bash
   percli login http://localhost:8080 -u admin -p password
   ```
3. Run the migration command:
   ```bash
   percli migrate -f <path-to-grafana-json-file> --online -o json > perses-dashboard.json
   ```

   ```bash
   percli migrate -f grafana/acm-vm-status.json --online -o json > perses/perses-acm-vm-status.json
   ```
