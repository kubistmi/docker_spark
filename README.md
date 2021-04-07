# docker_spark
[![Build Status](https://dev.azure.com/MichalKubista/Spark%20Dockerfiles/_apis/build/status/kubistmi.docker_spark?branchName=master)](https://dev.azure.com/MichalKubista/Spark%20Dockerfiles/_build/latest?definitionId=5&branchName=master)

A set of Spark dockerfiles:
- executor can be used in `Visual Studio Code Remote - Containers`
- driver can be used in `Kubernetes` setup

Serves mostly as learning project.

## Usage
You can either build the image on your own, or download from DockerHub.

#### DockerHub
Check the [DockerHub](https://hub.docker.com/u/kubistmi) for the image name and pull into your machine.

```{bash}
# download only -----------------------------------------------------------
docker pull kubistmi/pyspark:latest

# download (if not already present) and run -------------------------------
docker run kubistmi/pyspark:latest
```

#### Own Build
1. download the repo
1. navigate to the folder containing the dockerfile you want to use
1. build the image

```{bash}
#!/bin/bash

# download
git clone git@github.com:kubistmi/docker_spark.git

# navigate and build
cd docker_spark/executor
docker build -t user/image:version
```
