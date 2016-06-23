# alpine-node-pm2  for docker 

### Install
  
    docker pull cowpanda/alpine-node-pm2:latest

### Create new nodejs pm2 container

    docker run -d yourAppPath:/app -v /etc/localtime:/etc/localtime:ro  \ 
    --name nodepm2 -p 3000:80 -e "APP=app.js" cowpanda/alpine-node-pm2:latest
  
  * `APP=app.js` specify your node app start file.
  
### Restart your app in docker container
  
    docker exec -it nodepm2 pm2 restart app

### Display your app logs in docker container

    docker exec -it nodepm2 pm2 logs app
  
  
