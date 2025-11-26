# baser sur la derniere version ubuntu
FROM ubuntu:latest
# Mettre a jour apt en utilisant :
RUN apt-get update
# mettre a niveau les logiciels actuel installer via apt en utilisant:
RUN apt-get upgrade -y
# installation python3 et pip
RUN apt-get install -y python3 python3-pip
# supprime la gestion externe
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED
# installe flask obligatoire de le faire avec pip et non apt
RUN pip3 install flask
# defini le repertoire de travail
WORKDIR /app
# copier le script Flask dans l'image
COPY ./api.py /app/api.py
# execute l'app flask
CMD ["python3", "api.py"]