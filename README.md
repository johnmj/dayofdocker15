# dayofdocker15

You need docker and docker-compose to run this setup.

Jenkins runs at http://YOUR-DOCKER-HOST:8080/jenkins
Artifactory runs at http://YOUR-DOCKER-HOST:8090/artifactory
Registry run at http://http://YOUR-DOCKER-HOST:5000

The testing web server (written in Go) will be accessible at http://YOUR-DOCKER-HOST:8000 - when you compile it and run it.

There is a centos-slave Docker container, which you may need to build yourself if yuo decide to modify it. 

The containers home directories (data directories) are in /opt/containers . 
The /opt/containers directory tree needs to be owned by uid 1000 and gid 1000. They are setup to have this ownership.
If you want to do something manually to these directories, you need to use sudo.

The user student is granted sudo access.

On the host, the user is member of both docker and admin groups. Created as:

root# useradd -m  -G docker,admin  -s /bin/bash -c "Student" student


There is a GoWebServer directory which contains http.go file. You can run it and it will open a port 8000 and listen on it.
This is the test project, which will be compiled by the students through jenkins.

