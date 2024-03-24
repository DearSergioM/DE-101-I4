# PRE SETUP

## Prerequisites

* [Docker][install_docker]

## Steps

### Step 1 - Composer

* Run the docker-compose.yml that start docker containers that has Airflow Celery Components

  ```sh
  docker-compose up -d
  ```

### Step 2 -  Airflow Web UI

Once docker-compose runs all the Airflow Celery component containers

* Open a web browser and open following URL to access to Airflow Web UI:
  * <http://localhost:8080>

    ![img](img/airflow-2.png)

* Login
  * username: `airflow`
  * password: `airflow`

    ![img](img/airflow-3.png)

* Example DAG's

  ![img](img/airflow-4.png)

## Links

* [Install Docker][install_docker]

[install_docker]: https://docs.docker.com/engine/install/
