# Pre-setup

On this course we will be using the pre-setup as preparation before the session

## Prerequisites

* [Docker][install_docker]
* [VSCode][vscode]
* [DBeaver][dbeaver] \
  **We will not be using the DBeaver during this document, however we will be using it during the session*

## Steps

### Step 1 - Dockerfile

* Within this folder create a file named `Dockerfile`

  ```Dockerfile
  FROM mysql
  ENV MYSQL_ROOT_PASSWORD=mypassword
  ENV MYSQL_DATABASE=mydatabase
  ENV MYSQL_USER=myuser
  ENV MYSQL_PASSWORD=mypassword
  EXPOSE 3306 
  ```

### Step 2 - Docker Image

* Run the following command

  ```sh
  docker build -t clinic .
  ```

* Check existing images with the command

  ```sh
  docker images
  ```

  >An image with the name `clinic` should be listed

### Step 3 - Container

* Run the following command

  ```sh
  docker run --rm -d -p 6603:3306 --name clinic-container clinic
  ```

  This command will create a docker container named as `clinic-container` from `clinic` image.

  * The `-d` option runs the container in detached mode, which allows it to run in the background.
  * The `-p` flag helps to publish Publish container's port(s) to the host, in this case `<host-port>:<container-port>`
  * The `--rm` flag instructs Docker to also remove the anonymous volumes associated with the container if the container is removed

## Links

* [Install Docker][install_docker]
* [DBeaver][dbeaver]
* [VSCode][vscode]

[install_docker]: https://docs.docker.com/engine/install/
[dbeaver]: https://dbeaver.io/download/
[VSCode]: https://code.visualstudio.com/Download
