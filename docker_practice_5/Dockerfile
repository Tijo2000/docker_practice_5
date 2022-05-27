FROM ubuntu:latest

RUN apt update
RUN apt install python3 -y

WORKDIR /usr/app/src

COPY inference.py ./
COPY label_map.pbtxt ./
COPY saved_model.pb ./ 

CMD [ "python3", "./inference.py" , "./label_map.pbtxt" , "./saved_model.pb"]