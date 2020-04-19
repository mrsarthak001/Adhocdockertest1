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

#### [Docker HUB Image Link](https://hub.docker.com/repository/docker/sarthakjain07/rhythm)
