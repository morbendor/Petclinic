# Petclinic

# Prerequisite 
Linux machine with docker servie up and running and git command line tool 

 how to install Docker service on ubuntu
https://phoenixnap.com/kb/install-docker-on-ubuntu-20-04

 how to install git command line tool 
https://linuxize.com/post/how-to-install-git-on-ubuntu-18-04/


 Minikube up and running  
 How to install minikube:
https://minikube.sigs.k8s.io/docs/start/


# Create docker image 
 git clone https://github.com/morbendor/Petclinic.git
 cd Petclinic 
 
 docker build -t <image_name:tag> .
 in order to save the image as file run 
 docker save -o <save_file_locatio/filename.dockerfile> <image_name:tag>
 if you want to run the image as a container in docker run 
 docker run -p 8080:8080 <image_name:tag>
 
 
