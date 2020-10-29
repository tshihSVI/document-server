## Building docker image

For building the image, go to the root directory and build docker with this command (don't foreget last character it's a dot)

```
docker build -t document-service .
```

or use of docker-compose

```
docker-compose build
```


## Run docker image

Running the image with `-d` runs the container in detached mode and background. The `-p` flag redirects a public port to a private port inside the container.

```
docker run -d -p 3000:3000 document-service
```

or use of docker-compose that `-d` run the command in the background

```
docker-compose up -d
```


## Usefull docker commands

-   `docker images`: list of docker images
-   `docker ps`: list of docker conainers



## Usefull docker -compose commands

-   `docker-compose stop`
-   `docker-compose start`
-   `docker-compose run <custom service>`


## Frequently Problems

- ERROR: `Error: Cannot find module 'express'` <br />
- ERROR: `Error: Cannot find module 'nodemon'` <br />
  CAUSE: docker-compose > volumes <br />
  SOLUTION: Try to check node_modules 

