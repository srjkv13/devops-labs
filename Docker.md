## Docker Commands

1. ### Run a container
   `docker run <image-name>` it will run all the containers from the selected images
2. ### List the images

   `docker images` - display the images in use

   `docker images -a` - display all the images

3. ### List the containers

   `docker ps` - display the running containers

   `docker ps -a` - display all the containers

4. ### filter the images

   `docker images --filter=reference='alpine' `

   where `alpine` is the container id

5. ### export a container

   `docker export aa717d51d7a5 > <file name>`

   where `aa717d51d7a5` is the container id

   Note: Exporting a container will not store metadata info

6. ### import a container

   `docker import - impnginx < <file name>`

   where `impnginx` as image name, it will create a new image

7. ### save a container externally

   `docker save -o alpine.tar <image name>`

   Note : saving container will store all metadata info

8. ### Load container archived file to docker

   `docker load < alpine.tar`

   Note: It imports alpine.tar with metadata info, if we are using import statement it will create a new image

9. ### Accessing a container shell

   - create an image Eg: ubuntu

     `docker run -dit ubuntu`

     were d - dettached mode, i - interactive mode and t - provides a terminal

   - Accessing the container shell

     `docker exec -t <container id> bash`

   - Then access the container shell using below command

     `docker attach <container id>`
