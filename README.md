# Petclinic

# Prerequisite 
Linux machine with docker servie up and running and git command line tool 

Minikube up and running 

helm installed 

 how to install Docker service on ubuntu:
https://phoenixnap.com/kb/install-docker-on-ubuntu-20-04

 how to install git command line tool: 
https://linuxize.com/post/how-to-install-git-on-ubuntu-18-04/

 How to install minikube:
https://minikube.sigs.k8s.io/docs/start/

 How to install helm:
https://helm.sh/docs/intro/install/

# How to Create docker image 
 ```
 git clone https://github.com/morbendor/Petclinic.git
 cd Petclinic 
 docker build -t <image_name:tag> .
 ```
 # How to save docker image 
 in order to save the image as file run 
 ```
 docker save -o <save_file_locatio/filename.dockerfile> <image_name:tag>
 ```
 # How to run docker container  
```
 docker run -p 8080:8080 <image_name:tag>
 or 
 docker-compose up -d 
```

# How run image as a pod in minikube
```
minikube image load <"YOUR_FILE_LOCATION">
example: minikube image load "C:\Users\XYZ\Desktop\Home_challenge\image\petclinic.dockerfile"
cd <"HELM_FOLDER_LOCATION">
example: cd C:\Users\XYZ\Desktop\Home_challenge\helm\
helm install petclinic
```
# Monitor application state 
 check the pod name with this command and copy the name
```
kubectl get pods
```
 check application state with this command 
 ```
 kubectl logs -f <POD_NAME_FROM_PREVIOUS_STEP>
 ```
 wait until you get "Started Jetty Server"
 
 after you see this line close the log mointor with ctl+c
 
 check service name with this command
 ```
 kubectl get svc
 ```
 copy the service name
 
 open tunnel from minikube to your PC
 
 ```
 minikube service <SERVICE_NAME_FROM_PREVIOUS_STEP>
 ```
 
