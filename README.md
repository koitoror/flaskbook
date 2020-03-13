# The FlaskBook App

> An advanced scalable social media app using Python-Flask with Templating and MongoDB

## The Approved Study Book Club

The FlaskBook App - The Approved Study Book Club -  is the new social application to meet share and make solo reading a thing of the past.

### Required Features

1. Users can create an account and log in.
2. Users can create profile page.
3. Users can add, edit, remove or block friends/leaders
4. Users can create or upload posts/conversations in different formats.
5. Users can see the friends posts/conversations.
6. Admin can add comment on posts/conversations by friends


## APP Installation

To set up The FlaskBook App , make sure that you have python3, postman and pip installed.

Use [virtualenv](http://www.pythonforbeginners.com/basics/how-to-use-python-virtualenv) for an isolated working environment.

Clone the Repo into a folder of your choice
```
git clone  https://github.com/koitoror/flaskbook.git
```

Create a virtual enviroment.
```
virtualenv venv --python=python3
```

Navigate to api folder.
```
cd flaskbook
```

Install the packages.
```
pip3 install -r requirements.txt

```
In order to use mongo+srv protocol, you need to install pymongo-srv
```
pip3 install pymongo[srv]
```

## APP Usage

To get the app running...

```bash
$ mongo --shell
'use <database-name>;'
```

```bash
$ mongo
'show dbs'
"
db.createUser(
  {
    user: "<new_user>",
    pwd: "<some_password>",
    roles: [ { role: "<readWrite>", db: "<database-name>" } ]
  }
)
create user <your-user-name> with password <your-password> createdb"

$ MONGODB_SETTINGS = {
    # 'db': 'flaskbook',
    'host': 'mongodb+srv://<new-user>:<some-password>@cluster0-hcxxx.mongodb.net/<db-name>?authSource=admin&replicaSet=Cluster0-shard-0&w=majority&readPreference=primary&appname=MongoDB%20Compass%20Community&retryWrites=true&ssl=true'
}
$ HOSTNAME = 'HOSTNAME = 'https://yourapp-youruser.pythonanywhere.com'

```

Set environment variables for ON THE 'SETTINGS.PY'  file

> `SECRET_KEY` is your secret key

> `FLASK_CONFIG` is the enviroment you are running on. Should be either `Production`, `Development` or `Testing`. NOTE: its case sensitive

> `ROLE` is the mongo_db user

> `PASSWORD` is the mongo_db password for the user created

> `DEBUG` the default for development configuration is True

> `PORT` the default port for mongo_db service which 5432

> `HOSTNAME` which is the full connection string

> `HOST` which is localhost

> `MONGODB_DB` the name of the app database (NOSQL)


```bash
$ python manage.py runserver
```

Open root path in your browser to test the endpoints. 
You can also use Postman or any other agent to test the endpoints

## APP Testing

To run your tests use

```bash
$ python tests.py or
$ pytest --cov
```
To test endpoints manually fire up postman and run the endpoints

## APP LOCAL VIEW

Once app server is running you can view locally from
```
http://localhost:5000/
```



## How to Access & Run Tests for FRONTEND Online

* Access the hosted app here [here](http://koitoror.pythonanywhere.com/)
=======

# Website
http://thekiplagat.tk/
