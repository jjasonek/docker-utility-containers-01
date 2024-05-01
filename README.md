### Node:14-alpine is extra slim node image
For some reason using extra slim image is better than normal image.

docker build -t node-util .
docker run -it -v "C:\Training\Docker\utility-containers-01:/app" node-util npm init
### Now we have package.json in our bind mount, 
### so we did call npn init without having node.js installed in our local machine  
