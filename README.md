# Cinema API
This is a simple API for a cinema service. It is written in Python using the Django REST Framework.
## For this project you must use Docker.
Make sure that docker is working properly on your machine
## Installing using GitHub
Install PostgresSQL and create db
```
git clone https://github.com/BohdanLazaryshyn/Cinema-API.git
cd cinema_API
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```
## Prepare docker-compose
To use docker-compose, create .env file and enter the following data there
```
POSTGRES_HOST=db
POSTGRES_USER=postgres
POSTGRES_PASSWORD=secretpassword
POSTGRES_DB=postgres
POSTGRES_NAME=postgres
```
## Run server
```
python manage.py migrate
python manage.py runserver
```
## Run docker
```
docker-compose build
docker-compose up
```
## Getting access
+ create user via /api/user/register/
+ get access token via /api/user/token/
## Features
+ JWT authenticated
+ Admin panel /admin/
+ Documentation is located at /api/doc/swagger/
+ Managing orders and tickets
+ Creating movies with genres and actors
+ Creating Cinema halls
+ Adding movies sessions
+ Filtering movies and movie sessions
