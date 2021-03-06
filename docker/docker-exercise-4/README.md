# Docker Excercise Four

This is a simple challenge that involves publishing ports and setting environment variables, as well as mounting volumes and creating a Dockerfile when building and running a Docker container.

You will **NOT** need to modify `main.go`

You **WILL** need to modify the `Dockerfile`

## What do I do?

Build this directory into a docker container. Remember to build the go binary for Linux first!

When running your docker container you will need to:

- Set an environment variable for the PORT
- Set an environment variavle for the FILEPATH
- Publish the same port as the environment variable PORT
- Mount a volume containing `hooray.txt` into your container corresponding to `FILEPATH`
- Build the `Dockerfile` with appropraite container build steps

Take another look at [Dr. Stearn's Docker tutorial](https://drstearns.github.io/tutorials/docker/) if you need hints!

## Test it out

Open a browser window and go to `localhost:<port>`. If everything went well you should see a success message. If you aren't able to connect then you there is an issue with your ports!

If your container crashed, use `docker logs <container-id>` to see what the issue is and fix it!

*If you named your container, you will need to remove it before you can start another with the same name.*

## Stop and remove the container

You likely don't need or want this container to be running any more so let's stop and remove it.

Run `docker ps` to list all currently running containers and copy the `CONTAINER ID` of the docker exercise container.

Stop the conainer:

`docker stop <container-id>` or `docker stop <container-name>`

Remove the container:

`docker rm <container-id>` `docker rm <container-name>`

*When you run `docker stop` and `docker rm` you will see the container ID printed to your terminal window. You can treat this as a success message.*

Remember that you can also stop and remove a running container in one command:

`docker rm -f <container-id>` or `docker rm -f <container-name>`

This forces the removal of the container, even if it is currently running.
