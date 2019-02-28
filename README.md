# Dockerfiles

Here's how to start the containers:  
### Apache2
```{r, echo=false}
docker run -d -p 80:80 -p 22:22 --name myapache pferrervich/apache2  
```
### Postgres (with Duplicati)
```{r, echo=false}
docker run -it -p 22:22 -p 8200:8200 --name postgres pferrervich/postgres /bin/bash
```

### ProFTPD
```{r, echo=false}
docker run -p 21:21 -p 20:20 --name proftpd -e USERNAME=username -e PASSWORD=password -v `pwd`/ftp:/ftp pferrervich/docker-proftpd
```

### Streama
```{r, echo=false}
docker run 80:8080 -p 80:8080/udp stre
```
