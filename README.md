## Docker Commands

- ***docker version***
  
- ***docker run hello-world***
    
    by using this command, we are talking to client that talk to docker server for running a container through hello-world image
    
- ***docker run busybox echo hi there***
    
    echo is going to print out ‘hi there’
    
- ***docker run busybox ls***
    
    give us all files and ficrectories
    
- **docker ps**
    
    give us all containers that are running in background.
  
- **docker ps -d**
  
    give all all running containers.
    
- ***docker ps --all***
    
    give us All containers
    
- ***docker ps -a -q***
    
    Delete all containers that are not running
    
- ***docker system prune***
    
    Remove all containers
    
- ***docker image prune***
    
     remove all images
    
- ***docker build -t neginazadi/redis:latest***
    
    build and create image based on docker file
    
- ***docker run busysbox ping google.com***
- **docker run = docker create (container out of image) + docker start**
- ***docker create hello-world***
    
    by creating image, in response it gives us an Id of the container
    
- ***docker start -a <container Id>***
    
    start container.  -a means watch the output of container and print them out.
    
- ***docker logs <container Id>***
  
- ***docker stop <container Id>*** ⇒ stop the container

    it says ok stop the container with some additional things like cleanup things like save some files or emit some messages.
  
- ***docker kill <container Id>***
    
     kills signal and shutdown container without additional things
    docker stop gets 10 seconds to shutdown. if it doesnt shutdown in 10 seconds automatically it goes to issue docker kill to shutdown.
    
- ***docker run redis***
    
    create an image for redis. at the end, you have to get this message: Ready to accept connections
    
    now we want to issue redis-cli inside of the container ⇒
    
    in another CMD we issue this command: 
    
    ***docker exec -it <container Id> redis-cli***
    
    -it means -i -t but shortly  is -it ⇒ -i is for attaching terminal inside STDIN in container.
    
    -t is for nicely formatted.  exec is when we want to execute a command inside a running container
    
    STDERR : showing errors inside running process
    
    ***docker exec -it <container Id> sh*** ⇒ sh is a shell and very powerful for all inside commands
    
    


