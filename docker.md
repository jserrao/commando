## Docker stuff

1.  `docker-compose build` (builds a docker image, based on a Dockerfile and a docker-compose file - both should be in the root of the project)
2.  `docker-compose up -d` (turns on the container you just built)
3.  `docker-compose logs -f` (spits out logs when Docker fails - and you better believe Docker will fail on you)
4.  `docker ps` (take a look at the containers you have running)
5.  `docker exec -it <your-container-here> <your-bash-cmd-here>` (lets you run commands against the container)