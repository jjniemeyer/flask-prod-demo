# pull base image
FROM python:3.10-slim-bullseye

#set working directory
WORKDIR /usr/src/app

# python environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# install system dependencies
RUN apt-get update && apt-get install -y netcat

# install python dependencies
RUN pip install --upgrade pip
COPY ./requirements.txt /usr/src/app/requirements.txt
RUN pip install -r requirements.txt

# copy everything to workdir
COPY . /usr/src/app

ENTRYPOINT ["/usr/src/app/entrypoint.sh"]