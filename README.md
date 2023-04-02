# spiritlab

Docker compose based local data engineering dev environment for playing with stuff

Currently includes:

* Jupyter with pyspark
* Kafka
* Airflow

Ports used on host:
* 9080: jupyterlab
* 9091: kafka broker

ToDo:
[ ] Connect jupyterlab to kafka via docker network


```bash
mkdir -p ./dags ./logs ./plugins
echo -e "AIRFLOW_UID=$(id -u)" > .env
```

Initialize airflow
```
docker compose up airflow-init
```

Finally, run everything
```
docker compose up
```

Airflow on: [localhost:8080](localhost:8080)
Jupyter Notebook on: [localhost:8000](localhost:8000)
