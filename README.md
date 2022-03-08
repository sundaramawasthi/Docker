TABLE  OF CONTENT 

   INTRODUCTION
1. Container
    Benifit of Container
2. Container vs Virtulization
3. Docker
4.  Docker Platform
       Use of docker platform
5. Advantage
6. Feature
7. Docker Component
   7.1     Docker Architucture
              Key Component of Docker Architucture
   7.2     Docker Object
              Different type of docker Object
   7.3     Docker Engine
   7.4     Docker Images
               Type of docker images
  7.5       Docker Container
  7.6       Docker Networking
                Network Driver
                Type of network driver 
        
Introduction
In a Inial Stage  we  can run  only one application on one server.
one server for one application , So , suppose 200 people use the application but when people incease load also increase , and we don't have the way to run multiple application on server. Every time for new application we have to  buy a new server .
Virtual Machine


Virtual Machine
So, the one application for one server problem  solved by VMware  by virtual machine .VM machine solve one application on one server problem , Now you can run multiple application on same server . but vm required their own OS. Its far better than one application on one server but not so good.

PROBLEM -
 There is some problem are still there -
1.  The problem comes with Virtual machine is its need there own Os. Which is also take some storage and space.
2.  Shift one code one point to another then migration are consuming .
3.  Suppose you built an application and give it to your developer friends to test it , but it not run on their machine , it say some files, or version is mismatch .


CONTAINER -
A container is a piece of software that package code and all of its software . It Contain the software package , data , dependencies and all other staf that required to run a container . 
We also say that Containerization is define form of operating system virtulization through which application run isolated user spaces called Container .
Container


BENEFIT OF CONTAINER -
 1. Portability -> A container seperate application from thier host operating system making then portable.

2. Scability - > A Container application with a service application designe can handle growing workload
   resulting increase application scability.

3. Faster Deployment -> A contaier can create a master version of an image that can be distribuated
   on demand , increase app productivity.

4. High productivity -> Container allow developer to track and make changes to the platform's
   source code .

5. Enhanced security -> Containerization enhanced Security by adhering to an app seperation mechanism .

6. Continuity - > Containerization ensures continuity because container operate independently,
   if one container fail due to some reason it's does not affect other.
 
CONTAINER VS VIRTULIZATION -
1. Virtualization

Virtualization allow you to run different systems on the same physical servers hardware . 
Concept of virtual machine is use as fundamental unit of virtulization 
Virtualization allow you to run several operating system on a single physical server hardware
Virtualization replicate real hardware 
Virtualization is heavy weight operation that consume lot of resource
Virtualization provide complete isolation from the host OS .
Virtual machine has its own Operating System 
Startup time in a minute
virtualization is not portable.

2. CONTAINERIZATION 


Containerization use the container .
where Containerization allow you to deploy new application on same server with same operating system. 
In container its replicate at os-level 
Containerization is lightweight operation it now container lot of resource.
Less isolation from host OS
container share the same os that is host os . 
Startup time in a secound . 
Containerization is portable.
Docker - 



DOCKER is helping us to run application on isolated enviroment, Docker is popular Contanerization tool. Docker is Contanerization platform from packageing your application along with all
of this dependencies .

The whole idea of docker is to easily developed the application ship container that can be deploy evreywhere.It is free and open platform creating , delivery and operating application.

 
 DOCKER PLATFORM - 

Docker platform is one of the feature provide by docker to manage the lifecycle of container .
Docker Provide the ability to package and run an applicaion loosly isolated enviroment called a
container .
 

USE OF DOCKER PLATFORM -
       we use docker platform to development , deployment , testing the application.
       Wheather your production enviroment is Data Center , Cloud provider , hybried of tools its   work same for all .

ADVANTAGE OF DOCKER -
       The advantage of docker is that we can  BUILT, TEST, DEPLOY AND MAINTAIN our application in very easy way . we don't need to move here and there for resources.

 FEATURE -
       The feature provided by docker are - 

  1. SCALABLE
  2.PROVIDE EASY AND FASTER CONFIGURATION
  3. IS ABLE TO REDUCE THE SIZE
  4. INCREASE PRODUCTIVIY
  5. APPLICATION ISOLATION
  6. SWARM
  7. ROUTER MESH
  8. SERVICES
  9. SECURITY MANAGEMENT


  DOCKER COMPONENT -

  1. DOCKER ARCHITUCTURE -

  Docker built on Client-server Architucture. The docker Client commnucate with docker daeman which handle construction , distribuation and execuation of docker container . 
You can use docker client or docker daeman on same machine or you can use it seperatly. Docker Client and docker doeman use a RESTAPI , UNIX Socket Or network interface to commnucate .



 KEY COMPONENT OF DOCKER ARCHITECTURE -


1.  DOCKER HOST
IT OFFER Complete enviroment of execuete and running application that include docker deoman that is also a core component .
docker daemon handle docker object such as images, volume , container , network by listeing docker
API request .to manage request docker daeman commnucate with other daeman

2. DOCKER CLIENT .
Docker User can use client intract with docker when client execuate a docker command its transmit to docker daeman which execuate it

