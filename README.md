# Jenkins-Docker-and-Git-Task2-
Objective:
1. Create container image that’s has Jenkins installed using dockerfile
2. When we launch this image, it should automatically starts Jenkins service in the container.
3. Create a job chain of job1, job2, job3 and job4 using build pipeline plugin in Jenkins
4. Job1 : Pull the Github repo automatically when some developers push repo to Github.
5. Job2 : By looking at the code or program file, Jenkins should automatically start the respective language interpreter install image container to deploy code ( eg. If code is of PHP, then Jenkins should start the container that has PHP already installed ).
6. Job3 : Test your app if it is working or not.
7. Job4 : if app is not working , then send email to developer with error messages.
8. Create One extra job job5 for monitor : If container where app is running. fails due to any reson then this job should automatically start the container again.

Implementation:

Step 1: Creating Jenkins image 

You can find the dockerfile for creating jenkins image in this repository with file named Dockerfile.

Now build the image using docker build command 
docker build -t jenkins:1.0 
After successfull build launch the container using docker run command <br> 
![v](https://user-images.githubusercontent.com/64701398/86028712-dc559380-ba4f-11ea-9706-ca8ff0ee98e1.png) <br>

New container will launch that has jenkins installed.
Now open jenkins using the url as your container's ip address and port number 8080 similar to this 
172.17.0.2:8080
Jenkins home screen will appear. 
For initial password use cat command followed by the location provided in home page of jenkins<br>
![b](https://user-images.githubusercontent.com/64701398/86029799-415db900-ba51-11ea-91b6-87e47b8ae0b9.png)<br>

