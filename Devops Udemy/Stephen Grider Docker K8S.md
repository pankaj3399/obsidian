docker run <image name> -> Run the image

docker run <image name> command -> The command will override the default command that was supposed to run when docker started the image.But this command will only run if the filesystem in the image supports that command.

docker ps -> list running containers

docker ps --all -> list all containers ever created

docker run = docker create <image name> + docker start -a <container id>

-a basically watches output of the image and prints it on terminal

docker system prune -> to delete everything

docker logs <container id> -> to see container logs

docker stop <container id> -> issues a SIGTERM system call, gives process a little bit time to clean up and then stop itself 

docker kill <container id> -> Issues a SIGKILL system which instantly stops the process and container 

docker exec -it <comtainer id> <command> -> To execute command inside container. -it allows us to give input to container

docker build ->> Build image out of dockerfile

docker build **--no-cache** **--progress=plain** .(Use this to disable buildkit and see errors more properly)

docker build -t pankajvatwani/abc:latest  . -> Tagging the image.Now in docker run you can use the id or the tag

docker run -p 8080:8080 <image id>.  -> Port mapping for image

docker-compose up ==> docker run myimage

docker-compose up -- build => docker build . docker run myimage

docker-compose up -d => run in background

docker-compose down => stop containers

you can attach restart policy with docker-compose.yaml to tell docker the restart policy when container crashes

docker-compose ps => containers that are running/status. Only works when you run it from directory where docker-compose file is present.

docker build -f Dockerfile.dev . -> If the docker file name is different use this

