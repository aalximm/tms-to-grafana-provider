# Qase TMS, InfluxDB and Grafana - delicious

## About

### This project allow you to:
 - Pull test-runs data from Qase TMS and save it into InfluxDB bucket
 - Track test-runs runtime on Grafana dashboards

Project have [submodule](https://github.com/aalximm/tms-metric-collector) - that is the script, which will interact with Qase API

## Installation and usage

### You need to run some comands:

    git clone --recursive <project url>

Now you can change .env file as you want, add Qase API token and change credentials

	docker-compose up --build -d --remove-orphans

After docker compose up, script from submodule will start and pull data from qase. This data will be saved in InfluxDB. 

*Saved points will have measurment names "test run" and "test case"*

Grafana will be initializating with default datasource and usefull dashboard

## Hosts and Ports

 - **Grafana**: http://localhost:3000
 - **InfluxDB**: http://localhost:8086

## Default credentials:
*\*you can check these values in .env file\**
 - **Grafana**: admin / 12345678
 - **InfluxDB**: admin / 12345678


