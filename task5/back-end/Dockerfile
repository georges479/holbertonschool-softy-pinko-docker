# base from ubuntu
FROM ubuntu:latest

# Update the current packages
RUN apt-get update

# Upgrade all installed packages
RUN apt-get upgrade -y

# install python3 and pip
RUN apt-get install -y python3 python3-pip

# Remove the EXTERNALLY-MANAGED file to allow pip installations
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

# install flask
RUN pip3 install flask

# install flask-cors
RUN pip3 install flask-cors

# define working directory
WORKDIR /app

# copy Flask script into the image
COPY ./api.py /app/api.py

# run the Flask app
CMD ["python3", "api.py"]