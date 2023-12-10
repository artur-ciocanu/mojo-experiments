# Modular Mojo Language Experiments
This repo contains some of my Mojo language experiments.

## Installation
On Mac OS X using Intel CPU there is no other than to use Docker. I have the used
Docker Compose using this command:
```bash
$ docker compose -f docker-compose.yml build
```
Where the `docker-compose.yml` file has been downloaded from: `https://github.com/modularml/mojo/blob/main/examples/docker/`, it should be noted `docker-compose.yml` references `Dockerfile.mojosdk` which should be downloaded from the same repo.

## Running the Mojo Docker Container
```bash
$ docker run -it docker_mojo bash
```
This will start the Mojo Docker container and open a bash shell.

## Running the Mojo Docker Container with local filesystem access
```bash
$ docker run -v /<local folder>:/<container foler> -it docker_mojo bash
```

## Compile and Run the Mojo Example
Currently all the samples are in the `code` folder. To compile and run the `Hello World` example, use the following commands:
```bash
$ cd code
$ mojo run hello.mojo
```

To build an executable, use the following command:
```bash
$ cd code
$ mojo build hello.mojo
```
