#  - Twitter API
> This project pretends to be a copy of the twitter api.

## Table of Contents:
- [- Twitter API](#--twitter-api)
  - [Table of Contents:](#table-of-contents)
  - [Description](#description)
    - [Features](#features)
  - [Requirements:](#requirements)
  - [Installation](#installation)
  - [Run it locally](#run-it-locally)
    - [With docker](#with-docker)
    - [Without docker](#without-docker)
  - [Basic Usage](#basic-usage)


## Description
This is project is a simple REST API made with FastAPI for learning purposes.

### Features
Features included:
- Data modeling with pydantic.
- Data validation.
- CRUD of users.
- CRUD of Tweets.
- SQLAlchemy (MYSQL)
- Docker dev environment
- JWT Authentication
- FastAPI Router
- MyPY

## Requirements:
- Python >= 3.6
- Docker and Docker Compose (Optionally)

## Installation
1. Clone or download de repository:
    ```
    $ git clone git@github.com:JuanCarlosAguilarB/apirest-twitter.git
    ```

2. Open the console inside the project directory and create a virtual environment (You can skip this step if you have docker installed).
    ```bash
    $ python3 -m venv venv
    $ source venv/bin/activate
    ```

3. Install the app (You can skip this step if you have docker installed)
    ```bash
    (venv) $ pip install -r requirements.txt
    ```

## Run it locally
Copy the `env.example` file into the same directory with the name `.env`
```bash
$ cp ./env.example ./.env
```


### With docker
1. Run it with Docker Compose.
```bash
docker-compose up
```

### Without docker
1. Configure the environment variables into the `.env`.
```bash
# App
SECRET_KEY=rVsvupYHUbAgOGNMw0ytII_7tkn_iWkBhktVR_i3Tg8=  # You can leave this dev key as is.
DEBUG=True  # If DEBUG = True, the reload option of uvicorn will be enabled
PORT=8000  # Server port

# Database
DATABASE_URL=mysql+pymysql://${YOUR_USER}:${YOUR_PASSWORD}@${HOST}:${PORT}/${DATABASE NAME}  # Configure your database credentials here.

```

2. Run the server.
```bash
$ python3 main.py
```

## Basic Usage
Once you are running the server open the [Swagger UI App](http://localhost:8000/docs) or http://localhost:8000/docs to checkout the API documentation.
