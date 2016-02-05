# Mongodb-docker

This is a vagrant vm aim to be only a mongo instance. It is a vm with mongo docker image downloaded and ran by the provision.

## Specification

1. Contains a **mongo 3.2** docker container.
2. `docker-composer` a tool for defining and running docker multi-container.
3. Forwarded port
- ssh is forwarded from the port 22 to the port 1234
- mongodb is forwarded from the port 27017/tcp to the same guest port.

## Instructions

1. The `src-docker` folder contains everything referent to the docker images.
2. The `dump` folder is aim to contain database dump.

**Note:**
```
Both folders **src-docker** and **dump** are automatically mount into the vm onder the **vagrant_data** folder.
```

3. The mongo container is automatically load when the vm start.

**Note:**
```
If you wanna change that just comment into the **./src-docker/mongodb_init** 
the line that start the container. 
```