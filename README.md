# BIMserver
Deploy BIMserver in a Docker container

#### BIMserver 1.5.63

Deploys on a remote server with Ubuntux64:latest. The Dockerfile will install dependencies such as JDK and Tomcat and then install BIMserver into the webapps dir inside Tomcats home. Simply SSH into a server, install Docker with

```bash
$ wget -qO- https://get.docker.com/ | sh
```

and run the following (change username and password to your own choice):

```bash
$ docker run -d \
	-e TOMCAT_USER=xxx \
	-e TOMCAT_PASSWORD=xxx \
	-p 8080:8080 \
	--restart=always \
	px3l/BIMserver
```

This will pull the 'latest' tagged image. For other tags please see Tags on Dockerhub. To use a specific tag, put `:TAGNAME` after the docker image at the end of the run command.