# Shadow Traffic

Shadow Traffic is a powerful tool for simulating and testing real-world traffic patterns in various environments, including Azure and PostgreSQL.

## Prerequisites

Before running the Shadow Traffic container, ensure you have:
- Docker installed
- An `.env` file (`st-key.env`) with required environment variables
- Properly configured JSON configuration files in the `gen/` directory
- Access to Azure CLI if using Azure services

## Usage

### Running Shadow Traffic with Different Configurations

#### **Azure: Uber Eats**
Simulate Uber Eats traffic in Azure.
```shell
docker run \
  --env-file st-key.env \
  -v $(pwd)/gen/uber-eats.json:/home/config.json \
  shadowtraffic/shadowtraffic:0.15.5 \
  --config /home/config.json
```

#### **Azure: CDC Events**
Simulate Change Data Capture (CDC) event traffic in Azure.
```shell
docker run \
  --env-file st-key.env \
  -v $(pwd)/gen/cdc-events.json:/home/config.json \
  shadowtraffic/shadowtraffic:0.15.5 \
  --config /home/config.json
```

#### **PostgreSQL: Drivers**
Simulate driver-related traffic in PostgreSQL.
```shell
docker run \
  --env-file st-key.env \
  -v $(pwd)/gen/postgres-drivers.json:/home/config.json \
  shadowtraffic/shadowtraffic:0.15.5 \
  --config /home/config.json
```

## Azure Blob Storage Capacity Check
Ensure you are logged into Azure before running any Azure-related commands.
```shell
az login
```

## Notes
- The JSON configuration files should be structured appropriately for the Shadow Traffic use case.
- The `st-key.env` file must contain valid credentials and configuration values.
- Ensure Docker is running before executing the above commands.

## References
- [Shadow Traffic Docker Hub](https://hub.docker.com/r/shadowtraffic/shadowtraffic)
- [Azure CLI Documentation](https://learn.microsoft.com/en-us/cli/azure/)

---
