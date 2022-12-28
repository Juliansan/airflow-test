# Personal Airflow container Test


Personal docker container for testings. 

## Docker commands

Run database migrations and create the first user account
`docker compose up airflow-init`

start all services
`docker compose up`

Clean it up and restart from scratch
`docker-compose down --volumes --remove-orphans`

Get inside docker container
`docker exec -it /bin/bash` 

## Airflow wrapper

This wrapper helps on executing internal commands on airflow
make sure to grant execute to the script airflow.sh

Get information on running container
`./airflow.sh info`

Enter on interactive bash shell container
`./airflow.sh bash`

Enter on interactive python container
`./airflow.sh python`

More CLI commands:
https://airflow.apache.org/docs/apache-airflow/stable/usage-cli.html

## Airflow Requirements

If new packages or modules needs to get installed update variable on docker-compose.yaml file
**_PIP_ADDITIONAL_REQUIREMENTS**
example: `lxml==4.6.3 charset-normalizer==1.4.1`

