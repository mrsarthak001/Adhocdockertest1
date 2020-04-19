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
