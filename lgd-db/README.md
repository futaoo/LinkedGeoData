Run the Makefile to build the nominatim.so file required by this image

`make`

The original repo can only pull an amd64 docker image to host the PostGIS database, which can be very low-efficiency most of the time for people like me using arm64-based machine for experiments. 

I changed the docker image source from `postgis/postgis:14-3.2-alpine` to `arm64v8/postgres:14-alpine3.16` and added a built script adding PostGIS extentsion. The original script can be found at [this](https://github.com/postgis/docker-postgis/blob/master/14-3.3/alpine/Dockerfile) page.

