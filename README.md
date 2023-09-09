[![CircleCI](https://dl.circleci.com/status-badge/img/gh/caotatcuong/project-ml-microservice-kubernetes/tree/master.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/caotatcuong/project-ml-microservice-kubernetes/tree/master)

# Operationalize a Machine Learning Microservice API

## Project Overview
Deploy a python flask application to Kubernetes to serve predictions for housing price. It uses a a pre-trained, sklearn model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on.

## Code structure
```
* /.circleci : CircleCI configuration file for running the tests
* /model_data : Pretrain model
* /output_txt_files : Log of Output 
* Dockerfile : Dockerfile for building the image 
* Makefile : Install dependencies and lint tests
* app.py : Python flask app that serves out predictions (inference) about housing prices through API calls
* make_prediction.sh : Send a POST request to the Python flask app to get a prediction
* requirements.txt : require python libaraies
* run_docker.sh : run app in Docker container
* run_kubernetes.sh : run the app in kubernetes
* upload_docker.sh : upload the docker image to docker hub
```
## Getting started

Create a virtualenv

```
python3 -m venv <your_venv>
source <your_venv>/bin/activate
```

Run `make install` to install the necessary dependencies

Run ``./run_kubernetes.sh`` to start application

Run ``./make_prediction.sh`` to run predict