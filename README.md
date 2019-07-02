# docker-nginx
Simple docker testing for nginx proxy

Build the two images  
```
./build
```

Start the two images with docker-compose
```
docker-compose up -d && docker-compose logs -f
```

connect to the client and test the proxy redirect
```
docker exec -ti client /bin/bash
ping demo.pacman.com
culr -I demo.packman.com
```
