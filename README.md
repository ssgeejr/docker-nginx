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
curl -L demo.packman.com
curl -L donutsdontlie.com
```

Note: You will need to use the '-L' flag for curl in order for it to follow the redirect (pain in the ass to debug if you aren't aware of this little trick)
