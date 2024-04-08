# docker_color_proj
[Docker.pdf](https://github.com/Jatin-06/docker_color_proj/files/14910393/Docker.pdf)
![Capture](https://github.com/Jatin-06/docker_color_proj/assets/125106234/0d36798d-014d-457b-9f7f-7e80888e763a)

FROM ubuntu  <br>
RUN apt update && apt install nginx -y <br>
COPY . /var/www/html  <br>
CMD nginx -g 'daemon off;'    //this command will stop daemon so that it wont run in background. We want nginx to run in foreground <br>

docker build . -t jatin      //this command will make image  <br>
docker run -d -p 9090:80 jatin  //will create container  <br>
pen browser hit ip:portnumber <br> 
