# Docker-Angular-app
Docker-Angular-app  deployed on NGINX web-server.

# Application 
![image](https://github.com/user-attachments/assets/a30257cd-7722-4997-be97-fa600db3d655)



# Requirements and Point to noted 

1.	Angular is a framework which is used to develop frontend of application (UI)

2.	We will use NODE software to build and run Angular & React application.

3.	Angular app libraries will be configured in "package.json" file

4.	To download libraries configured we will use 'npm install' command.

5.	To build angular application we will use below command

			npm run build --prod

Note: When we run above command 'dist' folder will be generated for deployment.

=> To deploy angular application we will use NGINX webserver.


# Docker-Angular-app
  

Clone git repo

```bash
$ git clone https://github.com/Ashish89Rangari/Docker-Angular-app.git
```

Go inside the project folder

```bash
$ cd Docker-Angular-app
```
Build the image using the following command

```bash
$ docker build -t ng-app .
```
Run the Docker container using the command shown below.

```bash
$ docker run -d -p 80:80 ng-app  
```
To list Docker images and container using the command shown below.

```bash
$ docker images 
$ docker ps 
```
To Push docker image in Dockerhub first tag it , if tagged push directly to Dockerhub.

```bash
$ docker tag ng-app:latest ashishr99/docker-angular-app:latest
$ docker push ashishr99/docker-angular-app:latest 
```

# For windows
The application will be accessible at http://localhost:80

# For Linux
The application will be accessible at http://public-ip:80
