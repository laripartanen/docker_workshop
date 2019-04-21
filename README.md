# Docker workshop

## Basic commands

Build
```
docker build -t laripartanen/mynginx .
```

Run (with variants)
```
docker run -d --rm -p 80:80 mynginx
docker run -d -v $(PWD)/static:/usr/share/nginx/html -p 80:80 mynginx (bind mount)
docker run -d -v www:/usr/share/nginx/html -p 80:80 mynginx (volume)
```

Publish
```
docker login
docker push laripartanen/mynginx
```

Save image
```
docker save mynginx -o mynginx (tarball)
```

Other useful commands
```
docker images
docker ps -a
docker top <container ID>
docker inspect <container ID>
docker rm -f $(docker ps -a -q)
docker volume ls
```
