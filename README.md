1. ### Run a container
   `docker run <image-name>` it will run all the containers from the selected images
2. ### List the images

   `docker images` it will list all the images
   `docker images -a` it will list all the images

3. ### List the containers
   `docker ps` it will list all the containers
   `docker ps -a` it will list all the containers
4. `docker images --filter=reference='alpine' ` filter the images using the keyword alpine
5. `docker export aa717d51d7a5 > <file name>` export container where `aa717d51d7a5` is container id
6. `docker import - impnginx < <file name> `import the tar to docker as an image where `impnginx` as image name. It will create a new image
7. `docker save -o alpine.tar <image name>` export the container with all the metadata and histories
8. `docker load < alpine.tar` import the file as an image with the metadata

9. ### Accessing a container shell
   - create an image Eg: ubuntu
     `docker run -dit ubuntu`
   - Accessing the container shell
     `docker exec -t <container id> bash`
   - Then access the container shell using below command
     `docker attach <container id>`
