[![CircleCI](https://circleci.com/gh/nyan-lin-tun/Operationalize-a-Machine-Learning-Microservice-API.svg?style=svg)](https://circleci.com/gh/nyan-lin-tun/Operationalize-a-Machine-Learning-Microservice-API)

# Operationalize a Machine Learning Microservice API

This project contains the following: 

 1. Linting project codes.
 2. Docker for containerize the applicaion.
 3. Deploy containerize application using Docker and prediction.
 4. Configure Kubernetes and create a Kubernetes cluster
 5. Deploy container using and prediction.
 6. Installation of Kubernetes and Minikube.

## Requirements

- [Python 3](https://www.python.org/downloads/)
- [Docker](https://docs.docker.com/docker-for-mac/)
- [Kubernetes](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
- [Minikube](https://kubernetes.io/docs/tasks/tools/install-minikube/)

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies

### Running `app.py`

    python app.py

## Linting project codes

    make lint

## Run applicaion with docker.

    ./run_docker.sh

## Upload docker image

    ./upload_docker.sh
> :warning: **Please don't forget to change ```dockerpath``` and ``` docker ID ``` in `upload_docker.sh`**

## Configure Kubernetes to Run locally

    minikube start
    kubectl get pod
  
  After pod status change to ```Running```

    ./run_kubernetes.sh

## To test application via Docker or Kubernetes

    ./make_prediction.sh

## Files

- config.yml: CircleCI configuration file.
- Makefile: includes instructions for setup, install, test and lint.
- app.py: Python application file.
- Dockerfile: Dockerfile for build and expose.
- run_docker.sh: Shell file to run Docker, locally.
- upload_docker.sh: Shell file to upload Docker image.
- run_kubernetes.sh: Shell file to run the app with kubernetes.
- make_prediction.sh: Shell file to test flask app locally.




