### Node:14-alpine is extra slim node image
For some reason using extra slim image is better than normal image.

docker build -t node-util .
docker run -it -v "C:\Training\Docker\utility-containers-01:/app" node-util npm init
### Now we have package.json in our bind mount, 
### so we did call npn init without having node.js installed in our local machine  

## let's restrict commands to be executed in docker run to npm <something>

docker build -t mynpm .
docker run -it -v "C:\Training\Docker\utility-containers-01:/app" mynpm init
### Now we have the package.json file again
### And we can call another npm command, for example **npm install**:
docker run -it -v "C:\Training\Docker\utility-containers-01:/app" mynpm install

## Using compose.yaml we can simplify the command to do the same thing.

docker compose run --rm npm init
docker container prune