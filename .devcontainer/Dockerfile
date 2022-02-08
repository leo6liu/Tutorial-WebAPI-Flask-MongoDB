# file: .devcontainer/Dockerfile
#

FROM ubuntu:20.04

# update Ubuntu
ENV DEBIAN_FRONTEND=noninteractive
RUN apt update && apt upgrade -y

# install python3
RUN apt install -y python3 python3-pip

# install python packages
RUN pip install Flask
RUN pip install flask-mongoengine
RUN pip install flask-bcrypt

# install mongosh
# https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/
RUN apt install -y wget gnupg
RUN wget -qO - https://www.mongodb.org/static/pgp/server-5.0.asc | apt-key add -
RUN echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/5.0 multiverse" | tee /etc/apt/sources.list.d/mongodb-org-5.0.list
RUN apt update
RUN apt install -y mongodb-mongosh

#
# end of file: .devcontainer/Dockerfile
