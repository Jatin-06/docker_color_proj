# docker_color_proj

FROM ubuntu  <br>
RUN apt update && apt install nginx -y <br>
COPY . /var/www/html  <br>
CMD nginx -g 'daemon off;'    //this command will stop daemon so that it wont run in background. We want nginx to run in foreground <br>

docker build . -t jatin      //this command will make image  <br>
docker run -d -p 9090:80 jatin  //will create container  <br>
pen browser hit ip:portnumber <br> 
