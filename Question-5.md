
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
