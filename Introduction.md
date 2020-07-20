* Kubernetes is container orchestration system.
* Originated from Google, Now managed by cloud computing foundation
* DockerSwarm is another container orchestration system.
	* Simpler to work with
	* Comes integrated with docker engine
	* K8s is richer as compared to docker swarm.

## Getting started
### Installation
* https://kubernetes.io/docs/tasks/tools/install-minikube/
* Ensure virtualization is supported
* Install Hypervisor - Virtual Machine software, in windows this will launch linux virtual machine (Oracle VM Virtual Box)
* kubectl ->controller program to kubernetes: install kubectl.exe and place it in classpath
* minikube-> cut down version of kubernetes for development.
* cygwin to open unix style command prompt on windows

### Running
* *minikube start*: this will run minikube in Virtual Machine. This also runs docker daemon
* *kubectl version*: This will give client verison and server version.
* *minikube ip*: to find ip address of minikube VM.

## Docker
* Enables to create containers which are self contained environments containing complete linux distribution and any application.
* Containers and Images: Image is definition of container, its binary file that contains all software and environment variables required by container to run.
Container is running instance of image.
* Install Docker: https://docs.docker.com/docker-for-windows/install-windows-home/
* *docker image ls*:: gives you list of all images that are downloaded.
* docker command line tries to connect with daemon process - docker daemon.
* docker daemon needs to run in linux or VM.
* In order to use minikube started docker daemon we can use:  *minikube docker-env* and execute the export commands.

### Images
* to find docker images: https://hub.docker.com/
* to pull an image: docker pull {imagename}:{release number}
* to run an image: docker container run -p 80:80 -d {imagename}:{release number}  -> if image doesn't exist it will pull as well
	* -p 80:80 -> left side is exposed to world and traffic will be routed to right side port of container
	* -d -> run in background
	* number will be generated to identify container.
* *docker container ls* : we can see our container running.
* container is running inside docker daemon which is running in minikube VM.
* docker container stop {four characters of id} 
* docker container rm {four characters of id} 


<img src="https://github.com/Mayank-Mehta/Kubernetes/blob/master/DockerDaemon.jpeg"/>


