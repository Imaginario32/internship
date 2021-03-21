## Prerequsite

Docker 19.03 or greater

Docker-compose 1.26 or greater

## Legend

Docker compose with 3 applications (frontend + backend + DB).

### Instructions for running

1. Bootstrap the DB:

`docker-compose up -d db`

`docker-compose run --rm flaskapp /bin/bash -c "cd /opt/services/flaskapp/src && python -c  'import database; database.init_db()'"`

2. Boot up the cluster

`docker-compose up -d`

3. Browse to localhost:8080 to see the app in action.

## Questions

1. What is the difference between Docker Compose and dockerfile? Why do I need Docker Compose?
  Docker Compose is a tool for control and running multi-container application. You use a docker-compose.yml to configure your application
  Dockerfile is a file with image creation parameters

2. How do I parameterize compose for different environments?
  You can use different docker-compose.yml files with necessary settings for each environment, like:
  docker-compose -f docker-compose.base.yml -f docker-compose.prod.yml up -d
  docker-compose -f docker-compose.base.yml -f docker-compose.dev.yml up -d

3. What types of entities are used in docker-compose and for what purpose?
  version - docker compose version
  networks - network definition
  services - provide communication between services / containers
  secrets - secrets definition
  volumes - map volumes

4. `*` How to output application logs?
  docker-compose logs -f {app_name}

4. `*` How to copy\upload a file from host machine to the container?
  docker cp {path} {container id}:{path on container}

5. `*` How to save file changes made inside the container?
  You can use volumes to save data
  or
  docker commit {cid} {new_image_name}

## Tasks

* Docker-compose has a bug - investigate it! What would you improve?

* Docker-compose with an environment file. Create 2 different environment files for docker-compose

* `*` Change the `docker-compose.yml` to run through dockerstack with code reuse (don't repeat yourself)
