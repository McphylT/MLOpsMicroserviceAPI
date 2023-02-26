[![CircleCI](https://dl.circleci.com/status-badge/img/gh/McphylT/UdacityProj4/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/McphylT/UdacityProj4/tree/main)

## Project Overview

This project forms part of the requirements for completing the Cloud Devops NanoDegree programme.
This repository contains the material needed to operationalize a Machine Learning Microservice API. 

A pre-trained, `sklearn` model is used. It has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

The project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested


**The final implementation of the project showcases your abilities to operationalize production microservices.**

---

### Description of Files
* `app.py` contains the pre-built application we will be deploying using Docker
* `make_prediction.sh` is the script we will be calling to make predictions
* `requirements.txt` contains the dependencies we need to install as part of our environment
* `Makefile` This includes instructions on environment setup and lint tests
* `Dockerfile` contains the commands required to assemble the docker image


---

## Setup the Environment

* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash
python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
