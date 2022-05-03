# create network
```shell
$ docker network create web
```

# deploy traefik
```shell
$ docker-compose up -d 
```

# add labels on deploy
 
 ```
 --label "traefik.http.routers.socrate.rule=Host(\`${{ secrets.SSH_HOST }}\`)" 
 --label "traefik.http.routers.socrate.tls=true" 
 --label "traefik.http.routers.socrate.tls.certresolver=myresolver" 
 --label "traefik.enable=true" 
 --label "traefik.docker.network=web"
 ```
