# Services

## Deploying Prometheus, Grafana, and Loki using Docker Compose

To deploy Prometheus, Grafana, and Loki using Docker Compose, follow these steps:

1. Ensure you have Docker and Docker Compose installed on your system.
2. Clone the repository to your local machine.
3. Navigate to the directory containing the `docker-compose.yml` file.
4. Run the following command to start the services:
   ```sh
   docker-compose up -d
   ```
5. To stop the services, run the following command:
   ```sh
   docker-compose down
   ```

## Example Commands

### Starting the Services
```sh
docker-compose up -d
```

### Stopping the Services
```sh
docker-compose down
```

## Official Documentation

- [Prometheus Documentation](https://prometheus.io/docs/introduction/overview/)
- [Grafana Documentation](https://grafana.com/docs/grafana/latest/)
- [Loki Documentation](https://grafana.com/docs/loki/latest/)
