# ethminer-docker
Allows you to build ethminer in a docker container. 

### How to

```
docker build -t ethminer-builder .
docker run -v $(pwd)/build:/ethminer/build ethminer-builder
```