3.  DOCKER REGISTRY - >
docker images are store in docker registry , docker hub is a public repository that anybody can use.
4.  DOCKER OBJECT -
you can create a images container , network , volume , plugins and another thing when you use docker



 DIFFERENT TYPES OF DOCKER OBJECT -
   1 . IMAGES-  
          Image is just a file that contain the instruction .
          Image is a read only template , lot of time image based on other image with another custum,

   2.  Container 
          docker container are created when you ran a docker images .It is a running instance of docker   image . This container contain all of application on tHE enviroment.Docker API or docker CLI are use to start and stop the container.
     3. Volume . 
          volume are use to store persisitant data generated by docker and utilizes by docker container.
    4.   Network.
         A way for all isolated container to commnucate with one another.

4. DOCKER ENGINE 
Docker engine is a core part of whole docker engine , It is an application with a client-serever archiitucture that are insalled on host machine .
ITS has three component server, API , CLI .

5. DOCKER IMAGES -

An images is read only template for building a docker template that is based on another image that is been modified someway you can either make your images used these images that are developed by other and made available through registry .
TO create a images you can create a docker file for a simple syntax for define the step required .
a layer of images are created a each instruction of docker file when you change the docker file and rebuilt the image only those layer are changes and rebuilt .


 TYPES OF DOCKER IMAGES -

  Docker images are divided into two categories .

 1. Parent images -
    
    It is specified by the FORM directive in the image's pf dockerfile .
    It serves as a foundation of all docker command .
    A dockerfile from scratch directive creates a basic images without using any parent images.


 2. BASE IMAGES -

      It does not have parent images in his docker file .
      A FROM scratch directive is used in a dockerfile to create it .

DOCKER IMAGES COMMAND - 

      docker image build -> create an image
      docker image history -> display an image history
      docker image inspect -> display expensive info abot one or more images
      docker image ls -> list the images
      docker iamge prune -> delete unused images
      docker image pull -> pull images from registey
      docker images push -> push image to repositiry
      docker image rm -> delete one or more image
      docker image save -> save one or more image

.DOCKER CONTAINER -

A container are runnable instance of images.
a container are isolated from other container and its host machine .
When you create  or start a container you define it by its images any configuration option you give
any chages to state of container that is not save in persisitance storage lost when container are remove .

Docker container is tools that is used to create test and deploy to an application.
you can create , start, stop, move a container , delete a container by the help of docker API and CLI
Also you can attach storage to container connected to one or more network construct a new images

DOCKER NETWORKING -

Networking allow docker container to commnucate with each other .

 NETWORK DRIVER -

The network subsystem in docker is driver based plugable By default docker provide some driver with basic functionality are -
1 Bridge
2. Host
3. overlay
4. macklay
5. none

    BRIDGE -
    CONTAINER RUN ON SAME DOCKER DAEMAN SERVER AND CONNECTED BY  BRIDGE .
    A software bridge is use in a bridge network to allow container connected to same network to commnucate while isolated them to container not connected to the bridge network.

Docker bridge driver implement to rule the host machine to prevent container directly commnucate to host machine .

   HOST -
when you use host network for container ,network stack of that container is not isolated from docker host.the container share the host's networking namespace and container not assigne the ip address .

  OVERLAY -
The overlay driver conncted to many docker daeman host to form a distribuated network when encryption is enable then this network sit top on overlay specific network allow container (including swarm service)connected to it .

  MACVLAN -
Its a idea for legacy network traffic monitoring app that demand to directly conected to the physical network .in this case macvlan driver assigne mac address to each container virtual network interface , making appear to physical network interface link directly to physical network.

  NONE -
It is use to completely disable the network stack on the container.
You can use network none flag when start a container .

 
DOCKER REGISTRY AND DOCKER HUB -


DOCER REGISTRY -
It is storage and distribuated system for name docker images .
docker registry is organised in docker registry where repositiory hold all version of docke images
Registry alllow to docker user pull images locally and push new images to registry.

User should use Registry if they want to -

   Ensure their images are saved in a secure place .
   Have complete control of image distribuateion
   Integrate image storage and distribuation.
DOCKER HUB -

 Dockerhub is largest  container library and commnuity , A user can browse over 100000 image   softare manufacture opensource project  Commnuity . 

 Docker hub is docker host repository that allow us to share the images with the team

   FEATURE  OF DOCKER HUB -
         1. PRIVATE REPO
         2. AUTOMATED BUILT
         3. TEAM AND ORGANIATION
         4. OFFICIAL IMAGES
         5. PUBLISHED IMAGES
         6. WEB HOOKS


   DOCKER HUB ALLOW YOU TO -
         1. EXPLORE WORLD LARGEST CONTAINER REPOSITIORY
         2. EASY SEARCH OVER 1 MILION IMAGE
         3. SHARE AND STORE IMAGES ON PUBLIC AND PRIVATE REPO
         4. ACCESS FREE REPOSITIORY
         5. BECAME A VERIFY PUBLISER
         6. RUN MORE TECH IN CONTAINER WITH CIRTIFIED INFRASTRUCTURE.




 DOCKER COMPOSED -


Docker composed is a tools that allow user to define and run multi-container docker application.

Composed use a YAML file to figure your application services then by single command you can start your services .

Composed is campitable for all enviroment -

PRODUCTION
STAGING
DEVELOPEMENT
TESTING
CONTINEOUS INTEGRATION

PROCESS -

Create a docker file to difine your app enviroment so it can be replicated every where
docker composed define YAML to figure out services.
Then RUN docker composed ...
THANKYOU FOR READING .....
