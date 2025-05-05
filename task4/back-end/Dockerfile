# chercher dernière version ubuntu
FROM ubuntu:latest

# maj des paquets
RUN apt-get update

# Mise à niveau des paquets
RUN apt-get upgrade -y

# installation Python3 et pip3
RUN apt-get install -y python3 python3-pip

RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# installation flask avec pip3
RUN pip3 install flask

# installation flask cors
RUN pip3 install flask-cors

# definir /app comme working directory et copier le fichier dans docker image
WORKDIR /app
COPY api.py .

# lancer le serveur
CMD ["python3", "api.py"]