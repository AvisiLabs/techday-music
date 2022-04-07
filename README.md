# Techday Music

Source of GTZAN dataset: [http://marsyas.info/downloads/datasets.html](http://marsyas.info/downloads/datasets.html)

## Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AvisiLabs/techday-music/blob/master/Techday.ipynb)

## Jupyter Lab in Docker

* Open your terminal and change directory to the `docker` directory in this project
* Make sure Docker is running
* Run `make start` to run the Docker image
    * Alternatively, run this command: `docker run -p 8888:8888 -v "${PWD}/..":/home/jovyan/techday-music -e NOTEBOOK_ARGS="--NotebookApp.iopub_data_rate_limit=1.0e10" jupyter/tensorflow-notebook:lab-3.3.4`
* Open the last URL printed in your terminal, Jupyter Lab should open
* Use the file browser on the left to open `techday-music/docker/Techday-docker.ipynb`

## Jupyter Lab in Docker (M1)

* Open your terminal and change directory to the `docker` directory in this project
* Make sure Docker is running
* Run this command: `docker build . -t avisilabs/techday-music`
* Run this command: `docker run -p 8888:8888 -v "${PWD}/..":/home/ubuntu/techday-music -t -i avisilabs/techday-music`
* Open the last URL printed in your terminal, Jupyter Lab should open
* Use the file browser on the left to open `docker/Techday-docker.ipynb`
