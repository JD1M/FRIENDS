FROM python:3.8-slim-buster


WORKDIR /usr/src/app

# set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# install dependencies
RUN apt-get update && apt-get install -y  libmariadb-dev-compat libmariadb-dev \
    build-essential libssl-dev libffi-dev \
    libxml2-dev libxslt1-dev zlib1g-dev 
   
    
RUN pip install --upgrade pip
COPY ./requirements.txt /usr/src/app/requirements.txt
RUN pip install -r requirements.txt

# copy project
COPY . /usr/src/app/