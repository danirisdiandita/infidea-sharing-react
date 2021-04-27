# Docker for React 

## using docker for development

use the default `Dockerfile` inside this repository root folder
```
docker build -t infidea-sharing-react .
```

run in development mode 
```
docker run \
    -it \
    --rm \
    -v ${PWD}:/app \
    -v /app/node_modules \
    -p 3001:3000 \
    -e CHOKIDAR_USEPOLLING=true \
    infidea-sharing-react 
```

## using docker-compose for development 
build the docker image and run the docker container based on the image built 
```
docker-compose up --build 
```
stop the docker image 
```
docker-compose stop 
```

source: dockerising a react app https://mherman.org/blog/dockerizing-a-react-app/