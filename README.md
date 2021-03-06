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
![b](https://user-images.githubusercontent.com/64701398/86029799-415db900-ba51-11ea-91b6-87e47b8ae0b9.png) <br>

Step 2 : Creating JOB1 in jenkins to pull the Github repo automatically when some developers push repo to Github.<br>

![t](https://user-images.githubusercontent.com/64701398/86030835-a1089400-ba52-11ea-8ad2-89066f521862.png) <br>
![t4](https://user-images.githubusercontent.com/64701398/86031624-b500c580-ba53-11ea-8a35-d2828c290e99.png) <br>
![t1](https://user-images.githubusercontent.com/64701398/86030969-d614e680-ba52-11ea-824e-bdd57a1051bf.png) <br>

Step 3: Creating job2 ie looking at the code or program file, Jenkins should automatically start the respective language interpreter install image container to deploy code. <br>
![j2](https://user-images.githubusercontent.com/64701398/86032925-bf23c380-ba55-11ea-9558-cf911b382caa.png) <br>
![j22](https://user-images.githubusercontent.com/64701398/86032926-c054f080-ba55-11ea-8aa4-d35772a7b4e8.png) <br>

Step 4 : Creating job3 <br>

![j3](https://user-images.githubusercontent.com/64701398/86033153-204b9700-ba56-11ea-9829-49a8e206d253.png) <br>
![j33](https://user-images.githubusercontent.com/64701398/86033156-20e42d80-ba56-11ea-8fe8-e225ac4e5ced.png) <br>

Step 5: Creating job4 <br>
![j5](https://user-images.githubusercontent.com/64701398/86033661-ed55d300-ba56-11ea-8098-c91111b6e875.png) <br>
![j55](https://user-images.githubusercontent.com/64701398/86033663-edee6980-ba56-11ea-9ad2-b68d5ddeac8f.png) <br>

Step 6: Creating Job5 <br>
![j4](https://user-images.githubusercontent.com/64701398/86033755-11b1af80-ba57-11ea-8599-c35fe1688180.png) <br>
![j44](https://user-images.githubusercontent.com/64701398/86033761-12e2dc80-ba57-11ea-9d8e-977d3c0e2133.png) <br> <br>


![0](https://user-images.githubusercontent.com/64701398/86033967-6d7c3880-ba57-11ea-87dd-87b97fb7ffea.png)

