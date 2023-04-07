# Monitoring Stack with Docker Compose

> *POINTS TO NOTE*
> This README was conceived by ChatGPT (GPT-4).

This repository provides an easy way to deploy a monitoring stack using Prometheus, Alertmanager, Pushgateway, Node Exporter, Blackbox Exporter, and Grafana with Docker Compose. This allows you to efficiently and quickly set up monitoring for your systems and applications.

## Components

The monitoring stack consists of the following components:

- **Prometheus** : The main monitoring system for metrics collection and alert detection.
- **Alertmanager** : Manages alert notifications and configures destinations and methods for notifications.
- **Pushgateway** : Temporarily stores metrics from short-lived jobs, making them available for collection by Prometheus.
- **Node Exporter** : An exporter that collects host system metrics.
- **Blackbox Exporter** : An exporter that measures the availability and response time of external services.
- **Grafana** : Provides dashboards and visualizes metrics from Prometheus.

These components are defined within the docker-compose.yaml file and can be easily deployed using Docker Compose.

## Usage

1. Clone this repository.
```shell
$ git clone git@github.com:iedred7584/prometheus-stack.git
$ cd prometheus-stack
```

2. Create a `.env` file and set the necessary environment variables. (You may copy from `.env.sample`.)
Example:
```
PROMETHEUS_WEB_EXTERNAL_URL=https://prometheus.example.com
ALERTMANAGER_WEB_EXTERNAL_URL=https://alertmanager.example.com
```

3. Launch the monitoring stack using Docker Compose.
```shell
$ docker-compose up -d
```

The monitoring stack will now be running, and the components will be working together. Configuration and data for each component are stored in the config and data directories within the repository. You can modify the configuration as needed and restart with Docker Compose.

## Customization

Configuration for each service can be found in the config directory within the repository. Edit the configuration files as needed and use Docker Compose to restart the services for the changes to take effect.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.
