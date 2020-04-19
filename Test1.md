# Question 1

#### Create Dockerfile as follows
```
FROM alpine
MAINTAINER mrsarthak001@gmail.com
ENTRYPOINT date +%T
```

#### Build the image from Dockerfile as follows
```
docker build -t alpine:sarthak .
```

#### Create containers
#### Create 1st Container
```
docker run --name sarthak1q1 alpine:sarthak >> question1.txt
```

#### Create 2nd Container
```
docker run --name sarthak2q1 alpine:sarthak >> question1.txt
```

#### Now the 2 time values will be saved in you file names question1.txt

# Question 2
#### Run the Command to create the Dockerfile
```
docker build -t adhoc:sarthak https://github.com/redashu/summer2020dockertest.git
```

#### Use this command to tag the image
```
docker tag adhoc:sarthak sarthakjain07/adhoc:sarthakjain07
```

#### Then use this to login to docker
```
docker login
```
##### Enter you username and password

#### Run the command to push to docker hub
```
docker push sarthakjain07/adhoc:sarthakjain07
```

#### The image has be uploaded to Docker Hub
##### [Link to the Image](https://hub.docker.com/repository/registry-1.docker.io/sarthakjain07/adhoc/tags?page=1)


# Question 3

#### To run the container use
```
docker run -d --name sarthak.j3q3 -p 8000:80 dockerashu/ckad:v2
```
#### Accessing using
```
http://52.204.127.145:8000/
```

### Number of time "Docker" is shown: 7

#### Output
![DockerOutput](https://github.com/mrsarthak001/Adhocdockertest1/blob/master/q3.PNG)


# Question 4
#### Cloning the website repo
```
git clone https://github.com/redashu/beginner-html-site-styled
```

#### Renaming the folder
```
mv beginner-html-site-styled webapp
```

#### Creating Dockerfile
```
FROM centos
MAINTAINER mrsarthak001@gmail.com
RUN yum install httpd -y
COPY webapp /var/www/html/
EXPOSE 80
ENTRYPOINT httpd -DFOREGROUND
```

#### Running Container from the Image
```
docker run -d --name sarthak4q4 -p 8081:80 sarthak:q4
```

#### Accessing the website
[Link to Website](http://52.204.127.145:80/)


#### Tagging the image
```
docker tag sarthakjain07:q4 sarthakjain07/sarthak:q4
```

#### Pushing to Docker HUB
```
docker push sarthakjain07/sarthak:q4
```

#### [Docker HUB Image Link](https://hub.docker.com/repository/docker/sarthakjain07/adhoc)

# Qustion-5
#### Creating Docker Volume
```
docker volume create sarthakq5
```

#### Creating Container
```
docker run -it --name sarthak5q5 -v sarthak.j5:/adhocvol -v /etc/passwd:/user.txt alpine sh
```

#### Then inside the container run
```
wc -l user.txt > /adhocvol/usercount.txt
```

#### Lines Count: 28
