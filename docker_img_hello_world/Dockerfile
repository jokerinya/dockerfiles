# base image
FROM ubuntu:18.04
# update
RUN apt-get update -y
RUN apt-get install python3 -y
# working directory (make if there is no directory)
WORKDIR /my_app
# copy /app folder and paste it to current directory
COPY /app .
# run on sh "python3 app.py"
CMD ["python3", "app.py"]
