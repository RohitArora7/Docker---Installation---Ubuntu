# Docker-Installation


Just Remove the previous version is exsist 

--sudo apt remove docker.io


Now 

- sudo apt update
- sudo apt install docker.io 
- docker --version 

Now Error Part 

- docker ps
Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get http://%2Fvar%2Frun%2Fdocker.sock/v1.24/containers/json: dial unix /var/run/docker.sock: connect: permission denied


Check the Running Status

- sudo systemctl  status docker

Start the docker and enable Auto Run 

- sudo systemctl  start  docker 
- sudo systemctl  enable  docker

- docker ps
Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get http://%2Fvar%2Frun%2Fdocker.sock/v1.24/containers/json: dial unix /var/run/docker.sock: connect: permission denied


Still Error Showing 

Create the docker group 

- sudo groupadd docker 

Add your user to the docker group

- sudo usermod -aG docker $USER 

Run the following command or Logout and login 

- newgrp docker

Create a image 

- docker run hello-world 








